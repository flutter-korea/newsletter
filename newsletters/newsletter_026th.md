# **Flutter Seoul Newsletter 26호 (2026년 9월호)**

안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다.

3월호 이후 반년 만에 인사드립니다. 오래 기다려주신 만큼 더 알찬 소식으로 준비했습니다.

아침저녁으로 제법 선선해진 걸 보니 어느덧 추석이 코앞입니다. 연휴 중에는 장애 알림도, 급한 핫픽스도 없는 평온한 시간이 이어지길 바랍니다. 넉넉한 한가위 보내시고, 오가는 길도 안전하게 다녀오세요. 🍂

그사이 Flutter 생태계에는 굵직한 변화가 많았습니다. Material과 Cupertino가 드디어 코어 SDK에서 독립 패키지로 분리된 **Flutter 3.47**이 출시되었고, Google Play는 2027년부터 적용될 메모리 · 코드 최적화 기준과 Zero-Tap Sign-In 요구사항을 발표했습니다. Apple의 첫 폴더블 iPhone인 iPhone Duo도 공개되어, 개발자들이 챙겨야 할 숙제가 부쩍 늘어난 가을입니다. 11월에 열리는 **Flutter Korea 2026** 소식도 함께 전해드립니다.

그럼 뉴스레터 2026년 9월호 시작합니다.

이번 호에서는 다음과 같은 내용을 다룹니다.

* **Flutter 3.47 & Dart 3.13**
* **Flutter Seoul 행사 소식 — Flutter Korea 2026**
* **Google Play 기술 품질 요구사항 (2027년 2월 · 4월 시행)**
* **iPhone Duo & Xcode 27.1 beta 소식**
* **Flutter 오픈소스 소개**

# **Flutter 3.47 & Dart 3.13**

2026년 8월 12일 Flutter와 Dart의 신규 Stable 버전이 릴리즈 되었습니다.

**변경사항 문서:**

