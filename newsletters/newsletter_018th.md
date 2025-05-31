# Flutter Seoul Newsletter 18호

안녕하세요, 플러터 서울 홍종표(HDD), 박제창(Dreamwalker)입니다. 

5월의 마지막 주가 찾아왔습니다. Google I/O 2025에서 발표된 새로운 Flutter와 Dart 버전의 열기가 아직도 뜨겁게 달아오르고 있는 가운데, 개발자 커뮤니티 전체가 새로운 기능들을 탐험하며 흥미진진한 시간을 보내고 있습니다. 초여름의 싱그러운 기운과 함께 플러터 생태계도 한층 더 발전된 모습으로 성장하고 있습니다. 이번 호에서는 Google I/O의 주요 발표 내용부터 새롭게 업데이트된 기능들까지, 플러터 개발자 여러분이 놓치지 말아야 할 핵심 정보들을 정리해 드렸습니다. 함께 살펴보시죠.

이번 호에서는 다음과 같은 내용을 다룹니다.

* **Flutter 3.29.0, Dart 3.8 소식**
* **Google I/O 2025** 
* **한국의 첫 Flutter GDE 박제창님**  
* **Flutter 패키지 소식**

---

# Flutter 3.32.0, Dart 3.8 소식

Google I/O 2025에서 Flutter와 Dart의 최신 릴리즈가 발표되었으며, 개발자들이 고품질의 성능 좋은 크로스 플랫폼 앱을 만드는 새로운 방법들이 소개되었습니다.

Flutter 3.32에서는 웹 핫 리로드(실험적), iOS 충실도를 위한 Cupertino 스퀄클(squircles), Firebase와의 새로운 AI 통합 등의 주요 기능들이 추가되었습니다. 이 릴리즈는 웹, 프레임워크, Cupertino, Material, 접근성, 텍스트 입력, 데스크톱, iOS, Android, 그리고 엔진 컴포넌트 전반에 걸친 다양한 개선사항들을 포함하고 있습니다.

또한 Dart 3.8에서는 후행 쉼표 유지 옵션을 포함한 포매터 업데이트와 null이 아닐 경우에만 컬렉션에 요소를 추가할 수 있는 null-aware elements 기능 등이 개발자 편의성을 개선했습니다.

한글로 번역된 글들은 아래 링크에서 보실 수 있습니다.

