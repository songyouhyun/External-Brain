# **🧑🏻‍💻 데이터 처리 모델**

데이터 처리 모델이란, **데이터를 받는 방식**이라고 할 수 있다.<br>
이 방식에서는 동기식 처리 모델과 비동기식 처리 모델이 존재한다.


![image](https://user-images.githubusercontent.com/68471917/112572422-7c98e700-8e2d-11eb-81f0-c3574ed806b8.png)
<br><br><br>
# 🥇동기식 처리 모델(Synchronous process model)

동기식 처리 모델은 **직렬적**으로 태스크(task)를 수행한다.<br>
즉, 태스크는 순차적으로 실행되며 어떤 작업이 수행 중이면 다음 작업은 대기하게 된다.<br>

예를 들어 서버에서 데이터를 가져와서 화면에 표시하는 작업을 수행할 때,<br>
서버에 데이터를 요청하고 데이터가 응답될 때까지 이후 태스크들은 **블로킹**(blocking, 작업 중단)된다.<br>
![https://t1.daumcdn.net/cfile/tistory/99327B375BC7D7832A](https://t1.daumcdn.net/cfile/tistory/99327B375BC7D7832A)

동기식으로 처리되는 코드는, **순차적으로 실행**된다.<br><br><br>

# 🥈비동기식 처리 모델(Asynchronous process model)

비동기식 처리 모델은 **병렬적**으로 태스크(task)를 수행한다.<br>
즉, 태스크가 종료되지 않은 상태라 하더라도 대기하지 않고 다음 태스크를 실행한다.

예를 들어 서버에서 데이터를 가져와서 화면에 표시하는 태스크를 수행할 때,<br>
서버에 데이터를 요청한 이후 서버로부터 데이터가 응답될 때까지 대기하지 않고 즉시 다음 태스크를 수행한다.<br>

이후 서버로부터 데이터가 응답되면 이벤트가 발생하고 이벤트 핸들러가 데이터를 가지고 수행할 태스크를 계속해 수행한다.

자바스크립트의 대부분의 DOM 이벤트와 Timer 함수(setTimeout, setInterval),<br>
Ajax 요청은 비동기식 처리 모델로 동작한다.

![https://t1.daumcdn.net/cfile/tistory/99194A365BC7D8223C](https://t1.daumcdn.net/cfile/tistory/99194A365BC7D8223C)
<br>비동기식으로 처리되는 코드는, **순차적으로 실행되지 않는다.**
<br><br>

