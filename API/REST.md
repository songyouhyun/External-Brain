# RSET
<div align="center">
    <img src="rest.png">
</div>

## 🗣 REST의 정의
> ***Representational State Transfer***의 약자로,<br>
자원을 이름으로 구분하여 해당 자원의 상태를 주고 받는 모든 것을 의미한다.<br>

REST란 웹 상에 존재하는 다양한 자원들을 HTTP 프로토콜을 이용하여 전송하는 [인터페이스]()다.<br>
자원(이미지, 동영상, DB 자원)등 에 고유한 [URI]()를 부여해서 활용한다.<br>
<br>
우린 이 인터페이스를 이용해서 우리가 웹상에서 보는 데이터들인 자원을 주고받는다.<br>
이때 HTTP 프로토콜을 이용하니 우리(클라이언트)가 웹을 이용하며 자원을 **요청**(Request)하면 서버(Server)에서 자원을 **전달**(Response)해준다.<br>
보통 JSON 형태나 XML 형태를 이용하여 자원의 상태를 전달하게 된다.

<br>

추가적으로 REST는 [**ROP**]()(Resource Oriented Architecture)다.<br>
자원 지향 설계라고하는데 [**OOP**](),[**AOP**]()와 같이 프로그래밍 기법이 있다면, 이는 설계 기법중 하나라고 생각할 수있다.<br>
간단하게 자원들을 HTTP Method으로 처리하는 기법이다. 그렇다면 이 때 **어떤 방법**(Method)으로 자원들을 주고받을까?<br>

<div align="center">
    <img src = "http_method.png">
</div>