# Flutter Seoul Newsletter 20호


안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다. 

7월 마지막 주입니다\! 연일 계속되는 폭염에 지치셨을 텐데도 여전히 플러터 개발에 열정을 쏟고 계신 개발자분들을 보면 존경스러운 마음이 듭니다.

본격적인 휴가철이지만 플러터 생태계는 쉬지 않고 발전하고 있어서, 이번에도 놓치기 아까운 소식들을 담아봤습니다다. 시원한 실내에서 편안한 마음으로 천천히 읽어보시길 바랍니다다\!

이번 호에서는 다음과 같은 내용을 다룹니다.

* **Flutter 3.32 업데이트 소식**
* **한국 Flutter 행사 소식**
* **Flutter 관련 영상 소식**  
* **Flutter 패키지 소식**

# Flutter 3.32.x 업데이트 소식

지난 달 Flutter 3.32.5 버전이 배포된 이후 세 차례의 패치 업데이트가 있었습니다.

7월 10일 Flutter 3.32.6

* [flutter/171106](https://github.com/flutter/flutter/pull/171106) \- 스크롤 뷰가 모든 플랫폼에서 LayoutBuilder를 포함할 때 null 검사 충돌을 방지합니다.  
* [flutter/171239](https://github.com/flutter/flutter/pull/171239) \- Impeller \+ Vulkan을 사용하고 Android에서 Flutter를 사용하는 액티비티 간 전환 시 충돌을 방지합니다.  
* [flutter/171737](https://github.com/flutter/flutter/pull/171737) \- Android SDK 10-13 (API 29-33)에서 플랫폼 뷰를 사용할 때 앱을 백그라운드로 보낸 후 포그라운드로 복귀 시 앱 충돌을 방지합니다


7월 17일 Flutter 3.32.7

* [flutter/172121](https://github.com/flutter/flutter/pull/172121) \- 백그라운드에서 복귀할 때 iOS 이미지가 분홍색 채우기로 대체되는 문제를 수정했습니다.

7월 26일 Flutter 3.32.8

* [flutter/150131](https://github.com/flutter/flutter/issues/150131) \- macOS 15의 iOS 사용자들이 권한이 누락된 경우 도구 충돌을 볼 수 있습니다. mDNS 권한을 활성화하여 해결할 수 있습니다.  
* [flutter/155294](https://github.com/flutter/flutter/issues/155294), [flutter/169506](https://github.com/flutter/flutter/issues/169506) \- Android에서 이전에 반환된 것과 다른 새로운 표면을 임베더에 요청하는 새로운 API를 추가했습니다.  
* [flutter/172602](https://github.com/flutter/flutter/pull/172602) \- macOS 10.15 이전 버전에서 macOS 10.15에 도입된 hasUnifiedMemory를 호출하지 않도록 했습니다.  
* [flutter/172250](https://github.com/flutter/flutter/issues/172250) \- iOS에서 `TextInput.hide` 호출이 활성 텍스트 필드의 텍스트를 잘못 지우는 문제를 수정했습니다.

전체 [CHANGEDLOG.md](https://github.com/flutter/flutter/blob/master/CHANGELOG.md) 보러가기

# 한국 Flutter 행사 소식

## Google I/O Extended Incheon

2025년 7월 26일 Flutter Seoul 운영진 박제창님이 Google I/O Extended Incheon에서 How to build Agentic Apps with Flutter 핸즈온 세션을 진행했습니다.  
핸즈온 세션에서 진행했던 자료는 아래의 링크에서 확인해 볼 수 있습니다.   
[https://speakerdeck.com/itsmedreamwalker/hands-on-how-to-build-agentic-apps-with-flutter-at-bagjecang](https://speakerdeck.com/itsmedreamwalker/hands-on-how-to-build-agentic-apps-with-flutter-at-bagjecang)

## 2025 I/O Extended Seoul

2025년 8월 9일(토) 서울 성수에서 열리는 2025 I/O Extended Seoul 행사에 Flutter Seoul 운영진 박제창님이 Flutter로 Gemini와 MCP를 활용한 Agentic App 만들기 주제로 핸즈온 세션을 진행할 예정입니다. 관심있는 분들은 많은 참석 부탁드립니다.   
https://event-us.kr/gdgseoul/event/108328

# Flutter 영상 돌아보기

## StringBuffer (Technique of the Week)

[StringBuffer (Technique of the Week)](https://youtu.be/xSsFtDY-nOw?si=FTm8IzdLi-JmGRCP)

이 영상에서는 Dart의 문자열 처리와 관련된 흔한 오해를 해소하고, StringBuffer 를 활용하여 코드를 최적화하는 방법을 소개합니다.

## Build and ship amazing multiplatform iOS and Android apps with one codebase

[Build and ship amazing multiplatform iOS and Android apps with one codebase](https://youtu.be/W4JWeQolJsU?si=wIG0dPJ86kZoMO0K)

Flutter가 어떻게 iOS 및 Android 앱을 위한 단일 코드베이스를 사용하여 뛰어나고 다중 플랫폼의 모바일 앱을 구축하고 배포하는 데 사용될 수 있는지 설명합니다. 이 동영상은 Flutter가 효율적이고 개방형 개발 스택이며 고품질의 생산 등급 앱을 iOS, Android 및 웹에서 원활하게 실행할 수 있도록 하는 핵심 기능을 보여줍니다.

## YouTube stream watcher, part 3 | Observable Flutter \#66

[https://www.youtube.com/live/pK2itkQgMfc?si=sTQ2B8mX5kl4S8Af](https://www.youtube.com/live/pK2itkQgMfc?si=sTQ2B8mX5kl4S8Af)  
진행자 Craig Lens는 라이브 스트림 댓글을 표시하는 도구를 만들려는 Flutter 앱 프로젝트를 진행합니다. 이 에피소드에서는 API 키 처리, UI 조정, 앱 구조 개선에 중점을 둡니다.

## Vibe-coding with Gemini CLI | Observable Flutter \#67

[https://www.youtube.com/live/EsklFa3nkwA?si=yZErZ6v1dTH-DjyK](https://www.youtube.com/live/EsklFa3nkwA?si=yZErZ6v1dTH-DjyK)

진행자 Craig Levens는 Randall Schwarz와 함께 Gemini CLI를 사용하여 Flutter 앱을 개발하는 과정을 보여줍니다. Randall은 인공지능 도구인 Gemini CLI를 통해 Product Requirement Document (PRD)를 만들고, 테스트가 가능한 증분 단계를 계획하며, 코드를 작성하고, 버그를 수정하는 등 소프트웨어 엔지니어링의 표준 방식을 따르는 과정을 시연합니다.

# Flutter 패키지 소식

## dicom\_parser

[dicom\_parser | Flutter package](https://pub.dev/packages/dicom_parser)

`dicom_parser`는 Flutter(Dart) 환경에서 DICOM 의료 영상을 파싱하고 렌더링하기 위한 순수 Dart 기반 패키지입니다. 네이티브 C/C++ 라이브러리에 의존하지 않고 모바일, 웹, 데스크톱 플랫폼에서 모두 동작합니다.

### 주요 특징

**🔧 순수 Dart 구현**: 네이티브 종속성이 전혀 없는 100% Dart로 구현되어 있어, 별도의 네이티브 라이브러리 설치나 플랫폼별 설정이 필요하지 않습니다.

**🌐 완전한 크로스 플랫폼 지원**: Android, iOS, Web, macOS, Linux, Windows 등 Flutter가 지원하는 모든 플랫폼에서 동일하게 작동합니다.

**📂 DICOM 파일 파싱**: 표준 DICOM 파일 형식을 완전히 지원하여 의료 영상 데이터와 메타데이터를 추출할 수 있습니다.

**🔄 다양한 Transfer Syntax 지원**: 다양한 DICOM Transfer Syntax를 지원하여 압축된 이미지와 비압축 이미지 모두 처리할 수 있습니다.

**🎨 다중 Photometric Interpretation 지원**: 그레이스케일, RGB, YBR 등 다양한 색상 해석 방식을 지원합니다.

## flutter\_keyframe\_timeline

[flutter\_keyframe\_timeline | Flutter package](https://pub.dev/packages/flutter_keyframe_timeline)

`flutter_keyframe_timeline`은 Flutter에서 키프레임 기반 애니메이션을 구현하기 위한 전문적인 패키지입니다. 비디오 편집, 2D/3D 애니메이션, 복잡한 UI 애니메이션 등에 활용할 수 있는 타임라인 애니메이션 시스템을 제공합니다.
s

## chat\_bottom\_container 

[chat\_bottom\_container | Flutter package](https://pub.dev/packages/chat_bottom_container)  
`chat_bottom_container`는 채팅 애플리케이션의 하단 영역을 효과적으로 관리하기 위한 Flutter 패키지입니다.

## dartantic\_ai

[https://pub.dev/packages/dartantic\_ai](https://pub.dev/packages/dartantic_ai)  
Dartantic.ai는 Dart 언어를 사용하여 생성형 AI 기반의 클라이언트 및 서버 앱을 더 쉽고 재미있게 구축할 수 있도록 설계된 에이전트 프레임워크입니다. 이 패키지는 개발자가 여러 단계의 문제를 해결하기 위해 AI 에이전트가 자율적으로 도구를 연결하여 사용하도록 하는 등 다양한 기능을 제공합니다.

주요 특징:

* **자율적인 문제 해결:** AI 에이전트가 사람의 개입 없이도 여러 단계의 문제를 해결하기 위해 다양한 도구 호출을 스스로 연결하고 활용합니다.
* **광범위한 공급자 지원:** OpenAI, Google, Anthropic, Mistral, Cohere, Ollama 등 여러 AI 공급자를 별도의 설정 없이 즉시 사용할 수 있습니다.
* **실시간 응답:** 스트리밍 출력을 지원하여 사용자에게 실시간으로 응답을 제공합니다.
* **정확한 출력 및 도구 호출:** Dart의 타입 시스템과 JSON 직렬화를 활용하여 타입이 명확히 지정된 출력 및 도구 호출이 가능합니다.
* **다양한 입력 처리:** 텍스트, 이미지, 파일 등 다양한 형식의 멀티미디어 입력을 처리할 수 있습니다.
* **시맨틱 검색 기능:** 벡터 생성 및 시맨틱 검색 기능을 통해 관련성 높은 정보를 찾아냅니다.
* **MCP 지원:** 모델 컨텍스트 프로토콜(MCP) 서버와 통합하여 원활하게 작동합니다.
* **유연한 공급자 전환:** 대화 중에도 AI 공급자를 손쉽게 변경할 수 있습니다.
* **안정적인 운영 환경:** 로깅, 오류 처리, 재시도 처리 기능이 내장되어 있어 프로덕션 환경에서도 안정적인 사용이 가능합니다.
* **뛰어난 확장성:** 사용자 정의 공급자 및 도구를 쉽게 추가하여 기능을 확장할 수 있습니다.
---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)