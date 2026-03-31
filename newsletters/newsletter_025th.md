# **Flutter Seoul Newsletter 25호 (2026년 3월호)**

안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다.

어느덧 봄기운이 완연한 3월입니다. 꽃샘추위가 아직 남아있지만, 플러터 생태계에는 이미 따뜻한 봄바람이 불고 있습니다. 이번 달은 특히 **AI와 Flutter의 결합**이 본격적으로 꽃을 피운 시기라 할 수 있는데요, Google이 공개한 에이전틱 IDE인 Antigravity부터 Dart 전용 AI 프레임워크 Genkit Dart까지, Flutter 개발자가 AI 시대를 맞이하는 방식이 크게 달라지고 있습니다.

그럼 뉴스레터 2026년 3월호 시작합니다.

이번 호에서는 다음과 같은 내용을 다룹니다.

* **Flutter 3.41 패치 업데이트 소식**
* **Genkit Dart: 풀스택 AI 앱을 Dart로**
* **Google Antigravity로 20일 만에 20개 앱 만들기**
* **Flutter 행사 소식**
* **Flutter 패키지 소식**
* **Flutter 오픈소스 소개**

# **Flutter 3.41 패치 업데이트 소식**

2월에 릴리스된 Flutter 3.41 이후 세 차례의 패치 업데이트가 있었습니다.

### Flutter 3.41.4

