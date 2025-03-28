# **25/03 뉴스레터**

안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다.

봄의 시작을 알리는 3월이 찾아왔습니다. 따스한 햇살과 함께 새로운 에너지가 넘치는 이 계절에, 플러터 커뮤니티도 더욱 활기찬 모습으로 여러분을 맞이합니다. 이번 호에서는 플러터 개발자 여러분께 영감과 실질적인 도움을 드릴 수 있는 소식들을 준비했습니다. 함께 확인해 볼까요?

이번 호에서는 다음과 같은 내용을 다룹니다.

* **Flutter Seoul 이벤트 관련 소식**
* **Flutter 3.29 패치 업데이트 소식**
* **Flutter 패키지 소식**
* **Flutter 관련 게시글**

---

# **1\. Flutter 3.29 패치 업데이트 소식**

2월에 3.29.0 마이너 버전이 업데이트 된 후로 2번의 패치 업데이트가 있었습니다.

이번 업데이트는 UI, 성능, 안정성을 모두 잡았습니다. flutter upgrade 명령어를 실행해 최신 안정화 버전으로 업데이트 가능합니다.\!

### **주요 요약**

* 3월 7일 Flutter 3.29.1 버전에는 UI 애니메이션 개선, 테스트 및 CI 설정 변경, 오류 처리 강화, 그래픽 렌더링 문제 수정, 성능 향상, 메모리 관리 개선, 도구 기능 업데이트가 포함되었습니다.
* 3월 14일 Flutter 3.29.2 버전에는 웹 및 안드로이드 성능 개선, iOS 및 전체 플랫폼의 버그 수정이 있었습니다.

### **상세 설명**

#### **Flutter 3.29.1 변경사항 (3월 7일)**

이 버전은 다양한 영역에서 개선이 이루어졌습니다:

* **UI 및 애니메이션:** 탭의 선형 및 탄성 애니메이션 깜박임 수정, 글리프의 떨림 문제 해결, 아이콘이 있는 버튼의 전경색 무시 문제 수정.
* **테스트 및 CI:** macOS 14에서 테스트 실행을 위한 설정 변경, 마스터 브랜치 업데이트 시 LUCI 구성에 .ci.yaml 변경 반영, 웹 테스트를 위한 safaridriver 런치 프로세스 개선.
* **오류 처리:** iPhone에서 JIT 제한으로 인한 앱 충돌 시 안내 오류 메시지 제공.
* **테스트 수정:** 특정 순서 시드(예: 20250221)에서 실패하는 reorderable\_list\_test.dart 테스트 수정.
* **그래픽 및 렌더링:** 특정 GLES 드라이버에서 BackdropFilters 사용 시 충돌 수정, 안드로이드의 문제 있는 Xclipse GPU 드라이버 및 Exynos SoC에서 Vulkan 비활성화, Impeller DrawVertices 문제 수정.
* **성능 향상:** iOS 장치에서 스크롤 부드러움 개선, 안드로이드에서 전경으로 돌아올 때 텍스트 깜빡임 수정.
* **메모리 관리:** OpenGL "flipped" 텍스처 누출 방지.
* **도구 기능:** Flutter 도구가 추적된 engine.version을 존중하도록 수정, engine.version 오버라이드 전 확인 추가.

| 카테고리 | 설명 | 풀 리퀘스트 번호 |
| ----- | ----- | ----- |
| UI 및 애니메이션 | 탭 선형 및 탄성 애니메이션 깜박임 수정, 글리프 떨림 문제 해결, 버튼 아이콘 전경색 무시 문제 수정 | 163830, 163058, 163201 |
| 테스트 및 CI | macOS 14 테스트 실행 설정 변경, LUCI 구성 업데이트, 웹 테스트용 safaridriver 개선 | 164119, 164155, 164191, 163316 |
| 오류 처리 | iPhone JIT 제한 충돌 시 안내 오류 메시지 제공 | 164193 |
| 테스트 수정 | reorderable\_list\_test.dart 특정 시드 실패 문제 수정 | 164050 |
| 그래픽 및 렌더링 | BackdropFilters 충돌 수정, 안드로이드 Vulkan 비활성화, Impeller 문제 해결 | 163581, 163616, 163265, 163261 |
| 성능 향상 | iOS 스크롤 부드러움 개선, 안드로이드 전경 복귀 텍스트 깜빡임 수정 | 163666, 163754 |
| 메모리 관리 | OpenGL 텍스쳐 누출 방지 | 163667 |
| 도구 기능 | engine.version 추적 및 확인 기능 강화 | 163741, 163672 |

