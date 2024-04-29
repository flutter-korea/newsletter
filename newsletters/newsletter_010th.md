# Flutter Seoul Newsletter 10호

Flutter Seoul Newsletter 10호를 확인해주셔서 감사합니다.

플러터 서울 커뮤니티의 홍종표(HDD)와 박제창(Dreamwalker)입니다.

추운 겨울이 이제 끝나가고 있으며, 따뜻한 봄의 시작이 가까워졌습니다. 다가올 환절기 감기 조심하시고, 즐거운 3월 되시면 좋겠습니다. 

2월에는 플러터 관련 새로운 소식들이 많습니다. 짧은 시간을 투자해서 많은 정보를 얻어가실 수 있도록 요약해서 전달드리겠습니다.

이번 호에서는 다음과 같은 내용을 다룹니다.

- Flutter 3.19, Dart 3.3 업데이트 소식
- Flutter 2024 Roadmap
- Google Generative Dart SDK
- Flutter 개발자 커뮤니티 관련 소식

---

# 1. Flutter, Dart 업데이트 소식

2월 16일에 Flutter 3.19와 Dart 3.3 버전이 출시되었습니다.

## 🎯 Dart 3.3

**extension types** 라는 새로운 확장 타입 기능이 새로 추가되었습니다.

해당 기능은 코스트 없는 Wrapping을 가능하게 해주며 그로인해 호스트 플랫폼과 상호 운영할 때 성능에 민감한 코드를 최적화할 때 사용할 수 있습니다.

그로 인해 JS Interop 도 많은 발전을 가져오게 되었으며, 브라우저 라이브러리를 개선할 수 있게 되었습니다.

이 모든 것은 Dart를 웹 어셈블리로 컴파일하는 과정으로 이어집니다.

