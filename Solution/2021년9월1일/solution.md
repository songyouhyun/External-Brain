# **Node.js는 Spring처럼 별도의 웹서버 소프트웨어가 필요없나요?**
Java의 프레임워크인 Spring에서는 Apache나 Tomcat등의 별도의 웹서버 소프트웨어를 이용하여 웹서버를 동작시키는 장면을 자주 보았습니다.<br>
그런데 저는 Node.js를 공부하며 한번도 웹 서버 설정을 해본 적이 없어서 딱히 필요가 없는 줄 알고 넘어갔었습니다.<br>
하지만 그냥 넘기기엔 기분이 찜찜해서 질문합니다.<br>

# 답변
우선 질문에 답하기 전에, 우리는 Apache나 Tomcat이 무엇인지부터 알아볼 필요가 있다.

Apache는 Web Server, Tomcat은 WAS(Web Application Server) 종류 중 하나이다.

이 때, Web Server와 Web Application Server의 차이점에 대해서 알아보자.

지금부터 Web Application Server는 줄임말인 WAS로 대신 말하도록 하겠다.

### Web Server와 WAS의 차이
차이점이라고 해봤자, Application이라는 단어 하나 차이다.
그리고 이 단어 하나 차이처럼, 차이점도 단어 하나 차이다.

바로 정적과 동적의 차이이다.
Web Server는 정적인 데이터를 처리하고, WAS는 동적인 데이터를 처리한다.

Web Server가 처리하는 정적인 데이터의 예로는 이미지나 단순 HTML이 있고,
WAS가 처리하는 동적인 데이터의 예로는 DB연결, 데이터 조작이 있다.

부가적으로 WAS는 Web Server + Web Container를 합친 것이다.
(주로 WAS를 서블릿 컨테이너, 웹 컨테이너 등으로 부르기도 함)

다양한 기능을 컨테이너에 구현하여 다양한 역할을 수행한다.

Node.js는 내장 HTTP 서버 라이브러리를 포함하고 있어 웹 서버에서 `Apache🪶`등의 별도의 소프트웨어 없이 동작하는 것이 가능하며 이를 통해 웹 서버의 동작에 있어 더 많은 통제를 가능케한다.
<br>

그렇다고 Node.js를 사용하면 NginX와 같은 웹 서버를 사용하지 않는 것은 아니다. 기업에서는 NginX나 Apache등의 그동안 쌓인 기술들을 활용하여 이를 **리버스 프록시 서버**로 활용하여 보안상의 이점과 캐싱등을 통해 속도상의 이점을 갖는다.