[https://medium.com/flutter-korea/번역-whats-new-in-flutter-3-32-f63e87238776](https://medium.com/flutter-korea/번역-whats-new-in-flutter-3-32-f63e87238776)

[https://medium.com/flutter-korea/announcing-dart-3-8-번역-ab7bb373dfc9](https://medium.com/flutter-korea/announcing-dart-3-8-번역-ab7bb373dfc9)

# Google I/O 2025 

Google I/O 2025가 어김없이 찾아왔습니다\! 올해 Flutter 세션에서는 크로스 플랫폼 개발의 미래를 엿볼 수 있는 다양한 혁신적인 소식들이 공개될 예정입니다. 특히 WebAssembly (WASM) 지원을 통해 웹 앱 성능이 크게 향상될 것으로 기대되며, AI 및 머신러닝 통합 기능도 더욱 강력해질 것으로 예상됩니다. 또한, Flutter는 단일 코드베이스로 여러 플랫폼을 지원하며 개발 시간을 단축하고 비용을 절감하는 데 큰 기여를 하고 있습니다. 새로운 도구와 기능들을 통해 개발자 경험이 한층 더 향상될 이번 Google I/O 2025 Flutter 세션도 많은 관심 부탁드립니다.

## **What's new in Flutter**

**영상 바로보기 : [What's new in Flutter](https://youtu.be/v6Rzo5khNE8?si=rGaKoCItd4TRn3-G)**

Dart와 Flutter의 최신 릴리스를 확인해 보세요\! Dart와 Flutter가 현대 앱 개발자들의 요구를 충족시키기 위해 어떻게 진화하고 있는지 알아보세요. 또한, Flutter 프레임워크의 새로운 업데이트 소식과 여러 플랫폼에서 고품질의 고성능 앱을 구축하는 새로운 방법에 대해서도 배울 수 있습니다.

### **영상 요약** 

Dart와 Flutter는 현대 앱 개발자들의 요구를 충족시키기 위해 지속적으로 발전하고 있습니다. 이들은 단일 코드베이스를 통해 모바일, 데스크톱, 웹, 임베디드 장치 등 모든 플랫폼에서 고품질의 풍부한 경험을 제공하는 데 중점을 둡니다.  
주요 업데이트 및 개선 사항은 다음과 같습니다.

* **다트(Dart) 언어 발전**  
  * Null 안전성, 패턴, 스위치 표현식, 클래스 수정자, 레코드, 확장 타입, 숫자 구분 기호, 와일드카드 변수, 널 인식 요소, 점 표기법 단축 등 다양한 기능이 추가되거나 개선되어 개발 생산성이 향상되었습니다.  
  * 다트 CLI 도구의 성능이 크게 향상되어 dart format, dart doc, dart analyze 명령어가 훨씬 빨라졌습니다.  
  * 크로스 컴파일 기능이 지원되어 Windows 및 macOS에서 Linux 바이너리를 컴파일할 수 있게 되었습니다.  
      
* **개발자 경험(DX) 향상**  
  * 새로운 속성 편집기(Property editor) 기능을 통해 위젯 속성을 IDE에서 직접 쉽게 변경하고 소스 코드에 반영할 수 있습니다.  
  * pub.dev 패키지 관리자의 다크 모드, 다운로드 수 및 인기 패키지 확인 기능이 추가되었으며, 구글 클라우드 인프라로의 마이그레이션을 완료하여 안정성을 높였습니다.  
  * 다트 포매터(Dart formatter)가 후행 쉼표 자동 처리 및 포매팅을 최적화하여 코드 가독성을 향상시켰습니다.

* **플랫폼 통합 및 성능 최적화**  
  * Flutter UI 스레드를 플랫폼 스레드와 병합하여 네이티브 상호 운용성을 개선하고 타입 안전성을 확보하며, 빌드 훅스(Build Hooks), FFIgen/JNIgen과 같은 기능으로 네이티브 API 호출을 간소화했습니다.  
  * iOS에서는 스프링 및 스크롤 물리학, 하단 시트, 확장 가능한 내비게이션 바 등 쿠퍼티노(Cupertino) 위젯 라이브러리의 충실도가 향상되었습니다. 특히 Squircle과 같은 Apple 고유의 모양도 고품질로 구현되었습니다.  
  * Android에서는 Impeller가 기본 렌더러로 채택되어 성능이 최적화되었고, Edge-to-edge UI가 기본으로 지원됩니다.  
  * 웹(Web)에서는 WebAssembly(WasmGC) 지원을 통해 앱 시작 시간이 단축되고 복잡한 시나리오에서 프레임 렌더링 속도가 최대 두 배 빨라졌습니다. 웹용 스테이트풀 핫 리로드(Stateful Hot Reload)도 프리뷰로 제공됩니다.  
* **생태계 확장 및 AI 통합**  
  * Flutter는 2021년부터 가장 많이 사용되는 멀티 플랫폼 앱 프레임워크로 선정되었으며, 새로운 무료 앱의 28%가 Flutter를 사용하고 있습니다.  
  * Reflection(AI 기반 저널링), teamLab(인터랙티브 아트), Google Cloud 모바일 앱, NotebookLM(AI 연구/작성 도우미) 등 다양한 성공 사례가 있습니다.  
  * 캐노니컬(Ubuntu), LG(webOS SDK), 유니버설 데스티네이션즈 앤 익스피리언스(Universal Destinations & Experiences), 1080 Motion, GE Appliances 등 여러 기업이 Flutter를 채택하고 있습니다.  
  * Firebase AI Logic과 Gemini Live API를 통해 실시간 음성 및 영상 상호작용을 지원하는 AI 기반 앱을 쉽게 구축할 수 있습니다 (예: 식물 식별 앱).  
  * 다트패드(DartPad), Android Studio, VS Code에 Gemini 지원이 통합되어 AI 기반 개발이 가능하며, Model Context Protocol(MCP)을 통해 더 정확하고 관련성 높은 코드 생성 및 제안을 제공합니다.

## Build agentic apps with Flutter and Firebase AI Logic

**영상 바로보기 : [How to build agentic apps with Flutter and Firebase AI Logic](https://youtu.be/xo271p-Fl_4?si=NFHpDgfWJwoCB6bj)**

멀티모달 AI는 사용자가 애플리케이션과 상호작용하는 방식을 변화시키고 있습니다. Flutter, Firebase 및 Gemini를 사용하여 안전하고 확장 가능하며 지능적인 멀티플랫폼 및 멀티모달 AI 앱을 구축하는 방법을 알아보는 시간을 가져보세요. 최첨단 앱의 아키텍처를 분석하여 단일 코드베이스를 사용하여 음성, 이미지, 텍스트 상호작용을 웹 및 모바일 환경에 원활하게 통합하는 방법을 보여드립니다. 또한 Google Cloud의 최신 AI 발전을 기반으로 매력적인 사용자 경험을 만드는 방법을 공유할 예정입니다.

### **영상 요약** 

* 1\. 에이전트 앱의 시연 (데모):  
  * 비디오는 사용자가 앱의 색상 변경(노란색에서 파란색으로)이나 글꼴 변경에 대해 피드백을 제공하고, 느린 스크롤 문제에 대한 피드백 보고서를 생성하는 "myMail" 앱을 보여줍니다. 이는 앱이 사용자의 자연어 피드백을 이해하고 적절한 조치를 취하며, 심지어 추가 정보를 요청하는 등 에이전트 기능을 시연합니다.  
* 2\. 핵심 개념:  
  * 생성형 AI(GenAI): 프롬프트를 통해 코드, 이미지, 비디오와 같은 새로운 콘텐츠와 경험을 생성하는 기술입니다.  
  * AI 에이전트: 세상을 관찰하고, 도구를 사용하여 목표를 달성하려는 애플리케이션입니다. 에이전트는 언어 모델(LM)을 의사결정자로, 외부 세계와 상호 작용하는 도구(API)를 사용하며, 목표 달성을 위해 지속적으로 정보를 처리하고 결정합니다.  
* 3\. 기술 스택:  
  * Firebase: Google의 올인원 앱 개발 플랫폼으로, AI 기반 경험을 쉽게 구축하고 실행할 수 있도록 돕습니다. 특히 App Check과의 통합을 통해 프로덕션 환경에서 앱을 안전하게 보호합니다.  
  * Vertex AI in Firebase (Vertex SDK): 모바일 및 웹 앱에 GenAI 기능을 추가하는 쉬운 방법이며, 정식 출시(GA)되었습니다. 다양한 기능을 지원하며, Firebase의 다른 서비스들과도 긴밀하게 통합되어 있습니다.  
  * Flutter: 세계에서 가장 인기 있는 멀티플랫폼 앱 개발 SDK입니다. 단일 코드베이스로 iOS, Android, 웹, 데스크톱 등 다양한 플랫폼에 프로덕션 수준의 앱을 배포할 수 있습니다. Firebase와 Flutter는 100% Dart로 코드를 작성하여 개발 효율성을 높입니다.  
* 4\. 에이전트 앱 작동 방식 (아키텍처 및 코드):  
  * Flutter 앱은 사용자의 텍스트 피드백과 마크업된 스크린샷을 Gemini 2.0 모델(Flash, Live, Thinking)로 보냅니다. 이때 "친절하고 도움이 되는 앱 컨시어지"와 같은 시스템 지침을 함께 전달하여 에이전트의 페르소나와 목표를 정의합니다.  
  * Gemini는 '함수 호출'(도구 사용 지시)을 출력합니다. 예를 들어, setAppColor(앱 색상 변경), setFontFamily(글꼴 변경), fileFeedbackReport(피드백 보고서 생성)와 같은 도구들을 호출합니다.  
  * Gemini는 직접 함수를 실행하지 않고, 앱에게 "이것을 하라"고 지시를 내리면, 앱이 해당 작업을 수행합니다. 이는 마치 유능한 조수에게 지시를 내리는 것과 같습니다.  
  * 도구는 FunctionDeclaration을 통해 이름, 설명, 매개변수 등으로 명확하게 정의됩니다. 좋은 설명은 LLM이 올바른 도구를 선택하고 유용한 매개변수를 생성하는 데 중요합니다.  
* 5\. 고급 기능:  
  * Imagen 3: Vertex AI를 통해 제공되는 이미지 생성 모델로, 앱 내에서 프로필 사진과 같은 이미지를 생성하는 데 사용될 수 있습니다.  
  * 실시간 양방향 오디오 스트리밍: Gemini의 Live API를 사용하여 앱 내에서 에이전트와 실시간으로 음성 대화를 나눌 수 있는 기능(현재 미리보기)도 소개되었습니다. 이 기능은 동일한 API 구조를 따르며, 음성 대화를 통해 사용자 경험을 더욱 풍부하게 만듭니다.

## **How Flutter makes the most of your platforms**

**영상 바로보기 :** [How Flutter makes the most of your platforms](https://youtu.be/flwULzNYRac?si=wJ5SfPbpxDvahsWP)

네이티브 API 및 플랫폼별 UI 구성 요소를 사용하여, Android와 iOS에서 각 플랫폼의 고유한 외관과 느낌을 제공하여 마치 기본 앱처럼 자연스럽게 어울리도록 Flutter 앱을 구축하는 방법을 배웁니다.

### **영상 요약** 

Flutter는 크로스 플랫폼 개발을 위한 강력한 도구를 제공하는 동시에 네이티브 플랫폼 기능, UI 및 API와 깊은 통합을 제공합니다. 메소드 채널이 네이티브 코드와 상호 작용하는 방법을 제공하는 반면, JNIgen 및 FFIgen과 같은 도구는 네이티브 라이브러리에 대한 직접 Dart 바인딩을 생성하여 프로세스를 간소화합니다. 또한 플랫폼 뷰는 Flutter 위젯과 함께 네이티브 UI 구성 요소를 원활하게 삽입할 수 있도록 합니다. 이러한 기능을 통해 개발자는 기존 네이티브 코드를 포기하거나 프로젝트를 처음부터 시작하지 않고도 대상 플랫폼의 모든 잠재력을 활용할 수 있습니다.

Flutter 아키텍처: "Layer Cake”(레이어 케이크)

Flutter의 아키텍처는 구성 요소들이 서로를 기반으로 하는 "레이어 케이크" 시스템으로 구성됩니다:

* 프레임워크 (Dart): 위젯, 제스처, 접근성, 텍스트 입력 등을 위한 고수준의 재사용 가능한 API를 제공합니다.  
* 엔진 (C/C++): 기본 플랫폼과 Flutter 간의 메시징, 렌더링 및 기타 핵심 기능을 담당하는 저수준 레이어입니다.  
* 임베더 (플랫폼별): 호스트 시스템에서 Flutter 앱으로 진입하는 진입점으로, 각 플랫폼의 기본 언어(예: Android용 Java/Kotlin, iOS용 Objective-C/Swift)로 구현됩니다.

네이티브 상호 운용성 (Interop)

네이티브 플랫폼 기능 및 라이브러리에 액세스하기 위해 Flutter는 여러 옵션을 제공합니다:

* 메소드 채널(Method Channels): Dart와 호스트 플랫폼 간의 명명된 통신 채널입니다. Flutter가 메시지를 보내면, 네이티브 플랫폼이 이를 가로채서 네이티브 코드를 실행하고 결과를 반환합니다. 기능적이지만, 메소드 채널은 복잡한 객체에 대해 번거롭고 수동적인 타입 안전성을 요구하며, 서로 다른 플랫폼에서 API가 변경될 때 유지보수 비용을 증가시킬 수 있습니다. Pigeon 패키지는 타입 안전하고 쉬운 통신을 위한 코드 생성 도구를 제공하여 이러한 한계를 해결합니다.  
* JNIgen: 특히 Android 개발용으로, JNIgen은 Java Native Interface(JNI)를 통해 Java/Kotlin 코드를 직접 호출하고 실행할 수 있는 Dart 코드를 생성합니다. 이를 통해 개발자는 네이티브 Dart 라이브러리를 게시하지 않는 Android Health Connect와 같은 Android 특정 라이브러리를 통합할 수 있습니다. JNIgen은 Java/Kotlin 클래스에 대한 Dart 바인딩 생성 과정을 간소화합니다. 내부적으로 FFIgen을 사용하여 C 바인딩을 생성합니다.  
* FFIgen: Foreign Function Interface로, iOS 및 기타 플랫폼에서 사용되며 Dart가 C/Objective-C/Swift 코드를 직접 호출할 수 있도록 합니다.

JNIgen의 장점:

* 흐름 유지: 언어 간 전환 없이 Dart 코드를 작성할 수 있습니다.  
* API 즉시 액세스: 새로운 API가 출시되는 즉시 바인딩을 생성할 수 있습니다.  
* 쉬운 변환: 네이티브 샘플 코드 스니펫을 생성된 바인딩을 사용하여 Dart로 쉽게 변환할 수 있습니다.

플랫폼 뷰(Platform Views)

플랫폼 뷰를 통해 개발자는 네이티브 UI 구성 요소를 Flutter 애플리케이션에 직접 삽입할 수 있습니다. 이는 네이티브 위젯의 Flutter 버전이 없거나, 기존 네이티브 UI 구성 요소를 Flutter로 마이그레이션하기가 즉시 불가능할 때 특히 유용합니다.

플랫폼 뷰의 작동 방식:

* Flutter는 네이티브 구성 요소를 위한 래퍼 역할을 하는 UiKitView(iOS용) 또는 AndroidView(Android용)와 같은 위젯을 제공합니다.  
* 네이티브 측의 팩토리 클래스가 Flutter의 요청을 가로채서 네이티브 뷰를 생성하고 삽입합니다.  
* 네이티브 뷰의 구현은 네이티브 코드(예: iOS용 Swift, Android용 Kotlin)에 있습니다.

플랫폼 뷰의 성능 고려사항:

플랫폼 뷰를 사용하면 그리기 위해 주 플랫폼 스레드를 사용하므로 성능 비용이 발생하며, 이는 다른 필수 작업을 방해할 수 있습니다. 따라서 네이티브 구성 요소가 정말로 필요한 경우에만 신중하게 사용해야 합니다.

# 🎉 한국 최초의 Flutter GDE 탄생을 축하합니다\!

Flutter Seoul 커뮤니티의 Dreamwalker(박제창)님이 한국 첫 번째 Flutter Google Developer Expert로 선정되었습니다.

한국 Flutter 생태계 발전에 기여해온 노고에 깊은 감사를 드리며, 앞으로도 Flutter 커뮤니티와 함께 더 큰 성장을 이루어 나가시길 응원합니다.

# Flutter 패키지 소식

## time\_plus

'time\_plus' 패키지는 Flutter 개발자들이 날짜와 시간을 더 효율적으로 다룰 수 있도록 도와주는 새로운 도구입니다.

패키지 개발자는 아래와 같이 말합니다.

수년간 Dart의 네이티브 `DateTime`과 `Duration` API로 씨름한 끝에, `time_plus`를 만들었습니다 — **128개의 신중하게 설계된 API**와 **700개 이상의 테스트**로 엣지 케이스, 윤년 로직, 변환 등을 검증하는 가볍고 의존성 없는 extension 패키지입니다.

이 패키지는 제가 다양한 프로젝트에서 개인적으로 작성하고 사용해온 수십 개의 extension 으로 구성되어 있으며, 마침내 이들을 하나의 일관된 패키지로 *패키징*했습니다.

정확하고, 프로덕션에 안전하며, 실제 앱에서 검증된 패키지입니다 — 함정이나 보일러플레이트 없이 표현력 있고 신뢰할 수 있는 시간 계산을 제공하도록 설계되었습니다.

Dart에서 시간을 다루고 있고 *그냥 작동하는* 도구를 원한다면, 전체 README를 자유롭게 살펴보세요 — 상세한 문서, 실제 예제, 그리고 이 패키지가 제공하는 모든 것들로 가득합니다.

[pub.dev 링크](https://pub.dev/packages/time_plus)

## use\_scramble 

무작위 텍스트 애니메이션을 위한 경량 패키지입니다.  
앱을 만들다가 무작위 텍스트 애니메이션을 사용할 일이 있다면 사용해보셔도 좋을 것 같습니다.

[pub.dev 링크](https://pub.dev/packages/use_scramble)

## D4RT

D4rt (다트라고 발음한다고 합니다.) 는 Dart 로 작성된 Dart 언어의 인터프리터 & 런타임 입니다.  
해당 패키지를 통해 Dart 코드를 동적으로 실행할 수 있다고 합니다.

[pub.dev 링크](https://pub.dev/packages/d4rt)

# Flutter 로 만들어진 앱

## Wine Prefix Manager

리눅스에서 윈도우즈 애플리케이션을 사용하게 해주는 앱이라고 합니다.

홈페이지 링크:[Wine Prefix Manager \- Simplify Your Windows Apps on Linux](https://wpm.crownparkcomputing.com/)  
깃허브 링크: [CrownParkComputing/wine\_prefix\_manager](https://github.com/CrownParkComputing/wine_prefix_manager)

## Google NotebookLM

Google NotebookLM은 Google이 개발한 혁신적인 AI 기반 연구 및 메모 작성 도구입니다.  
해당 앱이 플러터로 제작되었다고 합니다.

구글 플레이스토어 링크: [Google NotebookLM \- Google Play 앱](https://play.google.com/store/apps/details?id=com.google.android.apps.labs.language.tailwind)

---

**Flutter Seoul 뉴스레터 구독하기**

Flutter Seoul 의 뉴스레터 구독을 원하시는 분들은 해당 리포지토리의 `watch` 눌러 구독하실 수 있습니다

---

플러터 서울 공식 트위터: [@FlutterSeoul](https://twitter.com/flutterseoul?s=21&t=1lvvhkp7LX_b-JT8sVoYCA)

플러터 서울 공식 디스코드: [https://flutter-seoul.com](https://flutter-seoul.com)

플러터 서울 공식 오픈 카카오톡: [참여하기](https://open.kakao.com/o/gdL2Gj1e)

플러터 서울 공식 밋업: [https://meetup.flutter-seoul.com](https://meetup.flutter-seoul.com)
