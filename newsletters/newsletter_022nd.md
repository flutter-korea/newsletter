# Flutter Seoul Newsletter 22호

안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다. 

추석 연휴를 앞두고 인사드립니다. 가족, 친구들과 따뜻한 명절 보내시고, 잠시 여유를 가지며 재충전하는 시간 되시길 바랍니다. 🌕

그럼, 이번 달  Flutter 업데이트 소식 전해드립니다\!

이번 호에서는 다음과 같은 내용을 다룹니다.

- Flutter 3.35 & Dart 3.9 패치 소식  
- Flutter Seoul 행사 소식  
- Flutter 패키지 소식  
- Flutter 관련 오픈소스


# Flutter 3.35 & Dart 3.9 패치 소식

### **3.35.3**

* [flutter/172627](https://github.com/flutter/flutter/issues/172627) \- non-verbose 모드에서 불필요한 출력이 표시되는 문제를 수정했습니다.  
* [flutter/173917](https://github.com/flutter/flutter/issues/173917) \- Android에서 `--build-number` 사용 시 `flutter build apk`가 버전 코드 계산에 실패하는 문제를 수정했습니다.  
* [flutter/174437](https://github.com/flutter/flutter/issues/174437) \- Flutter 웹 애플리케이션을 디버그 모드로 실행할 때 콘솔에 치명적이지 않은 오류 메시지가 대량으로 출력되는 문제를 수정했습니다.  
* [flutter/174267](https://github.com/flutter/flutter/issues/174267) \- Golden 테스트 실패 시 테스트 하네스가 멈추는 문제를 수정했습니다.  
* [flutter/171691](https://github.com/flutter/flutter/issues/171691) \- 경쟁 조건(race condition)으로 인해 Impeller Vulkan 백엔드에서 충돌이 발생하는 문제를 수정했습니다.  
* [flutter/174100](https://github.com/flutter/flutter/issues/174100) \- Impeller 사용 시 슈퍼타원(Superellipse)이 올바르게 렌더링되지 않는 문제를 수정했습니다.  
* [flutter/174015](https://github.com/flutter/flutter/issues/174015) \- Xcode에서 빌드 모드 전환 시 구식 경고 및 오류 메시지가 표시되는 문제를 수정했습니다.

### **3.35.4**

* [flutter/173474](https://github.com/flutter/flutter/issues/173474) \- 모든 플랫폼에서 핫 리스타트 후 PlatformDispatchers.instance.engineId가 더 이상 null을 반환하지 않습니다.  
* [flutter/174513](https://github.com/flutter/flutter/issues/174513) \- iOS 26에서 플랫폼 뷰의 제스처 차단이 실패하여 Flutter 뷰의 터치가 하위 플랫폼 뷰로 전달되는 버그를 수정했습니다.

### **3.35.5**

* [flutter/172105](https://github.com/flutter/flutter/issues/172105) iOS add-to-app 환경에서 여러 번 화면 전환 후 Flutter 뷰 멈춤 현상 해소.  
* [flutter/173106](https://github.com/flutter/flutter/issues/173106) 다중 커서(Multiple cursors)가 올바르게 표시됩니다.

# Flutter Seoul 행사 소식

## Flutter Alliance 2025

* 티켓 구매 링크: [Flutter Alliance 2025 | 티켓타코](https://www.ticketa.co/events/27)
* 일자: 2025년 10월 19일 (일) 10시 30분 \- 17시 00분  
* 장소: [한국마이크로소프트 13층](https://maps.app.goo.gl/99p5Nn4TfNWp8azF7) (서울특별시 종로구 중학동 종로1길 50\)


## Flutter Korea 2025

* 티켓 구매 링크: [https://www.ticketa.co/events/26](https://www.ticketa.co/events/26)  
* 일자: 2025년 10월 25일 (토) 13시 00분 \- 21시 00분  
* 장소: 구글 스타트업 캠퍼스 서울  
* 주관: Flutter Seoul

# Flutter 패키지 소식

## polly\_dart

**Polly**는 .NET 생태계에서 가장 널리 사용되는 회복성 및 일시적 오류 처리 라이브러리입니다.  
**Polly Dart**는 .NET Polly의 공식 Dart 포팅 버전으로, Flutter 개발자들이 동일한 수준의 회복성 패턴을 사용할 수 있게 합니다.

### 🎓 Polly Dart 장점

 ✅ **검증된 패턴**: .NET 생태계에서 수년간 검증된 회복성 패턴을 Flutter에서 그대로 활용  
 ✅ **선언적 API**: 복잡한 에러 처리 로직을 간결하고 읽기 쉬운 코드로 표현  
 ✅ **프로덕션 준비**: 네트워크 불안정, 서버 장애, 과부하 등 실제 운영 환경의 다양한 시나리오 대응  
 ✅ **유연한 조합**: 여러 전략을 파이프라인으로 조합하여 복잡한 회복성 로직 구현  
 ✅ **타입 안전성**: Dart의 강력한 타입 시스템을 활용한 안전한 에러 처리

**GitHub**: [https://github.com/flutterninja9/polly_dart](https://github.com/flutterninja9/polly_dart)  
**Pub.dev**: [https://pub.dev/packages/polly_dart](https://pub.dev/packages/polly_dart)

## Contribution Heatmap \- GitHub 스타일 기여도 히트맵 위젯

### 📊 패키지 소개

**Contribution Heatmap**은 Flutter용 고성능 GitHub 스타일 기여도 히트맵 위젯입니다. 커스텀 RenderBox 구현으로 최고의 효율성과 완벽한 커스터마이징을 제공하며, 시간에 따른 기여 데이터를 시각적으로 표현합니다.

### ✨ 주요 특징

### **🚀 성능과 최적화**

* **초고성능**: 커스텀 RenderBox 구현으로 최적화된 렌더링 파이프라인  
* **스마트 무효화**: 필요한 부분만 재계산하여 프레임 드롭 방지  
* **메모리 효율성**: HashMap 기반 데이터 구조로 빠른 조회 및 최소 GC 압력  
* **확장성**: 수천 개의 데이터 포인트도 원활하게 처리

### **🎨 기능과 커스터마이징**

* **👆 인터랙티브**: 완벽한 탭 지원 및 제스처 처리  
* **🎨 완전한 커스터마이징**: 색상, 크기, 레이블, 레이아웃 옵션  
* **📅 월별 분리 뷰**: 시각적으로 월을 구분하여 표시  
* **📊 셀 날짜 표시**: ⭐NEW\! 기여도 셀 내부에 날짜 숫자 표시  
* **♿ 접근성**: 텍스트 스케일링 및 고대비 모드 지원  
* **🌍 국제화**: 로케일 인식 텍스트 렌더링 및 커스터마이징 가능한 주 시작일

**Pub.dev**: [https://pub.dev/packages/contribution_heatmap](https://pub.dev/packages/contribution_heatmap)  
**GitHub**: [https://github.com/abdullah-cse/contribution_heatmap](https://github.com/abdullah-cse/contribution_heatmap)

### Loader Pro \- 현대적인 커스터마이징 가능한 로더 컬렉션

### 📦 패키지 소개

**Loader Pro**는 다양한 스타일의 현대적이고 아름다운 로딩 애니메이션을 제공하는 Flutter 패키지입니다. 간단한 API로 앱에 세련된 로더를 추가할 수 있습니다.

### 🎭 제공되는 로더 타입

Loader Pro는 **11가지** 독특한 로더 스타일을 제공합니다:

1. **Square** (사각형) \- 클래식한 사각형 로더  
2. **Squircle** (스쿼클) \- 부드러운 사각형 (Square \+ Circle)  
3. **Reuleaux** (뢸로) \- 독특한 삼각형 기반 곡선 도형  
4. **Ripples** (파문) \- 물결 효과 애니메이션  
5. **Ping** (핑) \- 펄스 효과  
6. **LineWobble** (라인 워블) \- 흔들리는 선 애니메이션  
7. **Pulsar** (펄사) \- 펄스 효과 로더  
8. **Star** (별) \- 별 모양 로더  
9. **DotPulse** (점 펄스) \- 점이 펄스하는 애니메이션  
10. **DotStream** (점 스트림) \- 흐르는 점 애니메이션  
11. **Trefoil** (세잎 클로버) \- 세잎 모양 로더  
12. **Hatch** (해치) \- 해치 패턴 로더

**Pub.dev**: [https://pub.dev/packages/loader\_pro](https://pub.dev/packages/loader_pro)

# Flutter 관련 오픈소스

## RMinder \- 프라이버시 우선 개인 재정 관리 앱 💰

📱 앱 소개

전 오프라인 개인 재정 관리 앱입니다. 사용자가 더 똑똑하게 예산을 관리하고 빚을 빠르게 갚을 수 있도록 설계된 프라이버시 우선 솔루션입니다.

### 💡 주요 기능

- **📊 제로 베이스 예산 관리** \- 모든 수입을 할당하여 남는 돈이 없도록 관리  
- **💸 빠른 거래 입력** \- 수입과 지출을 간편하게 기록하고 예산에 즉시 반영  
- **🏦 부채 및 채무 추적** \- 자동차 대출, 학자금 대출, 신용카드 등을 추가하고 실시간 상환 진행 상황 확인  
- **📈 시각적 리포트** \- fl\_chart를 활용한 지출 vs 예산, 부채 상환 차트  
- **📅 유연한 급여일 지원** \- 매월 1일이 아닌 급여일 기준으로 예산 시작 가능  
- **🏠 홈 스크린 위젯** (Android) \- 홈 화면에서 바로 거래 추가, 숫자 전용 키패드와 빠른 카테고리 선택  
- **🎨 커스텀 런처 아이콘** \- 전문적인 브랜드 앱 아이콘  
- **🧹 최적화된 UI** \- AppBar 제거 및 SafeArea 활용으로 깔끔하고 넓은 인터페이스

**GitHub**: [https://github.com/kahwai0227/rminder\_app](https://github.com/kahwai0227/rminder_app)

## comfer\_wallpaper \- Flutter로 만든 멀티플랫폼 배경화면 자동 변경 앱

### 📱 앱 소개

**Comfer Wallpaper**는 Flutter로 제작된 오픈소스 데스크탑 배경화면 자동 변경 애플리케이션입니다. Unsplash의 고품질 사진을 활용하여 사용자의 데스크탑에 아름다운 배경화면을 자동으로 설정해줍니다.

### 🎯 이런 분들께 추천합니다

* 매일 새로운 배경화면으로 데스크탑 환경을 바꾸고 싶은 분  
* 고품질의 아름다운 사진을 좋아하는 분  
* 간단하고 가벼운 배경화면 관리 도구를 찾는 분  
* Flutter 데스크탑 앱의 실제 사례를 보고 싶은 개발자

**💡 개발자 노트**: Flutter 프로젝트로, [Flutter 공식 문서](https://docs.flutter.dev/)에서 더 많은 정보를 확인할 수 있습니다. Comfer Wallpaper는 Flutter가 모바일뿐만 아니라 데스크탑 애플리케이션 개발에도 얼마나 효과적인지 보여주는 훌륭한 예시입니다\!

**GitHub**: [https://github.com/jeerovan/comfer\_wallpaper](https://github.com/jeerovan/comfer_wallpaper)

## Sim Flights Tracker \- 플라이트 시뮬레이션 네트워크 추적 앱

### 📱 앱 소개

**Sim Flights Tracker**는 VATSIM 및 IVAO 네트워크에서 시뮬레이션 비행과 관제사를 실시간으로 추적하는 Flutter 애플리케이션입니다. 플라이트 시뮬레이터 애호가들을 위한 필수 도구입니다.

### ✨ 핵심 특징

**🌐 실시간 추적**

* **VATSIM 네트워크**: 실시간 비행 및 관제사 추적  
* **IVAO 네트워크**: 글로벌 시뮬레이션 네트워크 지원  
* **실시간 데이터**: 라이브 플라이트 상태 및 위치 정보

**🗺️ 지도 통합**

* **Google Maps API**: 비행 경로 시각화  
* **대화형 지도**: 실시간 항공기 위치 확인

**공식 웹사이트**: [https://www.simflightstracker.com](https://www.simflightstracker.com)

**GitHub**: [https://github.com/Node-Ninja/sim-flights-tracker](https://github.com/Node-Ninja/sim-flights-tracker)

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)