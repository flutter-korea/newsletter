# **25/06 뉴스레터**

안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다.

6월의 마지막 주, 무더위 속에서도 플러터와 함께 열정적으로 코딩하고 계실 구독자님을 위해 새로운 소식을 가지고 찾아왔습니다. 이번 호에서는 다음과 같은 내용을 다룹니다.

WWDC 25에서 발표된 새로운 소식으로 기술 커뮤니티가 뜨겁습니다. 특히 이번에 공개된 '리퀴드 글래스(Liquid Glass)' 디자인 시스템은 visionOS의 영향을 받아 더욱 깊이 있고 생동감 넘치는 사용자 경험을 제공할 것으로 기대되는데요, 오늘은 이 '리퀴드 글래스'가 무엇이며, 우리 플러터(Flutter) 개발자들은 어떻게 활용할 수 있을지에 대한 이야기를 나누어 볼까 합니다.

* **Flutter 3.32 업데이트 소식**
* **Flutter 관련 영상 소식**
* **Flutter 패키지 소식**
* **Flutter 오픈소스 프로젝트 관련 소식**

# Flutter 3.32.x 업데이트 소식

지난 달 Flutter 3.32.0이 배포된 이후 4 차례의 패치 업데이트가 있었습니다.

### 6월 5일 Flutter 3.32.2