* [What's new in Flutter 3.47](https://flutter.dev/blog/whats-new-in-flutter-3-47)
* [Announcing Dart 3.13](https://dart.dev/blog/announcing-dart-3-13)

현재는 패치 업데이트가 다섯 번 진행되어 **Flutter 3.47.5** 버전까지 출시된 상태입니다.

* [CHANGELOG.md](https://github.com/flutter/flutter/blob/master/CHANGELOG.md)

## 🚀 Flutter 3.47 주요 업데이트 하이라이트

이번 릴리스의 부제는 "Modular by design"입니다. 21호(Flutter 3.35)에서 예고로 전해드렸던 Material & Cupertino 분리가 드디어 현실이 되었습니다.

* **Material & Cupertino 독립 패키지 1.0 출시 (opt-in)**
    * `material_ui`, `cupertino_ui`가 pub.dev에 1.0으로 공개되었습니다. 분기별 SDK 릴리스와 무관하게 주 단위로 버그 수정과 신규 컴포넌트가 배포되며, 커뮤니티 기여도 다시 열렸습니다.
    * 마이그레이션: `dart fix --apply --code=migrate_design_widgets`
        * `pubspec.yaml` 갱신이 실패하는 초기 버그가 있습니다. 이 경우 `flutter pub add material_ui` 실행 후 `dart fix --apply`를 다시 실행하세요.
    * 의존 패키지가 아직 기존 import를 쓰고 있어도 `MaterialUiCompatibilityBridge`로 앱을 감싸 먼저 이전할 수 있습니다.
    * `flutter_localizations`도 함께 분리되었습니다. `localizationsDelegates: GlobalMaterialLocalizations.delegates` 한 줄로 Cupertino/Widgets delegate까지 포함됩니다.
    * ⚠️ 코어 SDK에 내장된 기존 라이브러리는 **11월 Fall stable 릴리스에서 공식 deprecated** 될 예정입니다. 패키지 메인테이너라면 이번 이전을 메이저 릴리스로 취급하라는 것이 공식 권고입니다.
* **데스크톱 Impeller 기본 활성화**: macOS, Windows, Linux에서 Impeller가 기본 렌더러가 되었습니다. SDF 기반 렌더링으로 데스크톱 텍스트가 더 선명해졌고, macOS에서는 Wide Gamut Color가 기본 활성화됩니다. Skia 폴백 옵션은 향후 제거될 예정입니다.
* **Widget Previews Stable 승격**: 21호에서 실험적 기능으로 소개했던 Widget Previews가 안정 버전이 되었습니다. `.widget_preview/` 로컬 캐싱으로 시작 속도가 빨라졌고, `PreviewThemeData` API와 웹 에셋 자동 동기화가 추가되었습니다.
* **Web — Wasm 기본화 준비**: Wasm 기본 활성화를 향한 작업이 계속되고 있으며, Wasm deferred loading이 실험적으로 추가되었습니다(main 채널, `--enable-wasm-deferred-loading`). `dart:html`은 Wasm에서 지원되지 않으므로 `package:web` 이전이 필요합니다.
* 🇰🇷 **Windows 한글 입력 캐럿 위치 수정**: 한글 조합 중 캐럿 위치가 어긋나던 문제가 [@CHOIgoung](https://github.com/CHOIgoung)님의 기여로 해결되었습니다. ([#186353](https://github.com/flutter/flutter/pull/186353))

### 🍎 Apple 플랫폼 대응 (업그레이드 전 확인 필수)

* **최소 지원 버전 상향**: iOS 13 → **15**, macOS 10.15 → **12**
* **UIScene lifecycle 필수화**: Xcode 27로 빌드한 앱은 UIScene을 채택하지 않으면 **실행 시 시작에 실패**합니다. 대부분 Flutter CLI가 빌드 중 자동 마이그레이션하지만, `AppDelegate`에 커스텀 네이티브 코드가 있거나 레거시 lifecycle에 의존하는 플러그인을 쓰는 경우 [수동 마이그레이션](https://docs.flutter.dev/release/breaking-changes/uiscene-lifecycle-ios)이 필요합니다.
* **Intel Mac 지원 단계적 종료**: Intel 호스트 빌드 시 경고가 출력되며 향후 오류로 전환됩니다. `flutter config --enable-macos-arm64-only`로 ARM64 전용 빌드를 미리 적용할 수 있습니다.
* **SwiftPM 전환 가속**: 상위 100개 iOS 플러그인 중 92개가 SwiftPM으로 이전했습니다. CocoaPods는 유지보수 모드이며, 미이전 플러그인은 pub.dev 점수가 낮아지고 결국 동작하지 않게 됩니다.

### 🤖 Android 검증 의존성 버전

* Java 17 / KGP 2.4.0 / AGP 9.1.0 / Gradle 9.3.1
* `compileSdk` 36, `targetSdk` 36, `minSdk` 24

## 🚀 Flutter 3.47 패치 업데이트

출시 이후 다섯 번의 패치가 있었습니다. Xcode 27 / iOS 27 대응과 SwiftPM 관련 수정이 많으니, 3.47을 쓰신다면 최신 패치로 올리시길 권장합니다. 전체 내역은 [CHANGELOG.md](https://github.com/flutter/flutter/blob/master/CHANGELOG.md)에서 확인하실 수 있습니다.

* **[3.47.1](https://github.com/flutter/flutter/releases/tag/3.47.1)** - Wasm 웹 빌드의 hot restart와 Pub workspace 환경의 hot reload 문제를 수정했습니다. SwiftPM 병렬 빌드 시 발생하던 race condition을 해결했고, `GeneratedPluginRegistrant` 코드 인젝션 방지를 위한 플러그인 식별자 검증이 추가되었습니다.
* **[3.47.2](https://github.com/flutter/flutter/releases/tag/3.47.2)** - SwiftPM 활성화 시 iOS/macOS 빌드 실패와 Xcode 27에서의 add-to-app 빌드 실패를 수정했습니다. `libpng` 보안 취약점 패치, Linux 터치 이벤트 메모리 누수 수정, Windows 외부 텍스처 크래시 수정이 포함됩니다. 데스크톱 빌드에 `--build-name` / `--build-number`가 반영됩니다.
* **[3.47.3](https://github.com/flutter/flutter/releases/tag/3.47.3)** - `Actions.handler`가 항상 null을 반환하던 문제를 수정했습니다. PowerVR B-Series GPU Android 기기의 Impeller 렌더링 이상 및 성능 저하를 개선했고, Android cmdline-tools 23.0+에서 `flutter doctor`의 라이선스 상태 오표기를 수정했습니다.
* **[3.47.4](https://github.com/flutter/flutter/releases/tag/3.47.4)** - Xcode 27 디버깅 시 앱이 흰 화면에서 수 분간 멈추던 문제를 수정했습니다. native assets를 포함한 iOS 앱의 App Store 제출 실패 문제도 해결되었습니다. Windows Smart App Control 등 보안 정책 차단 시 크래시 대신 안내 메시지를 출력합니다.
* **[3.47.5](https://github.com/flutter/flutter/releases/tag/3.47.5)** - iOS 27 실기기 디버깅 중 간헐적 크래시를 수정했습니다. Widget Previewer에서 그룹을 다시 펼칠 때 발생하던 크래시와 DDS 시작 실패 시 flutter_tools 크래시도 수정되었습니다.

## 🎯 Dart 3.13 주요 업데이트

* **Primary constructors Stable**: Dart 3.12에서 실험적으로 공개되었던 primary constructor가 정식 기능이 되었습니다. 필드 선언과 생성자를 클래스 헤더 한 줄로 작성할 수 있습니다.

    ```dart
    class Point(final int x, final int y);
    ```

    * 본문이 비어 있는 선언은 `{}` 대신 `;`로 끝낼 수 있고, `empty_container_bodies`, `initialize_in_field_declaration` 등 새 lint와 자동 수정이 함께 제공됩니다.
* **dart2wasm deferred loading 프리뷰**: 대규모 웹 앱의 초기 로딩 최적화를 위한 Wasm 지연 로딩이 실험적 플래그로 제공됩니다.

# **Flutter Seoul 행사 소식**

## Flutter Korea 2026

올해도 **Flutter Korea**가 돌아옵니다!

Flutter Korea는 Flutter Seoul이 매년 주최하는 국내 Flutter 개발자 컨퍼런스입니다. 현업 개발자들이 실무에서 겪은 문제와 해결 과정을 세션으로 나누고, 평소 온라인으로만 만나던 커뮤니티 구성원들이 한자리에 모여 교류하는 자리입니다.

지난해 구글 스타트업 캠퍼스에서 열린 [Flutter Korea 2025](https://github.com/flutter-korea/newsletter/blob/main/newsletters/newsletter_023rd.md)에서는 접근성, 딥링크, gRPC, 오픈소스 기여 등 다양한 주제의 세션과 핸즈온, 그리고 2시간 동안 진행된 바이브 코딩 해커톤까지 풍성한 하루를 보냈습니다. 올해는 장소를 아마존 코리아로 옮겨 진행합니다. 세션과 프로그램 등 상세 내용은 예매 페이지를 통해 안내드릴 예정이니 많은 관심과 참여 부탁드립니다.

* 티켓 예매 링크: **[Flutter Korea 2026 | 티켓타코](https://ticketa.co/event/c9xsstcs)**
* 일자: 2026년 11월 7일 (토) 11시 00분 ~
* 장소: 아마존 코리아 (서울 강남구 테헤란로 231 센터필드 EAST 12층)
* 주최: Flutter Seoul

# **Google Play 기술 품질 요구사항 (2027년 2월 · 4월 시행)**

Google이 8월 26일 [Android Developers Blog](https://android-developers.googleblog.com/2026/08/app-quality-memory-optimization-secure-onboarding.html)를 통해 Google Play의 새로운 기술 품질 요구사항을 발표했습니다. 기준을 충족하지 못하면 **Play 스토어 노출과 게시(업데이트) 권한에 영향**을 받을 수 있으며, 선택 사항이 아닙니다. 상세 기준은 [Play Console 고객센터 문서](https://support.google.com/googleplay/android-developer/answer/17492799)에서 확인하실 수 있습니다.

## 📉 2027년 2월부터 — 메모리 사용량 & 코드 최적화

RAM 가격 상승으로 인한 기기 메모리 제약에 대응하기 위한 조치로, Android vitals의 core vitals에 메모리 지표 두 가지가 새로 추가됩니다. 최근 28일 데이터의 **90번째 백분위(P90)** 값으로 평가하며, 모바일/태블릿 폼팩터에만 적용됩니다. (Android 13 이상 기기의 데이터로 평가)

* **메모리 사용량 (Anonymous RSS + Swap)**: 기기 RAM 등급(4 GB ~ 16 GB)과 앱 상태별로 기준치가 다릅니다. 예를 들어 8 GB 기기에서 일반 앱은 Foreground 2.25 GB, Background 1.5 GB가 기준이며, 게임은 더 높은 기준치가 적용됩니다. 전체 기준표는 [고객센터 문서](https://support.google.com/googleplay/android-developer/answer/17492799)를 참고하세요.
* **Bitmap 메모리 사용량**: 화면에 보이지 않는 상태에서 bitmap을 오래 쥐고 있으면 안 됩니다. User-perceived services / Background 상태에서 200 MB, Cached 상태에서 400 MB가 기준치입니다.
* **DEX 코드 최적화**: DEX 코드가 **10 MB를 초과하는 앱**(게임은 50 MB)은 Play Console에 업로드하는 번들에서 난독화(Obfuscation) · 최적화(Optimization) · 축소(Shrinking) 각각 **최소 25%** 를 달성해야 합니다. R8 사용을 권장하지만 필수는 아닙니다. 내 앱의 DEX 크기와 최적화 비율은 Play Console의 **App bundle explorer**에서 확인할 수 있습니다.

각 지표는 Play Console → Android vitals의 **Memory** 항목에서 지금 바로 확인할 수 있으니, 시행 전에 현재 수치를 점검해 보시길 권장합니다.

## 🔑 2027년 4월부터 — Zero-Tap Sign-In Restoration

로그인 기능이 있는 앱(선택 로그인 포함)은 사용자가 **새 Android 기기로 이전하며 데이터를 복원할 때 로그인 상태가 자동으로 복원**되어야 합니다. [Restore Credentials API](https://developer.android.com/identity/sign-in/restore-credentials)(Android 9 이상)를 사용하는 것이 기본 방법입니다.

* 게임은 현재 대상에서 제외되며, 금융·헬스케어 등 규제 대상 앱은 Play Console을 통해 예외를 신청할 수 있습니다.
* ⏰ **[Block Store](https://developer.android.com/identity/block-store)로 구현한 경우 2026년 9월 30일까지 프로덕션에 적용된 건에 한해** 요구사항을 충족한 것으로 인정됩니다. 이후의 신규 연동은 Restore Credentials API를 사용해야 합니다.
* MFA를 우회하는 기능이 아닙니다. 복원된 기기에서 추가 인증을 요구할지는 앱이 결정하며, 사용자 식별 컨텍스트를 복원하는 것만으로도 요구사항은 충족됩니다.

# **iPhone Duo & Xcode 27.1 beta 소식**

9월 9일 Apple의 첫 폴더블 iPhone인 **iPhone Duo**(외부 5.4" / 내부 7.6")가 발표되었습니다. 10월 23일 iOS 27.1과 함께 출시됩니다.

* **시뮬레이터**: 9월 18일 공개된 **Xcode 27.1 beta**(macOS 26.6 이상 필요)에 iPhone Duo 시뮬레이터가 포함되었습니다. Device Hub에서 iPhone Duo를 선택하면 화면 하단 컨트롤로 열기 / 닫기 / 회전 / 접기 포즈를 전환하며 레이아웃을 확인할 수 있습니다.
    * 베타 known issues ([릴리스 노트](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_1-release-notes)): iPhone Duo 시뮬레이터에서 StandBy 미지원 및 대부분의 App Extension 실행·디버깅 불가, 시뮬레이터 첫 실행에 수 분 소요
* **빌드 SDK에 따라 화면 활용 범위가 달라집니다**: 재빌드 없이도 실행은 되지만, iOS 27 SDK로 빌드하면 내부 디스플레이에서 상태바 왼쪽 영역까지, iOS 27.1 SDK로 빌드해야 화면 끝까지 확장됩니다.
* **Flutter 프레임워크 지원 현황**: `MediaQuery.displayFeatures`는 현재 Android에서만 채워지기 때문에, Flutter 앱은 iPhone Duo의 접힘 상태나 fold 영역을 알 수 없습니다. iOS 27.1의 reserved region API를 `DisplayFeature`로 매핑하자는 제안이 [flutter/flutter#192515](https://github.com/flutter/flutter/issues/192515)에 올라와 있습니다.

레이아웃 가이드는 Apple Tech Talk [Prepare your app for iPhone Duo](https://developer.apple.com/videos/play/tech-talks/111461/)를 참고하세요.

# **Flutter 오픈소스 소개**

## hAudiotagger

[https://pub.dev/packages/haudiotagger](https://pub.dev/packages/haudiotagger)

Flutter에서 오디오 파일의 메타데이터(제목, 아티스트, 앨범, 앨범 아트, 가사 등)를 읽고 쓸 수 있는 오픈소스 패키지입니다. Rust의 오디오 메타데이터 라이브러리 [lofty](https://github.com/Serial-ATA/lofty-rs)를 [flutter_rust_bridge](https://github.com/fzyzcjy/flutter_rust_bridge)로 연결한 구조로, **Android, iOS, Linux, macOS, Windows, Web** 6개 플랫폼을 모두 지원합니다. 9월 18일 2.0.0 버전이 공개되었으며 MIT 라이선스입니다.

* **폭넓은 포맷 지원**: MP3, FLAC, MP4/M4A, Ogg Vorbis, Opus, AAC, WAV, AIFF, APE, WavPack 읽기/쓰기
* **부분 업데이트**: 다른 필드는 그대로 두고 원하는 필드만 수정 (`Haudiotagger.update`)
* **배치 처리**: 여러 파일을 한 번에 처리하고 진행률 콜백 제공. 제작자 벤치마크(Linux, 약 8 MB MP3 100개) 기준 읽기 1,282 files/s
* **확장 메타데이터**: MusicBrainz, AcoustID, ISRC 등 60개 이상의 필드, ReplayGain, MP3 챕터(팟캐스트 · 오디오북용) 지원
* **Web 지원**: 파일 경로 대신 `readFromBytes` / `writeToBytes` 등 bytes 기반 API를 사용하며, cross-origin isolation 설정이 필요합니다. ([Web Setup](https://github.com/Hirdaya-Shrestha/haudiotagger/wiki/Web-Setup))

음악 플레이어, 팟캐스트, 오디오북 앱을 만들고 계시다면 살펴볼 만합니다. 설치 없이 브라우저에서 [라이브 데모](https://haudiotagger.hirdaya-shrestha.com.np/)를 바로 써볼 수 있습니다. 아직 활발히 개발 중인 프로젝트로, 제작자가 Reddit 글을 통해 피드백과 기능 제안을 받고 있습니다.

* [GitHub 저장소](https://github.com/Hirdaya-Shrestha/haudiotagger)
* [Reddit 소개 글](https://www.reddit.com/r/FlutterDev/comments/1wcr7bk/i_built_an_audio_metadata_library_for_flutter/)

## android_restore_credentials

[https://pub.dev/packages/android_restore_credentials](https://pub.dev/packages/android_restore_credentials)

위에서 소개한 Google Play의 **Zero-Tap Sign-In Restoration**(2027년 4월 시행) 요구사항에 Flutter 앱이 대응할 수 있도록, Android의 [Restore Credentials API](https://developer.android.com/identity/sign-in/restore-credentials)를 감싼 Android 전용 플러그인입니다. WunderBytes에서 9월 3일 0.1.0 버전을 공개했으며 BSD-3-Clause 라이선스입니다.

* **API**: 로그인 후 `createRestoreKey`, 새 기기 첫 실행 시 `getRestoreKey`, 로그아웃 시 `clearRestoreKey` 세 가지로 구성됩니다. Android 9(API 28) 이상에서 동작하며, 멀티 플랫폼 앱에서는 Android에서만 호출하도록 분기해야 합니다.
* **2단계 복원 구조**: 기기 복원 직후 Flutter 엔진 없이 실행되는 `BackupAgent.onRestoreFinished`(백그라운드)와 앱 첫 실행 시점(포그라운드) 두 곳에서 복원을 시도하는 구성을 안내합니다. 백그라운드 단계는 플러그인이 제공하는 Kotlin 클라이언트를 호스트 앱에서 직접 호출해야 합니다.
* **서버 작업 필요**: 클라이언트 전용 플러그인입니다. `requestJson`은 WebAuthn 옵션 JSON이며, 서버(RP)에서 restore key의 등록 · 검증 · 저장을 구현해야 합니다. README에 passkey와 구분해 저장하기, 기기별 다중 키 지원, TTL 설계 등 백엔드 고려 사항이 정리되어 있습니다.

아직 0.1.0 초기 버전이므로 도입 전 직접 검증이 필요하지만, 요구사항 대응을 어디서부터 시작해야 할지 막막하다면 README만 읽어봐도 전체 그림을 잡는 데 도움이 됩니다.

* [GitHub 저장소](https://github.com/wunderbytes/android_restore_credentials)
* [Reddit 소개 글](https://www.reddit.com/r/FlutterDev/comments/1wdfi4j/plugin_for_new_android_requirement_zerotap_signin/)

## Flutter Production Starter

[https://github.com/Ali-El-Khatib/flutter-production-starter](https://github.com/Ali-El-Khatib/flutter-production-starter)

**Dart Pub Workspaces**와 **Melos**를 함께 사용하는 프로덕션 지향 Flutter 모노레포 스타터입니다. 제작자는 기존 스타터 템플릿들이 "모든 것을 한 폴더에 넣은 지나치게 단순한 구조"이거나 "토글 버튼 하나에도 인터페이스를 요구하는 과도한 추상화" 둘 중 하나라는 문제의식에서 출발했다고 밝히고 있습니다. Pub Workspaces가 패키지 간 로컬 링크와 단일 lockfile을 담당하고, Melos는 포맷 · 코드 생성 · 분석 · 테스트 · 커버리지 등 워크스페이스 전체 명령을 실행하는 역할로 나뉘어 있습니다. Flutter 3.47.0 기준으로 작성되었으며 MIT 라이선스입니다.

* **구성**: `apps/mobile` 앱 1개 + 패키지 7개 (`app_core`, `app_network`, `app_storage`, `design_system`, `app_lints`, `auth_contract`, `auth`)
* **실용적인 Clean Architecture**: 설정 화면 같은 단순한 기능은 Presentation + State만 두고, 인증처럼 복잡한 기능에만 Use Case · Data Source 계층을 적용합니다. 작은 기능은 앱 안에 feature-first로 두고, 독립된 계약(contract)과 경계를 가진 기능만 패키지로 분리합니다.
* **환경 분리**: dev / staging / prod 엔트리 포인트를 제공하며, 데모용 샘플 데이터는 개발 환경에서만 동작하고 staging · production에서는 요청 실패가 그대로 실패로 드러나도록 구성되어 있습니다.
* **CI**: GitHub Actions에서 Flutter 버전을 고정하고 포맷 · 분석 · 테스트와 함께 모바일 라인 커버리지 60% 하한을 검사합니다.
* **사용 스택**: `kaisel`(라우팅 · route guard), `bloc_signals` + `signals_flutter`(상태 관리), `get_it` + `injectable`(DI), `dio`(네트워크, 로그에서 토큰 · 비밀번호 마스킹), `Result<T>` + `Failure` 기반 에러 처리

스타터를 그대로 쓰지 않더라도, Pub Workspaces와 Melos의 역할을 어떻게 나누는지, 어떤 기능을 패키지로 분리할지에 대한 기준을 참고하기 좋습니다. 저장소의 [ARCHITECTURE.md](https://github.com/Ali-El-Khatib/flutter-production-starter/blob/main/ARCHITECTURE.md)와 [제작자의 소개 글](https://dev.to/alielkhatib/architecting-a-production-grade-flutter-monorepo-lego-modular-boundaries-melos-blocsignals-bf)에 설계 의도가 정리되어 있습니다.

* [Reddit 소개 글](https://www.reddit.com/r/FlutterDev/comments/1w0t3hk/open_sourced_a_productiongrade_flutter_monorepo/)

---

# **마치며**

반년 만의 뉴스레터, 끝까지 읽어주셔서 감사합니다. 이번 호에 미처 담지 못한 소식들은 다음 호에서 이어서 전해드리겠습니다. 앞으로는 다시 매달 찾아뵐 수 있도록 하겠습니다.

모두 풍성한 한가위 보내시고, 11월 Flutter Korea 2026에서 직접 뵙겠습니다. 🙇‍♂️

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)
