<h1>Spring이란?</h1>
Spring Framework는 자바 플랫폼을 위한 오픈소스 애플리케이션 프레임워크<br>
동적인 웹 사이트를 개발하기 위한 여러가지 서비스를 제공<br>

<h1>Spring의 특징</h1>
- Plan Old Java Object 방식의 프레임 워크<br>
&nbsp;&nbsp;특정 라이브러리를 사용할 필요가 없어 개발이 쉽다.<br><br>
- Inversion Of Control(IOC:제어반전) 을 지원함<br><br>
- Dependency Injection(DI:의존성 주입)을 지원한다.<br> <br>
- Aspect-Oriented Programming(AOP:관점 지향 프로그래밍)을 지원<br> 
 &nbsp;&nbsp;트랜잭션이나 로깅, 보안과 같이 여러 모듈에서 공통적으로 사용하는 기능의 경우 해당 기능을 분리하여 관리가능<br> <br> 


IOC :: 프로그래머가 작성한 프로그램이 재사용 라이브러리의 흐름제어를 받게되는 소프트웨어 디자인 패턴<br> 
DI :: 하나의 객체가 다른 객체의 의존성을 제공하는 테크닉<br> 

<h1>SpringFramework 구조</h1>

![image](https://github.com/ovoaaahj/ComputerScience/assets/49386460/42c0a254-8f2a-41d4-aecd-ad1409a335cd)

<h3>Core Container</h3>
Core, Beans, Context 및 Expression Language 로 구성되어있음 <br>
Core 및 Beans모듈은 IoC 및 종속성 주입 기능을 포함하여 프레임워크의 기본부분을 제공<br>
이는 BeanFactory 팩토리 패턴을 정교하게 구현한것 <br>
이를통해 싱글톤 방식이 필요하지않으며, 실제 프로그램 논리에서 종속성 구성 및 사양 분리 가능<br><br>
Context 모듈은 Core 및 Beans 기반으로 구축<br>
JNDI레지스트리와 유사한 프레임워크 스타일 방식으로 객체에 엑세스하는 수단<br>
인터페이스 ApplicationContext 는 컨텍스트 모듈의 핵심<br><br>
SpEL 모듈은 런타임에 개체 그래프를 쿼리하고 조작하기 위한 강력한 표현 언어를 제공<br>
JSP 2.1 사양에 지정된 통합 표현 언어(unified EL)의 확장<br>
속성 값 설정 및 가져오기, 속성 할당, 메서드 호출, 배열, 논리 및 산술 연산자, 명명된 변수, Spring의 IoC 컨테이너에서 이름으로 개체 검색을 지원<br><br><br>

<h3>Data Access/Integration</h3>
Data Access/Integration 계층은 JDBC, ORM, OXM, JMS, Transaction 모듈로 이루어져있음<br>
JDBC 모듈은 데이터베이스 공급업체별 오류 코드 구문 분석을 수행할 필요성을 제거하는 JDBC 추상화 계층을 제공<br>
ORM 모듈은 PA , JDO 및 Hibernate 를 포함하여 널리 사용되는 객체 관계형 매핑 API에 대한 통합 레이어를 제공<br>
OXM 모듈 은 JAXB, Castor, XMLBeans, JiBX 및 XStream에 대한 객체/XML 매핑 구현을 지원하는 추상화 계층을 제공<br>
JMS (Java Messaging Service ) 모듈에는 메시지를 생성하고 소비하는 기능이 포함<br>
Transaction 모듈 은 특수 인터페이스를 구현하는 클래스와 모든 POJO(Plain Old Java Object) 에 대해 프로그래밍 방식 및 선언적 트랜잭션 관리를 지원<br><br><br>

<h3>Web</h3>
Web, Web-Servlet, WebSocket, Web-Portlet 모듈로 구성
Spring’s Web 모듈은 멀티파트 파일 업로드 기능, 서블릿 리스너 및 웹 지향 애플리케이션 컨텍스트를 사용한 IoC 컨테이너 초기화와 같은 기본적인 웹 지향 통합 기능을 제공<br>
Web-Servlet 모듈은 웹 애플리케이션을 위한 Spring의 MVC (모델-뷰-컨트롤러) 구현이 포함되어 있습니다. Spring의 MVC 프레임워크는 도메인 모델 코드와 웹 양식 간의 명확한 분리를 제공하고 Spring Framework의 다른 모든 기능과 통합.<br>
Web-Portlet 모듈은 포틀릿 환경에서 사용할 MVC 구현을 제공하고 웹 서블릿 모듈의 기능을 미러링합니다.<br><br><br>

<h3>AOP and Instrumentation</h3>
AOP 모듈은 분리되어야 하는 기능을 구현하는 코드를 깔끔하게 분리하기 위해 메서드 인터셉터 및 포인트컷 등을 정의할 수 있도록 AOP Alliance 호환 측면 지향 프로그래밍 구현을 제공<br>
Instrumentation 모듈은 특정 애플리케이션 서버에서 사용할 클래스 계측 지원 및 클래스 로더 구현을 제공<br><br><br>

<h3>Test</h3>
Test 모듈은 JUnit 또는 TestNG를 사용한 Spring 구성 요소 테스트를 지원<br><br><br>


<h1>사용 시나리오</h1>

![image](https://github.com/ovoaaahj/ComputerScience/assets/49386460/e8fdb9d6-0539-47d4-9a06-2721727a58f7)
- 일반적인 완전한 Spring 웹 애플리케이션 <br><br>

![image](https://github.com/ovoaaahj/ComputerScience/assets/49386460/9eb166d6-730c-467a-9e36-74daff87bca1)
-  타사 웹 프레임워크를 사용하는 Spring 중간 계층 <br><br>

![image](https://github.com/ovoaaahj/ComputerScience/assets/49386460/b44819af-3db0-4ef5-9343-e36ba843cfe4)
- 원격 사용 시나리오 <br><br>





<br><br><br>
참고 :: https://docs.spring.io/spring-framework/docs/4.0.x/spring-framework-reference/html/overview.html

