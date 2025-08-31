# Flutter Seoul Newsletter 21호

안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다.

8월이 저물어가는 가운데, Flutter와 Dart 생태계에 흥미진진한 소식들이 가득합니다. 이번 달에는 특히 AI 통합과 개발자 생산성 향상에 중점을 둔 Flutter 3.35와 Dart 3.9가 출시되어 많은 화제를 모았는데요, 새로운 기능들과 함께 주목할 만한 패키지들도 소개해드리겠습니다.

여름의 마지막을 장식하는 이번 뉴스레터도 즐겁게 읽어보시길 바랍니다\! 🌻

이번 호에서는 다음과 같은 내용을 다룹니다.

* Flutter 3.35 & Dart 3.9
* Flutter Seoul 행사 소식
* 한국 Flutter 행사 소식
* Flutter 관련 오픈소스

# Flutter 3.35 & Dart 3.9

2025년 8월 15일 Flutter와 Dart의 신규 Stable 버전이 릴리즈 되었습니다.

**변경사항 문서:**

* [What's new in Flutter 3.35](https://medium.com/flutter/whats-new-in-flutter-3-35-c58ef72e3766)
* [Announcing Dart 3.9](https://medium.com/dartlang/announcing-dart-3-9-ba49e8f38298)

현재는 패치 업데이트가 두 번 진행되어 **Flutter 3.35.2** 버전까지 출시된 상태입니다.

* [CHANGELOG.md](https://github.com/flutter/flutter/blob/master/CHANGELOG.md)

## 🚀 Flutter 3.35 주요 업데이트 하이라이트

* **Dart & Flutter MCP Server 안정 버전 출시**: AI 어시스턴트(Cursor, GitHub Copilot 등)가 프로젝트를 깊이 이해하고 자동으로 오류 수정, 의존성 관리, 코드 생성 수행
* **Widget Previews (실험적)**: 전체 앱 실행 없이 위젯을 독립된 환경에서 미리보기 및 테스트
* **Stateful Hot Reload 기본 활성화**: 웹에서 실험적 플래그 없이 상태 유지 핫 리로드 사용 가능
* **Material & Cupertino 라이브러리 분리**: 핵심 프레임워크에서 독립 패키지로 분리하여 더 빠른 업데이트 주기 및 커뮤니티 기여 활성화
* **Deprecation & Breaking changes**
    * 32비트 x86 아키텍처 중단 예정
    * Flutter 3.13 이전 버전 IDE 지원 중단
    * Android: 최소 SDK API 24 (Android 7\)

## 🚀 Flutter 3.35.1 변경사항

* flutter/173785 \- flutter.dev에서 Windows용 Flutter SDK 다운로드를 방해했던 문제를 수정합니다.

## 🚀 Flutter 3.35.2 변경사항

* flutter/173823 \- flutter.minSdkVersion을 사용하지 않고 Kotlin 빌드 파일에서 24보다 낮은 값을 사용하는 Android 빌드에서, Flutter의 자동 마이그레이션이 Kotlin 구문으로 값을 올바르게 업데이트합니다.
* flutter/173741 \- (웹) 스크린 리더가 키보드 단축키를 통해 버튼을 누르지 못하게 하는 문제를 수정합니다.
* flutter/173960 \- Chrome 또는 Edge가 설치되지 않은 경우 위젯 미리보기가 시작되지 않는 문제를 수정합니다.
* flutter/174017 \- 64비트 Windows 시스템에서 32비트 프로세스를 실행할 때 발생하는 문제를 수정합니다.
* flutter/173895 \- Windows에서 directory watcher(디렉토리 감시자)가 다시 시작될 때 위젯 미리보기가 충돌하지 않도록 합니다.
* flutter/171992 \- exynos9820 칩이 Impeller Vulkan 백엔드를 사용하지 못하도록 차단합니다.
* flutter/173959 \- 유효하지 않은 노드에 @Preview()를 추가하려고 할 때 발생하는 null 어설션 오류를 수정합니다.
* flutter/174184 \- 드라이 런이 비활성화되고 \--wasm이 지정되지 않은 경우 WASM 빌드가 잘못 트리거되는 문제를 수정합니다.
* flutter/171758 \- 기존 Dart 개발 서비스가 있는 기기에서 flutter run을 실행할 때 발생할 수 있는 ExistingDartDevelopmentServiceException 오류를 수정합니다.

# Flutter Seoul 행사 소식

**APAC 지역 Flutter 개발자를 위한 글로벌 컨퍼런스가 올해 처음으로 서울에서 개최됩니다**.  
올해는 Flutter Meetup Network의 Flutter Seoul, Flutter Tokyo, Flutter Taipei 커뮤니티가 함께하고 있습니다\!. 해외 플러터 개발자와 연사를 만날 수 있는 기회를 놓치지 마세요.   
많은 관심과 참여 부탁드립니다.

## Flutter Alliance 2025

* 티켓 구매 링크: **[Flutter Alliance 2025 | 티켓타코](https://www.ticketa.co/events/27)**
* 일자: 2025년 10월 19일 (일) 10시 30분 \- 17시 00분
* 장소: [한국마이크로소프트 13층](https://maps.app.goo.gl/99p5Nn4TfNWp8azF7) (서울특별시 종로구 중학동 종로1길 50\)
* 주관: Flutter Seoul, Flutter Taipei, Flutter Tokyo

# 한국 Flutter 행사 소식

## 2025 I/O Extended Seoul

2025년 8월 9일(토) 서울 성수에서 열리는 2025 I/O Extended Seoul 행사에 Flutter Seoul 운영진 박제창님이 Flutter로 Gemini와 MCP를 활용한 Agentic App 만들기 주제로 핸즈온 세션을 진행했습니다. 참석해주신분들 감사드립니다.  
발표자료 링크: [https://speakerdeck.com/itsmedreamwalker/o-extended-seoul](https://speakerdeck.com/itsmedreamwalker/o-extended-seoul)

## 2025 I/O Extended Busan

2025년 9월 6일(토) 부산 국립부경대학교 컨벤션홀에서 열리는 2025 I/O Extended Busan 행사에 Flutter Seoul 운영진 박제창님이 Flutter with Dart MCP: All You Need 주제로 테크톡 세션을 진행할 예정입니다. 관심있는 분들은 많은 참석 부탁드립니다.  
이벤트 링크: [https://event-us.kr/gdgbusan/event/110303](https://event-us.kr/gdgbusan/event/110303)

# Flutter 관련 오픈소스

## [flutter\_nnnoiseless](https://pub.dev/packages/flutter_nnnoiseless)

순환 신경망(RNN) 기반의 고성능 노이즈 감소 기술을 Flutter에서 바로 사용할 수 있는 flutter\_nnnoiseless 패키지가 출시되었습니다. 이 패키지는 Rust로 개발된 nnnoiseless 프로젝트를 Flutter Rust Bridge를 통해 포팅한 것으로, 실시간 스트림 처리와 파일 기반 배치 처리 모두를 지원합니다.

## [draft](https://pub.dev/packages/draft)

**Draft는 JavaScript의 Immer를 Dart로 포팅한 라이브러리입니다.**

어떤 객체든 수정 가능한 draft로 변환하고, 수정한 후 다시 불변 버전으로 되돌려주는 편리한 API를 제공합니다.

```dart
import 'package:draft/draft.dart';

part 'example.draft.dart';

@draft 
class Foo { 
  final int value; 
  const Foo(this.value); 
} 
// Foo는 불변이지만 Draft로 편집 가능
Foo foo = Foo(1).produce((draft) { draft.value += 1; }); // 2 출력* print(foo.value);
```


---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)