* [flutter/169772](https://github.com/flutter/flutter/pull/169772) \- Flutter CI가 별도 요구사항이 없을 때 Windows 대신 Linux에서 테스트를 실행하도록 구성 변경
* [flutter/169630](https://github.com/flutter/flutter/pull/169630) \- Windows에서 flavored Android 패키지가 다음 clean까지 반복적으로 빌드에 실패할 수 있는 문제 수정
* [flutter/169912](https://github.com/flutter/flutter/pull/169912) \- API 문서 게시를 위한 Flutter CI 작업을 빌드 단계와 배포 단계로 분리

### 6월 12일 Flutter 3.32.3

* [flutter/170052](https://github.com/flutter/flutter/pull/170052) \- NavigationDrawer 의 NavigationBar "active" 표시기 수정
* [flutter/170013](https://github.com/flutter/flutter/pull/170013) \- Impeller Vulkan 백엔드의 메모리 누수 수정
* [flutter/169912](https://github.com/flutter/flutter/pull/170003) \- 릴리스 모드에서 Android AAB 빌드 실패 문제 수정

### 6월 13일 Flutter 3.32.4

* [flutter/170536](https://github.com/flutter/flutter/issues/170536) \- dart 도구 실행 시 Mac 호스트에서 발생하는 코드 서명 문제 수정

### 6월 26일 Flutter 3.32.5

* [flutter/170924](https://github.com/flutter/flutter/pull/170924) \- Intel 그래픽 카드와 같이 OpenGL ES 2만 지원하는 컴퓨터에서 Flutter Windows 수정
* [flutter/170880](https://github.com/flutter/flutter/pull/170880) \- IDE에서 사용하는 디버그 어댑터의 애플리케이션 종료 시 처리되지 않은 예외 수정
* [flutter/170846](https://github.com/flutter/flutter/pull/170846) \- 앱이 백그라운드 상태일 때 푸시 알림이 이미지 디코딩을 트리거하면 발생할 수 있는 iOS 이미지 디코드 오류 수정.
* [flutter/171034](https://github.com/flutter/flutter/pull/171034) \- 개발 의존성 누락으로 인해 iOS/macOS 워크플로우가 예상대로 동작하지 않을 수 있는 문제 수정

전체 [CHANGEDLOG.md](https://github.com/flutter/flutter/blob/fcf2c11572af6f390246c056bc905eca609533a0/CHANGELOG.md) 보러가기

# Flutter 영상 돌아보기

6월 한달간 어떤 영상들이 있었는지 같이 돌아보시죠.

## CupertinoRadio (Widget of the Week)

[https://youtu.be/D0xwcz2IqAY?feature=shared](https://youtu.be/D0xwcz2IqAY?feature=shared)

이 영상은 iOS 스타일의 UI를 구현하는 데 유용한 Flutter 위젯인 CupertinoRadio에 대해 소개합니다. CupertinoRadio는 여러 개의 상호 배타적인 옵션 중에서 하나를 선택할 수 있도록 해주며, enum을 사용하여 옵션들을 정의하는 것이 일반적입니다. 라디오 버튼 그룹은 공통의 group value를 공유하여 현재 선택된 라디오 버튼을 추적합니다. 또한, active color, inactive color, Inner Circle fill color와 같은 다양한 스타일을 설정할 수 있으며, CupertinoListTile과 함께 사용하여 라벨을 추가할 수도 있습니다. 이 위젯을 통해 iOS 사용자에게 익숙한 인터페이스를 제공할 수 있습니다.

## dart:convert (Technique of the Week)

[https://youtu.be/ngsxzZt5DoY?feature=shared](https://youtu.be/ngsxzZt5DoY?feature=shared)

## Dart Code Metrics | Observable Flutter \#63

[https://www.youtube.com/live/ftPD7jTTsjg?feature=shared](https://www.youtube.com/live/ftPD7jTTsjg?feature=shared)

이 영상은 dart code metrics (dcm)라는 Dart 및 Flutter 코드의 정적 분석 도구에 대한 소개와 사용법을 다루고 있습니다. dcm은 기본적인 린트 규칙 외에도 코드 메트릭, 리팩토링 명령어, 대시보드 등 다양한 기능을 제공하여 코드 품질 향상과 기술 부채 관리에 도움을 줍니다. 특히 미사용 코드 제거, 코드 중복 탐지, 위젯 구조 분석 등 개발 생산성과 코드 유지보수성을 높이는 데 유용한 기능들을 시연하며 dcm의 실용적인 가치를 강조합니다.

## Tricksy Projectses | Observable Flutter \#64

[https://www.youtube.com/live/K-duxcUpUrQ?feature=shared](https://www.youtube.com/live/K-duxcUpUrQ?feature=shared)

## Just Coding | Observable Flutter \#65

[https://www.youtube.com/live/cz8Z2DT7SMw?feature=shared](https://www.youtube.com/live/cz8Z2DT7SMw?feature=shared)

# Flutter 패키지 소식

## liquid\_glass\_renderer

[https://pub.dev/packages/liquid\_glass\_renderer](https://pub.dev/packages/liquid_glass_renderer#glassify-glass-effect-on-any-shape-experimental)

### **리퀴드 글래스(Liquid Glass)란?**

Apple은 **WWDC 2025**에서 "Liquid Glass"라는 새로운 소프트웨어 디자인을 공식 발표했습니다.

리퀴드 글래스는 현대 UI/UX 디자인에서 인기를 끌고 있는 **글래스모피즘(Glassmorphism)** 디자인 트렌드의 한 형태입니다. 반투명한 유리 표면처럼 보이면서 뒤의 배경을 굴절시키고, 여러 유리 요소들이 마치 액체처럼 자연스럽게 혼합되는 시각적 효과를 말합니다.

이 효과는 **깊이감과 투명도**를 통해 모던하고 세련된 느낌을 주며, Apple의 iOS나 macOS에서 볼 수 있는 블러 효과와 유사하지만 더욱 동적이고 상호작용적인 특징을 가집니다.

### **패키지 주요 특징**

*  **독립적인 유리 위젯**: 모든 위젯을 감싸서 유리 효과 적용

*  **블렌딩 레이어**: 여러 유리 모양이 액체처럼 자연스럽게 혼합

*  **고도로 커스터마이징 가능**: 두께, 색상, 조명, 굴절 등 세밀한 조정

*  **배경 블러 효과**: 배경 흐림 및 굴절 효과

*  **뛰어난 성능**: Flutter의 셰이더 지원 기반으로 최적화

### **현재 제한사항**

⚠️ **프리릴리즈 버전**으로 Impeller 엔진에서만 동작하여 Web, Windows, Linux는 지원되지 않으며, 최대 3개 모양까지만 블렌딩 가능합니다.

이 패키지는 특히 **프리미엄 UI/UX**를 구현하고자 하는 개발자들에게 매우 유용할 것으로 보이며, 향후 안정화되면 Flutter 앱의 시각적 품질을 크게 향상시킬 수 있는 도구가 될 것 같습니다.

## liquido

[https://github.com/renancaraujo/liquido](https://github.com/renancaraujo/liquido)

**⚠️ 실험적 버전 \- 기술 시연용으로만 사용하세요.**
이 패키지는 매우 실험적인 버전이며, 프로덕션(상용) 환경에서의 사용을 목적으로 하지 않습니다. 성능을 고려하여 제작되지 않았으므로 기술 시연 목적으로만 간주해야 합니다. 사용에 따르는 책임은 사용자 본인에게 있습니다.

**⚠️ 임펠러(IMPELLER) 전용**  
이 패키지는 플러터의 임펠러 렌더링 엔진과만 호환됩니다. 스키아(Skia) 백엔드에서는 작동하지 않습니다.

## vault\_storage

Flutter의 복잡한 스토리지 상황을 해결하기 위해 만들어진 통합 보안 스토리지 솔루션입니다. flutter\_secure\_storage로 마스터 암호화 키를 보호하고, 민감한 데이터를 위한 암호화된 Hive 박스, 파일을 위한 AES-GCM 암호화를 활용한 강력한 보안을 제공합니다.

암호화 작업은 UI 끊김을 방지하기 위해 백그라운드 isolate에서 compute를 사용하여 실행되는 고성능 구조를 갖추고 있으며, fpdart의 Either와 TaskEither를 활용한 명시적이고 함수형 스타일의 오류 관리로 타입 안전성을 보장합니다.

[https://pub.dev/packages/vault\_storage](https://pub.dev/packages/vault_storage)

미디움 기사: [I Was Tired of Flutter’s Storage Mess, So I Built a Solution](https://medium.com/@abdulgafoorabid/i-was-tired-of-flutters-storage-mess-so-i-built-a-solution-0fb5a16a2013)

## gemini\_live

[https://pub.dev/packages/gemini\_live](https://pub.dev/packages/gemini_live)  
Google의 Gemini 모델과 실시간, 멀티모달 대화를 가능하게 해주는 실험적인 Gemini Live API를 사용하기 위한 Flutter 패키지입니다. 이 패키지는 Firebase / Firebase AI Logic 사용 없이 활용가능 합니다. 그리고 gemini-2.0-flash-live-001 모델을 지원합니다.

# Flutter 오픈 소스

# Where is My Train

인도에서 수백만 명이 사용하는 활용도 높은 앱을 클론코딩하여 UI를 구현했다고 합니다.

### **🛠️ 기술 스택**

* 프런트엔드를 위한 **플러터**
* **다트** 언어

깃허브 링크: [https://github.com/AnshMNSoni/Where-is-my-Train-Clone](https://github.com/AnshMNSoni/Where-is-my-Train-Clone)

Sara Baby Tracker & Sounds

**Sara**는 부모와 보호자들의 육아를 돕기 위해 Flutter로 개발된 **오픈소스 크로스플랫폼 육아 추적 앱**입니다. 실시간 로깅, 다중 보호자 지원, 수면 사운드, 그리고 이유식 레시피까지 제공하는 **올인원 육아 솔루션**입니다.

### **🛠️ 기술 스택**

### **프론트엔드**

* **Flutter 3.x**: 크로스플랫폼 UI 개발
* **flutter\_bloc**: 상태 관리
* **Custom AppRouter**: 내비게이션 관리

### **백엔드 & 데이터베이스**

* **Firebase Auth**: 사용자 인증 (이메일/비밀번호)
* **Cloud Firestore**: 활동, 아기, 보호자 데이터 저장
* **Firebase Storage**: 아기 아바타 이미지 저장
* **SQLite**: 오프라인 캐싱 및 로컬 접근
* **SharedPreferences**: 로컬 설정 저장

### **특별 기능**

* **커스텀 백그라운드 사운드 플레이어**: 루프 및 페이드 기능
* **로컬 이미지 피커**: 아기 아바타 선택

깃허브 링크: [https://github.com/suleymansurucu/flutter\_sara\_baby\_tracker\_and\_sounds](https://github.com/suleymansurucu/flutter_sara_baby_tracker_and_sounds)  
PlayStore 링크: [https://play.google.com/store/apps/details?id=com.suleymansurucu.sarababy](https://play.google.com/store/apps/details?id=com.suleymansurucu.sarababy)  
AppStore 링크: [https://apps.apple.com/us/app/sara-baby-tracker-sounds/id6746516938](https://apps.apple.com/us/app/sara-baby-tracker-sounds/id6746516938)

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)