자세한 내용은 아래의 링크를 참고해보세요.

* [flutter/163830](https://github.com/flutter/flutter/pull/163830) \- Fix Tab linear and elastic animation blink.
* [flutter/164119](https://github.com/flutter/flutter/pull/164119) \- Configuration changes to run test on macOS 14 for Flutter's CI.
* [flutter/164155](https://github.com/flutter/flutter/pull/164155) \- Roll .ci.yaml changes into the LUCI configuration only when the master branch is updated.
* [flutter/164191](https://github.com/flutter/flutter/pull/164191) \- Improve safaridriver launch process in Flutter's CI testing for web.
* [flutter/164193](https://github.com/flutter/flutter/pull/164193) \- Provide guided error message when app crashes due to JIT restriction on iPhones.
* [flutter/164050](https://github.com/flutter/flutter/pull/164050) \- Fixes test reorderable\_list\_test.dart failing for certain ordering seeds, such as 20250221\.
* [flutter/163316](https://github.com/flutter/flutter/pull/163316) \- Configuration changes to run test on macOS 14 for Flutter's CI.
* [flutter/163581](https://github.com/flutter/flutter/pull/163581) \- Fix crash when using BackdropFilters in certain GLES drivers.
* [flutter/163616](https://github.com/flutter/flutter/pull/163616) \- Disable Vulkan on known bad Xclipse GPU drivers for Android.
* [flutter/163666](https://github.com/flutter/flutter/pull/163666) \- Always post new task during gesture dispatch to fix jittery scrolling on iOS devices.
* [flutter/163667](https://github.com/flutter/flutter/pull/163667) \- Ensure that OpenGL "flipped" textures do not leak via texture readback.
* [flutter/163741](https://github.com/flutter/flutter/pull/163741) \- Flutter tool respects tracked engine.version.
* [flutter/163754](https://github.com/flutter/flutter/pull/163754) \- Fix text glitch when returning to foreground for Android.
* [flutter/163058](https://github.com/flutter/flutter/pull/163058) \- Fixes jittery glyphs.
* [flutter/163201](https://github.com/flutter/flutter/pull/163201) \- Fixes buttons with icons that ignore foregroundColor.
* [flutter/163265](https://github.com/flutter/flutter/pull/163265) \- Disable Vulkan on known bad exynos SoCs for Android.
* [flutter/163261](https://github.com/flutter/flutter/pull/163261) \- Fixes for Impeller DrawVertices issues involving snapshots with empty sizes.
* [flutter/163672](https://github.com/flutter/flutter/pull/163672) \- Check for tracked engine.version before overriding.

#### **Flutter 3.29.2 변경사항 (3월 14일)**

이 버전은 성능과 안정성에 중점을 둔 업데이트를 포함합니다:

* **성능 향상:** 웹용 CanvasKit 렌더링 성능 개선, 지원되는 경우 안드로이드 플랫폼 뷰에 하드웨어 버퍼 항상 사용.
* **버그 수정:** iOS에서 toImage/toImageSync 표면 할당 실패로 인한 충돌 수정, canvaskit.wasm의 이중 다운로드 문제 해결, v2 임베더 마이그레이션 후 안드로이드 앱에 빈 io.flutter.app.FlutterApplication 재추가, 스크롤 가능한 항목과 동시에 애니메이션 및 상호작용 시 발생하는 전체 플랫폼 충돌 수정.

| 카테고리 | 설명 | 풀 리퀘스트 번호 |
| ----- | ----- | ----- |
| 성능 향상 | 웹용 CanvasKit 렌더링 성능 개선, 안드로이드 플랫폼 뷰 하드웨어 버퍼 사용 | 163175, 164201 |
| 버그 수정 | iOS toImage 충돌 수정, canvaskit.wasm 이중 다운로드 문제 해결, 안드로이드 앱 지원 재추가, 스크롤 충돌 수정 | 164628, 162198, 164024, 164392 |

자세한 내용은 아래의 링크를 참고해보세요.

* [flutter/163175](https://github.com/flutter/flutter/pull/163175) \- Improve performance of CanvasKit rendering for web.
* [flutter/164628](https://github.com/flutter/flutter/issues/164628) \- iOS Fixes crash when allocation of surface for toImage/toImageSync fails.
* [flutter/164201](https://github.com/flutter/flutter/pull/164201) \- Always use Android hardware buffers for platform views when supported.
* [flutter/162198](https://github.com/flutter/flutter/issues/162198) Fixes double-download of canvaskit.wasm
* [flutter/164024](https://github.com/flutter/flutter/issues/164024): \- Add back an empty io.flutter.app.FlutterApplication for Android apps post v2 embedder migration.
* [flutter/162198](https://github.com/flutter/flutter/issues/162198) \- Fixes double-download of canvaskit.wasm
* [flutter/164392](https://github.com/flutter/flutter/pull/164392) \- All platforms, Fixes a crash that can occur when animating and interacting with a scrollable simultaneously.

---

#### **결론**

Flutter 3.29.1 및 3.29.2는 프레임워크의 안정성과 성능을 강화하는 데 중점을 둔 업데이트로, 특히, 웹 및 모바일 플랫폼 간의 통합성과 안정성이 크게 향상되었습니다.

👉 [Flutter CHANGELOG.md](https://github.com/flutter/flutter/blob/master/CHANGELOG.md)

# **2\. 플러터 서울 이벤트 소식**

**📣 \[Flutter Seoul 4월 오픈스테이지\] 연사 모집 안내**

안녕하세요, Flutter Seoul입니다. 오는 4월 오픈스테이지 행사에서 발표를 함께할 연사님을 모집합니다.  
이번 오픈스테이지는 Flutter 개발자뿐 아니라 다양한 기술과 경험을 가진 분들 모두에게 열린 무대입니다.  
Flutter는 물론, 모바일·웹·서버·AI·디자인 등 다양한 분야의 발표 또는 구인/구직, 사이트 프로젝트 소개도 좋습니다. 부담 없이 여러분의 이야기를 들려주세요.

👉 발표자 신청하기 링크  
[https://forms.gle/C7EUYFXZaAKDy2To6](https://forms.gle/C7EUYFXZaAKDy2To6)

📝 신청 방법  
아래 폼을 통해 발표 주제와 간단한 소개를 적어주세요.

🔥 오픈스테이지는 누구나 주인공이 될 수 있는 자리입니다.  
기술, 경험, 고민, 도전, 실패, 성장… 어떤 이야기든 환영합니다.  
함께 만들고, 함께 나누는 자리에 여러분을 초대합니다\!

🎤 모집 대상  
개발 또는 비개발 관련 주제로 발표를 해보고 싶은 누구나  
(신입/경력/비개발자 등 무관, 처음 발표하는 분도 환영합니다\!)

📌 발표 주제 예시  
• Flutter를 도입하면서 겪은 시행착오  
• Riverpod vs Bloc, 나는 이렇게 선택했다  
• 서버와 클라이언트의 실전 협업 팁  
• AI/ML, 백엔드, 디자인 시스템 등 관심 있는 어떤 주제든 OK  
• 개인 앱 출시 후 경험 공유  
• 우리 회사 구인/구직  
• 커리어 전환 이야기  
• 내가 만든 Flutter 사이드 프로젝트

🙌 발표 형식 및 시간  
• 발표 시간: 20\~30분 (Q\&A 포함)  
• 발표 형식: 자유 (슬라이드/데모/토크 등 편한 방식)  
• 발표 장소: 장소는 추후 안내 예정

🗓 행사 일정  
• 행사 일시: 2024년 4월 중 (정확한 일정은 개별 안내 예정)  
• 연사 모집 마감: 4월 5일(금) 까지

# **3\. Flutter 패키지 소식**

3.1 [versionarte | Flutter package](https://pub.dev/packages/versionarte)

versionarte는 앱의 버전 관리와 가용성을 원격으로 처리할 수 있는 패키지입니다. 주요 기능은 다음과 같습니다:

* 사용자가 최신 버전으로 업데이트하도록 강제.
* 업데이트 알림 표시.
* 유지보수 모드에서 앱 비활성화 가능.
* UI를 앱 브랜딩에 맞게 커스터마이징 가능.

Firebase Remote Config나 RESTful API와 같은 제공자를 통해 버전 정보를 가져오며, 이는 백엔드 시스템과의 통합을 용이하게 합니다. 이 패키지는 보안 업데이트나 새로운 기능 도입 시 유용합니다.

3.2 [flutter\_numeric\_text | Flutter package](https://pub.dev/packages/flutter_numeric_text)

flutter\_numeric\_text는 텍스트, 특히 숫자 텍스트에 애니메이션을 추가할 수 있는 위젯입니다. 이는 UI를 더 동적이고 매력적으로 만듭니다. 주요 특징:

* 표준 Text 위젯과 유사하게 쉽게 통합.
* 애니메이션 지속 시간과 스타일 커스터마이징 가능.
* 텍스트 정렬, 방향 등 다양한 속성 지원.

카운트다운 타이머, 진행률 표시기 등에서 유용하며, 텍스트 변화에 시각적 매력을 더할 수 있습니다.

3.3 [http\_cache\_stream | Flutter package](https://pub.dev/packages/http_cache_stream)

http\_cache\_stream은 원격 콘텐츠를 동시에 다운로드, 캐싱, 스트리밍할 수 있는 패키지로, 미디어 플레이어와 같은 앱에 적합합니다. 주요 이점:

* 캐싱을 통해 성능 개선.
* 네트워크 연결이 불안정할 때도 원활한 스트리밍 경험 제공.
* 미디어 플레이어 및 웹 콘텐츠 스트리밍 플러그인에 이상적.

이 패키지는 연속 재생이나 실시간 업데이트가 필요한 콘텐츠에서 사용자 경험을 향상시킵니다.

**3.4 pixel\_preview**

* 다양한 기기 크기에서 UI 컴포넌트를 미리 볼 수 있어 반응형 디자인을 쉽게 테스트할 수 있습니다. iPhone, Samsung, iPad 등 디바이스 프리셋 제공.

# **4\. Flutter 관련 게시글**

[10 Lesser-Known Dart and Flutter Functionalities You Should Start Using | by Majid Hajian | DCM Analyzer | Mar, 2025 | Medium](https://medium.com/dcm-analyzer/10-lesser-known-dart-and-flutter-functionalities-you-should-start-using-6f931460ec71)  
Dart와 Flutter의 덜 알려진 기능들을 중심으로, 개발자들이 이를 활용해 워크플로우를 개선하고 애플리케이션의 성능과 안정성을 높일 수 있는 방법을 다룹니다.

| 번호 | 기능명 | 설명/사용 사례 |
| :---- | :---- | :---- |
| 1 | Future.any | 여러 비동기 작업 중 하나가 완료되면 즉시 결과를 반환, 성공 또는 오류 처리 가능. |
| 2 | scheduleMicrotask | 마이크로태스크 큐에 콜백을 추가, 다음 이벤트 루프 작업 전에 실행. |
| 3 | compute | CPU 집약적 작업을 백그라운드 아이솔레이트로 오프로드, UI 스레드 반응성 유지. |
| 4 | @pragma('vm:notify-debugger-on-exception') 및 FlutterError.reportError | 잡힌 예외에서 디버거 중단, 구조화된 오류 보고와 함께 사용. |
| 5 | runZonedGuarded | 잡히지 않은 비동기 오류를 가로채는 오류 존 생성, 핸들러 함수로 라우팅. |
| 6 | Timeline.startSync / Timeline.timeSync | Flutter DevTools 타임라인에서 성능 프로파일링을 위한 수동 계측. |
| 7 | unawaited | 의도적으로 대기하지 않는 비동기 작업 표시, 린터 경고 억제. |
| 8 | FutureRecord2 | 여러 비동기 작업을 병렬로 대기, 결과 레코드 반환, 오류 처리 지원. |
| 9 | Expando | 객체 구조 수정 없이 동적으로 속성 연결, 메타데이터에 유용. |
| 10 | addPostFrameCallback | 프레임 렌더링 후 콜백 예약, 빌드 후 위젯 속성 접근에 유용. |

[15 Common Mistakes in Flutter and Dart Development (and How to Avoid Them) | DCM \- Code Quality Tool for Flutter Developers](https://dcm.dev/blog/2025/03/24/fifteen-common-mistakes-flutter-dart-development/)  
이 블로그는 Flutter와 Dart 개발에서 자주 발생하는 15가지 실수를 다루며, 각 실수의 원인, 문제점, 그리고 이를 피하는 방법을 설명합니다. 또한, DCM.dev의 도구와 규칙을 활용하여 이러한 문제를 해결할 수 있는 방법을 제안합니다

| 번호 | 실수 | 설명 |
| :---- | :---- | :---- |
| 1 | 메모리 누수로 인한 자원 해제 실패 | AnimationController, TextEditingController 등 자원을 해제하지 않아 메모리 누수 발생. |
| 2 | setState를 통한 불필요한 재빌드 | setState()를 오용하여 위젯 전체 재빌드, 성능 저하 초래. |
| 3 | 깊은 위젯 트리 및 과도한 재빌드 | 깊은 위젯 트리로 성능 문제 발생, RepaintBoundary 사용으로 개선 가능. |
| 4 | 비동기 처리 부실 | Future와 Stream API 오용으로 오류 미처리, 위젯 상태 문제 발생. |
| 5 | 이미지 최적화 부족 | 최적화되지 않은 이미지로 앱 크기 및 메모리 사용 증가, cacheWidth/Height로 개선. |
| 6 | 오류 처리 부실 | 빈 catch 블록이나 스택 트레이스 손실로 디버깅 어려움. |
| 7 | 비효율적인 테스트 | 어설션 없는 테스트나 중복 어설션으로 테스트 효율성 저하. |
| 8 | 패키지 과부하 | 불필요한 패키지 사용으로 미사용 종속성 증가, DCM.dev로 점검 가능. |
| 9 | 화면 크기 적응 실패 | 고정된 치수로 다른 화면에서 레이아웃 문제, MediaQuery 사용 권장. |
| 10 | BuildContext 오용 | 위젯 해제 후 BuildContext 사용으로 오류 발생, 동기적 사용 필요. |
| 11 | 비효율적인 코드 구조 | UI, 상태, 로직 혼합으로 유지보수성 저하, 코드 구조 분석 도구 활용. |
| 12 | GlobalKey 부적절한 사용 | 성능 문제와 캡슐화 파괴로 이어질 수 있음, 최소한으로 사용 권장. |
| 13 | FutureBuilder 및 StreamBuilder 남용 | build()에서 반복 생성으로 성능 저하, 외부에서 생성 권장. |
| 14 | 위젯 라이프사이클 메서드 부적절한 사용 | initState()에서 비동기 호출로 문제 발생, 라이프사이클 준수 필요. |
| 15 | 미사용 코드 및 파일 유지 | 미사용 코드/파일로 프로젝트 복잡도 증가, 정기 점검 및 제거 권장. |

[Using Semantics Identifiers for UI Testing](https://codewithandrea.com/tips/semantics-identifiers-ui-testing/)

Semantics Identifiers는 Flutter에서 UI 테스트를 간편하게 만듭니다. Semantics 위젯에 semanticsLabel을 추가해 위젯을 쉽게 식별하고, find.bySemanticsLabel로 테스트에서 접근성을 높이며 안정적인 테스트를 지원합니다. 접근성 개선과 테스트 효율성을 동시에 챙길 수 있는 유용한 기능입니다.

---

이번 호에서는 Flutter Seoul 이벤트, Flutter 3.29 패치 업데이트, 새로운 패키지 소식, 그리고 유용한 게시글들을 소개해 드렸습니다. 여러분의 개발 여정에 작은 영감과 도움이 되었기를 바랍니다.

여러분의 열정과 참여 덕분에 플러터 커뮤니티가 더욱 빛나고 있습니다. 다음 호에서도 최신 소식과 유익한 정보를 가득 담아 찾아뵙겠습니다. 늘 함께해 주셔서 감사합니다\! 🚀

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)