또한 Google 에서는 최신 AI 모델인 Gemini를 이용하여 Flutter 와 Dart에서 생성형 AI를 사용할 수 있도록 [package:google_generative_ai](https://pub.dev/packages/google_generative_ai) 를 베타버전으로도 출시했습니다.

이 내용들이 더 궁금하다면, Flutter 혹은 Flutter Seoul 미디움의 게시글을 확인해주세요!

👉  [What’s new in Dart 3.3 (원문)](https://medium.com/dartlang/dart-3-3-325bf2bf6c13) 

👉  [What’s new in Dart 3.3 (한글 번역)](https://medium.com/flutter-korea/whats-new-in-dart-3-3-2ce4dc246642) 

## 🐦 Flutter 3.19

Flutter 3.19 stable 버전이 출시되었습니다. 

요약해보면 아래와 같습니다. 많은 개선 및 변경사항이 있었는데요. 아무래도 이번에는 Google Generative ai Gemini를 쉽게 사용할 수 있도록 되어 눈여겨볼 포인트 같습니다. 

- **Gemini 지원:** Google AI의 최신 AI 모델을 사용하여 Flutter 앱에 생성 AI 기능을 구축하는 새로운 Dart SDK입니다.
- **스크롤 개선:** 손가락 개수와 상관없이 스크롤 동작을 제어하는 기능을 포함하여 다양한 스크롤 개선 사항과 버그 수정.
- **Adaptive Switch:** 다양한 플랫폼에서 기본적인 느낌과 모양을 가진 새로운 스위치 구성 요소.
- **Impeller 엔진 진행 상황:** 성능 향상 및 Skia와의 기능 동등성, Android OpenGL 장치에서 MSAA 지원 포함.
- **Flutter iOS 기본 글꼴:** Apple 디자인 지침에 따라 iOS에서 글꼴 렌더링 개선.
- **Windows Arm64 지원:** Windows Arm64 장치에서 Flutter 앱을 실행하는 초기 지원.

👉 [What’s new in Flutter 3.19 (원문)](https://medium.com/flutter/whats-new-in-flutter-3-19-58b1aae242d2)

👉 [What’s new in Flutter 3.19 (한글 번역)](https://medium.com/flutter-korea/whats-new-in-flutter-3-19-898b217d4f5e)

추가적으로 2월 29일에 Flutter **3.19.2** 버전이 출시 되었습니다.

수정 내용은 Flutter Web에서 `--flavor` 가 정상적으로 되지 않았던 것 같습니다.

👉 [Hotfixes to the Stable Channel](https://github.com/flutter/flutter/wiki/Hotfixes-to-the-Stable-Channel)

# 2. Gemini Dart SDK 공개

한국 시간으로 2월 16일 (목) 새벽 2시에 Flutter Youtube의 Observable<Flutter> 을 통해

생성형 AI Dart SDK가 공개되었습니다.

해당 유튜브 영상 이외에도 블로그 글, 퀵스타트 가이드 등 참고 자료들이 많이 올라왔으니 관심있으신 분들은 따라해보셔도 즐거운 경험이 되실 것 같습니다. 🙂

📺  [Youtube 링크](https://www.youtube.com/live/sojm449IB-4?si=ydTeDplSNLOvy6zo)

📦  [google_generative_ai 패키지](https://pub.dev/packages/google_generative_ai)

👉  **[Harness the Gemini API in your Dart and Flutter Apps](https://medium.com/flutter/harness-gemini-in-your-dart-and-flutter-apps-00573e560381)**

👉  [QuickStart](https://ai.google.dev/tutorials/dart_quickstart?hl=ko) 

  

# 3. Flutter 2024 Roadmap

매년 Flutter 팀은 한 해의 로드맵을 공유하며, 이를 통해 Flutter 팀의 우선 순위를 볼 수 있고 진행중인 작업을 바탕으로 계획을 세울 수 있도록 합니다.

작성된 목록이 전체 목록으로 간주되거나, 무조건 지키겠다는 약속으로 보아서는 안되며 로드맵에 대해 피드백이 있다면 이슈를 제기하거나 이슈에 이모지 반응을 사용하는 것으로 연락을 취할 수 있습니다.

제게 흥미로웠던 몇가지를 추려보면 아래와 같습니다: 

- **Impeller**
- **Material 3**
- **Swift Package Manager** **지원**
- **SEO 관련 조사**
- **Dart 언어의 새로운 기능들**
- **Non-goals: Code Push**

해당 내용은 Flutter Seoul의 nine님께서 번역해주셨습니다. (감사합니다! 🙇‍♂️) 

👉  [Roadmap](https://github.com/flutter/flutter/wiki/Roadmap)

👉  [Flutter’s 2024 로드맵 공유](https://medium.com/flutter-korea/flutters-2024-%EB%A1%9C%EB%93%9C%EB%A7%B5-%EA%B3%B5%EC%9C%A0-48c09a8b98a6)

# 4. Custom Lint  -- fix 기능 추가

Flutter의 가장 인기있는 상태관리 중 하나인 riverpod 을 사용하시는 분들이라면 생각보다 많이 익숙한 패키지인 custom_lint 패키지에 새로운 멋진 기능들이 추가되었습니다.

`--fix` 기능 입니다.

기존에는 직접 `alt` + `enter` 를 통해서 수정해야했다면 이제는 터미널에 `custom_lint --fix` 명령어를 통해 일괄적으로 수정이 가능하게 되었습니다.

Lint에 관심이 많으셨던 분이라면 이 기회에 좋은 린트를 만들어보시는건 어떨까요?

📦 [custom_lint 패키지](https://pub.dev/packages/custom_lint)

# 5. Flutter Seoul 미디엄 글

Flutter Seoul의 Medium에 새로운 글이 등록되었습니다.  

👉  [What’s new in Dart 3.3 (한글 번역)](https://medium.com/flutter-korea/whats-new-in-dart-3-3-2ce4dc246642) 

👉 [What’s new in Flutter 3.19 (한글 번역)](https://medium.com/flutter-korea/whats-new-in-flutter-3-19-898b217d4f5e)

👉  [Flutter’s 2024 로드맵 공유](https://medium.com/flutter-korea/flutters-2024-%EB%A1%9C%EB%93%9C%EB%A7%B5-%EA%B3%B5%EC%9C%A0-48c09a8b98a6)

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)