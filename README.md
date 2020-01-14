# Java-

<h3>Spring MVC Framework</h3>
 정의 :  스프링에서 제공하는 트랜잭션 처리, DI, AOP를 손쉽게 사용이 가능한 프레임워크인 모델 2방식 구조이다. 
   ※ 모델2 구조인 MVC 구조는 Model, View, Controller로 웹 개발 구조를 3가지로 나눠놓은 것이다.
   
 - Model : 애플리캐이션의 상태(data)를 나타내며 일반적으로 POJO로 구성된다.
           ※ POJO : Plain Old Java Object 방식으로 쉽게 말해 특정 '기술'에 종속되어 동작하는 것이 아닌 순수한 자바 객체로 이뤄졌다고 보면 된다.
 
 - View : 디스플레이 데이터 또는 Model data의 렌더링을 담당하는 HTML ouput --> JSP, Thymeleaf, Groovy, react  등등 
 
 - Controller : 요청을 처리하는 부분으로 뷰와 모델 사이의 통신 역할을 한다.
 
 종합해보면 MVC 모델의 처리 흐름은 '특정 요청 -> 컨트롤러 -> 모델 -> 컨트롤러 -> 뷰' 이렇게 진행이 된다고 생각하면 된다. 
 
Spring Framework가 제공하는 Class
 - DispatcherServlet : 사용자의 요청을 받는 Servlet 클래스
 - HandlerMapping : 사용자의 요청을 처리할 Controller를 찾는다 ex) @RequestMapping('/url')
 - ViewResolver : Controller가 반환한 값들을 가지고 View Object를 반환한다.


DispatcherServlet 설정
 - 기본적으로 /WEB-INF/디렉터리/000-servlet.xml 파일로부터 스프링 설정 정보를 읽어옴 
   --> 현재 회사에서 사용하는 설정 기준 '/WEB-INF/spring/appServlet/servlet-context.xml
 - 한개 이상 또는 다른 이름의 설정 파일을 사용할 경우 contextConfigLocation에 설정 파일 목록을 지정
   --> 현재 회사에서 사용하는 설정 기준 '/WEB-INF/spring/myBatis/mybatis-context.xml'로 마이바티스 설정을 따로 분리해서 관리
   
 
