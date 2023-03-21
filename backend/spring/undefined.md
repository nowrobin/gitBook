# 용어정리

## Spring Bean&#x20;

&#x20;spring-bean: IOC container, 또는 DI 컨테이너에서 관리하는 객체를 말한다.  new ..  으로 객체를 생성 하는것이 아닌, spring 자체적인 container를 통해서 생성된다.  ApplicationContext.getBean() 매소드를  작성해서 bean(객체를 가지고 온다).

Bean 설정하는 방법 :&#x20;

XML: \<Bean> 태그를 사용해서 , 직접적으로 연결 시킴

Annotation: @Component 로 부여된 클래스를 자동으로 부여시키는 방법

Java Annotation: @Bean 어노테이션을 이용해서,  매서드에  bean을 등록시키는 방법, 실제 java코드를 작성해야되는 부분.





## Servlet&#x20;

서블릿은 서버에서 사용되는 동적 웹페이지를 만들때 사용되는 자바기반의 클래스이다.&#x20;

&#x20;클라이언트의 동작에 동적인 웹 애플리케이션을 만들어 주는 역할을 한다. &#x20;

정적인 페이지들과 비즈니스 로직을 분리하여 사용



MVC

## MVC

Model  + View + Controller =MVC pattern &#x20;

–











Reference:&#x20;

MVC: [https://medium.com/@jang.wangsu/%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4-mvc-%ED%8C%A8%ED%84%B4%EC%9D%B4%EB%9E%80-1d74fac6e256](https://medium.com/@jang.wangsu/%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4-mvc-%ED%8C%A8%ED%84%B4%EC%9D%B4%EB%9E%80-1d74fac6e256)

SpringBean: [https://melonicedlatte.com/2021/07/11/232800.html](https://melonicedlatte.com/2021/07/11/232800.html)

Servlet:&#x20;

[https://velog.io/@falling\_star3/Tomcat-%EC%84%9C%EB%B8%94%EB%A6%BFServlet%EC%9D%B4%EB%9E%80](https://velog.io/@falling\_star3/Tomcat-%EC%84%9C%EB%B8%94%EB%A6%BFServlet%EC%9D%B4%EB%9E%80)

