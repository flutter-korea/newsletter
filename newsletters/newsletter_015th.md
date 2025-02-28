# Flutter Seoul Newsletter 15호

안녕하세요, 플러터 서울 커뮤니티의 홍종표(HDD), 박제창(Dreamwalker)입니다.

2월 뉴스레터로 다시 찾아뵙게 되었습니다. 이번에도 관심을 끌만한 플러터 소식들을 모아 봤습니다. 궁금한 점이나 의견이 있다면 언제든지 편하게 말씀 해주세요.

이번 호에서는 다음과 같은 내용을 다룹니다.

- **Flutter 2.29.0, Dart 3.7.0 업데이트**
- **Flutter 패키지 소개**
- **Flutter 로 제작된 앱 소개**

---

# **1. Flutter 3.29.0 & Dart 3.7.0 업데이트 소식**

2월 13일 Flutter 3.29.0 과 Dart 3.7.0 버전이 출시되었습니다.

Flutter Seoul 의 aiden님과 함께 Flutter 3.29.0, Dart 3.7.0 버전에 대해 번역한 글이 있으니, 자세한 내용은 medium 글에서 확인하실 수 있습니다.

**👉 [[번역] Announcing Dart 3.7](https://medium.com/flutter-korea/%EB%B2%88%EC%97%AD-announcing-dart-3-7-928b75d02255)**

👉 [**What’s new in Flutter 3.29 (번역)**](https://medium.com/flutter-korea/whats-new-in-flutter-3-29-번역-91dc5808129c)

# **2. Flutter 패키지 소식**

### **2.1 and_os 패키지 소개**

and_os 패키지는 Flutter 앱을 위한 보안 검사 패키지입니다.

안드로이드의 경우 **루트 상태**, **ADB(USB 디버깅) 상태**, **개발자 모드**, **앱 디버깅, Frida의 존재(역엔지니어링 툴), 
앱 서명 변조, 에뮬레이터** 등을 감지하며 iOS에서는 **디버그 모드, 에뮬레이터 감지, 런타임 변조, 앱 디버깅 상태** 등을 감지할 수 있다고 합니다.

위 패키지를 사용하여 보다 안전한 앱 개발에 활용할 수 있을 것 같습니다.

👉 [pub.dev 링크](https://pub.dev/packages/and_os)

# **3. Flutter 관련 앱, 오픈소스 소개**

### 3.1 Jaspr 와 Dart 로 구축된 오픈소스 블로그 엔진 **WriteSync**

앞으로 더 많은 테마와 플러그인을 만들 수 있도록 개발 예정이라고 합니다.

아래와 같은 특징을 가지고 있다고 합니다.

**🎨 현대적인 디자인:** Tailwind CSS를 사용한 깔끔하고 미니멀한 UI

**🌓 다크 모드:** 매끄러운 라이트/다크 모드 전환

**📱 반응형:** 모바일 우선의 반응형 디자인

**🚀 서버 사이드 렌더링:** SSR을 통한 빠른 로딩 속도

**📝 마크다운 지원:** 마크다운으로 게시글 작성

**🔍 검색:** 전체 텍스트 검색 기능

**🏷️ 태그:** 태그로 게시글 정리

**📊 스마트 페이지네이션:** 다양한 표시 옵션을 가진 설정 가능한 페이지네이션

**🌟 추천 게시글:** 추천 게시글을 위한 다양한 전략

**🎯 SEO 최적화:** 동적 메타 태그 및 구조화된 데이터

**🔄 소셜 통합:** 쉬운 소셜 미디어 공유

**📈 분석 통합:** Lukehog Analytics 내장 지원

👉 [깃허브 레포지터리 링크](https://github.com/tayormi/writesync?ref=producthunt)

### 3.2 pub.dev의 stat을 트래킹해주는 [pubstats.dev](http://pubstats.dev) 사이트

pub.dev에 올린 패키지들의 stat을 트래킹 해주는 사이트입니다.

주간, 월간, 분기별, 연간, 총 변화를 보여줍니다.

또한 변화가 생겼을 때 Discord 웹훅 알림등도 제공한다고 합니다.

👉 [pubstats.dev 사이트](http://pubstats.dev)

👉 [깃허브 레포지터리 링크](https://github.com/Rexios80/pub_stats/tree/master)

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com/)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com/)