* [flutter/182748](https://github.com/flutter/flutter/issues/182748) - Xcode 26에서 CocoaPod 의존성이 arm 지원을 제공하지 않을 때 iOS 시뮬레이터 빌드가 실패하는 문제를 수정했습니다.
* [flutter/182361](https://github.com/flutter/flutter/issues/182361) - iOS 플러그인 라이프사이클 이벤트에서 발생하는 충돌을 수정했습니다.
* [flutter/182367](https://github.com/flutter/flutter/issues/182367) - Flutter Web Skwasm 앱의 충돌 문제를 수정했습니다.
* [flutter/183071](https://github.com/flutter/flutter/issues/183071) - Test 패키지 및 관련 의존성이 업데이트되었습니다.

### Flutter 3.41.5

* [flutter/182708](https://github.com/flutter/flutter/issues/182708) - Impeller 사용 시 원(circle)을 렌더링할 때 45도 각도에서 블러 아티팩트가 나타나는 문제를 수정했습니다.

### Flutter 3.41.6

* [flutter/184025](https://github.com/flutter/flutter/pull/184025) - Skia 아틀라스에서 글리프 마스크 포맷에 맞는 올바른 아틀라스가 일관되게 사용되도록 수정했습니다.
* [flutter/182708](https://github.com/flutter/flutter/issues/182708) - 얇은 스트로크의 원이 거칠게(jagged) 보이는 시각적 결함을 수정했습니다.
* [flutter/183887](https://github.com/flutter/flutter/issues/183887) - 2024년 3월 보안 패치가 적용된 Android 기기에서 SCREEN_OFF 이벤트 시 발생하는 데드락 문제를 수정했습니다.

전체 [CHANGELOG.md](https://github.com/flutter/flutter/blob/master/CHANGELOG.md) 보러가기

# **Genkit Dart: 풀스택 AI 앱을 Dart로**

이번 달 가장 주목할 만한 소식은 **Genkit Dart**의 프리뷰 출시입니다. 기존에 TypeScript, Go, Python에서 사용 가능했던 Google의 오픈소스 AI 프레임워크 Genkit이 드디어 Dart를 공식 지원하게 되었습니다.

### 주요 특징

* **다양한 AI 모델 지원**: Google, Anthropic, OpenAI 등 주요 AI 공급자를 즉시 사용 가능
* **타입 안전한 AI 흐름**: `schemantic` 패키지를 활용하여 강력한 타입의 데이터와 타입 안전한 AI Flow를 구성
* **프론트엔드 & 백엔드 통합**: Flutter 앱 내부에서 직접 사용하거나, Shelf HTTP Server를 통해 백엔드에서도 동작
* **엔드투엔드 타입 안전성**: 프론트엔드와 백엔드가 동일한 Dart 스키마를 공유하여 완벽한 타입 안전성 보장

Flutter 개발자가 동일한 Dart 언어로 AI 기능까지 구축할 수 있는 길이 열린 만큼, 풀스택 Dart 생태계가 한층 더 강화될 것으로 기대됩니다.

* [Announcing Genkit Dart (Dart 공식 블로그)](https://blog.dart.dev/announcing-genkit-dart-build-full-stack-ai-apps-with-dart-and-flutter-2a5c90a27aab)
* [genkit 0.12.0 (pub.dev)](https://pub.dev/packages/genkit)
* [genkit-dart GitHub](https://github.com/genkit-ai/genkit-dart)

# **Google Antigravity로 20일 만에 20개 앱 만들기**

Flutter 공식 블로그에 흥미로운 글이 게시되었습니다. Dart & Flutter 팀에 합류한 Kevin Lamenzo가 Google의 에이전틱 IDE인 **Antigravity**(Gemini 기반 VS Code 포크)를 활용하여 20일 동안 20개의 Flutter 앱을 만든 경험담입니다.

건강 트래커, 동의어 슬라이더, GeoGuesser 스타일 게임(Street Sleuth), 학습 앱(Learn Witt), 보드게임 리메이크 등 다양한 장르의 앱을 AI 에이전트와 함께 기획하고 구현하는 "에이전틱 개발(Agentic Development)" 워크플로우를 생생하게 보여줍니다.

AI가 계획을 세우고, 코드를 작성하고, 오류를 수정하며, 개발자가 이를 검토하고 방향을 잡아주는 새로운 협업 방식이 인상적입니다.

* [20 apps in 20 days with Flutter and Antigravity (Flutter 블로그)](https://blog.flutter.dev/20-apps-in-20-days-with-flutter-and-antigravity-c62ce307c60b)
* [Google Antigravity 공식 문서](https://docs.flutter.dev/tools/antigravity)
* [Getting Started with Google Antigravity (Codelab)](https://codelabs.developers.google.com/getting-started-google-antigravity)

# **Flutter 행사 소식**

### Flutter Seoul Meetup! With Vibe Coding Hackathon

2026년 4월 25일(토) 13:00~19:00, 가천대학교 가천관 701호에서 Flutter Seoul 밋업이 열립니다. 개발자, 기획자, 디자이너 누구나 참여 가능한 해커톤으로, AI 코딩 에이전트와 자연어로 소통하며 앱을 만드는 바이브 코딩을 직접 체험할 수 있습니다.

* 티켓 구매 링크: [Flutter Seoul Meetup! With Vibe Coding Hackathon](https://ticketa.co/event/ycbz77ae)

### 다가오는 해외 Flutter 행사

* **FFDC 2026** (FlutterFlow Developer Conference) - 2026년 5월 27-28일, 샌프란시스코 + 온라인 ([ffdc.io](https://www.ffdc.io/))
* **FlutterCon USA** - 2026년 7월, 미국 올랜도 ([flutterconusa.dev](https://www.flutterconusa.dev))

# **Flutter 패키지 소식**

## genkit

[https://pub.dev/packages/genkit](https://pub.dev/packages/genkit)

위에서 소개한 Genkit Dart의 핵심 패키지입니다. `genkit_openai`, `genkit_mcp`, `genkit_middleware` 등 관련 패키지들도 함께 제공되어, AI 기능을 모듈 단위로 필요한 만큼 조합하여 사용할 수 있습니다.

## Very Good Ventures 소식

### Very Good AI Flutter Plugin (Alpha)

[https://github.com/VeryGoodOpenSource/very_good_ai_flutter_plugin](https://github.com/VeryGoodOpenSource/very_good_ai_flutter_plugin)

Very Good Ventures에서 공개한 AI 보조 Flutter 개발을 위한 플러그인입니다. 아키텍처 패턴, 네이밍 컨벤션, 테스트 전략, 접근성 등 Flutter 모범 사례를 AI 어시스턴트에게 컨텍스트로 제공하여 더 높은 품질의 코드 생성을 돕습니다.

* [Very Good AI Flutter Plugin 블로그](https://verygood.ventures/blog/very-good-ai-flutter-plugin/)

### Very Good CLI 테스트 개선

Flutter 테스트 워크플로우의 성능을 최적화하는 CLI 업데이트를 공개했습니다. 대규모 프로젝트에서의 테스트 실행 속도 개선에 초점을 맞추고 있습니다.

* [Flutter Tests with Very Good CLI](https://verygood.ventures/blog/flutter-tests-very-good-cli/)

## video_pool

[https://pub.dev/packages/video_pool](https://pub.dev/packages/video_pool)

TikTok, Reels, Instagram 스타일의 동영상 피드를 위한 오픈소스 비디오 풀 매니저 패키지입니다. 고정 개수의 플레이어를 재사용하는 컨트롤러 풀링 방식으로 메모리 효율성을 극대화하며, 스크롤 시 플레이어를 폐기하지 않고 재사용하여 프레임 드롭 없는 부드러운 경험을 제공합니다.

* **가시성 기반 라이프사이클**: 화면에 보이는 동영상만 재생
* **열 제한(Thermal Throttling)**: 기기 과열 시 자동으로 동시 재생 개수 감소
* **디스크 캐싱**: LRU 캐시로 동영상 사전 로드
* **오디오 포커스**: 백그라운드 전환 시 자동 일시정지
* **즉시 사용 가능한 위젯**: VideoFeedView, VideoListView 등 제공

* [Reddit 소개 글](https://www.reddit.com/r/FlutterDev/comments/1s3qrev/i_built_an_opensource_video_pool_manager_for/)

# **Flutter 오픈소스 소개**

## Flutter GenUI SDK

[https://github.com/flutter/genui](https://github.com/flutter/genui)

Google에서 공식으로 공개한 **GenUI SDK**는 LLM(대규모 언어 모델)을 활용하여 사용자의 의도에 따라 동적으로 적응하는 UI를 구축할 수 있는 SDK입니다. 기존의 정적인 UI를 넘어, AI가 사용자의 요청을 이해하고 적절한 UI 컴포넌트를 생성하는 새로운 패러다임을 제시합니다.

## AppFlowy

[https://github.com/AppFlowy-IO](https://github.com/AppFlowy-IO)

GitHub 스타 68,600개 이상을 기록하고 있는 오픈소스 Notion 대안 프로젝트입니다. AI 협업 워크스페이스를 표방하며, Flutter로 구축되어 크로스 플랫폼을 지원합니다. 3월에도 `appflowy-editor` 등 핵심 컴포넌트에 대한 업데이트가 이어지고 있습니다.

# **커뮤니티 인사이트**

### AI + Flutter 생태계의 전환점

3월은 Flutter 생태계에서 AI 통합이 본격적인 전환점을 맞이한 달이었습니다.

* **Google Antigravity** (에이전틱 IDE) + **Google Stitch** (AI 디자인 에이전트)가 개발 워크플로우를 혁신하고 있습니다.
* **Genkit Dart**가 타입 안전한 AI 프레임워크를 Dart/Flutter에 네이티브로 제공합니다.
* **Very Good AI Flutter Plugin**이 AI 보조 Flutter 개발의 모범 사례를 체계화했습니다.
* **Flutter GenUI SDK**가 LLM 기반의 동적 UI 생성을 가능하게 합니다.

Flutter 개발자에게 AI는 더 이상 별도의 기술 스택이 아닌, 개발 도구와 앱 기능 모두에 깊이 녹아드는 핵심 요소가 되어가고 있습니다.

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)
