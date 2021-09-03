# 📌 컴파일러(Compiler)와 인터프리터(Interpreter)란 무엇인가?
우선 모든 프로그래밍 언어는 컴파일러언어와 인터프리터언어로 나눌 수 있다.

**컴파일러**와 **인터프리터** 모두 하는 역할은 같다.
고급언어로 작성된 소스 코드를 기계가 이해할 수 있는 기계어로 번역하는 프로그램이다.


## 🔥 컴파일러(Compiler)
먼저 원시 프로그램(Source Program)이란 C언어, JAVA 등 프로그래밍 언어, 즉 고급 언어로 작성된 파일을 말한다.<br>
<br>
이 원시 프로그램은 고급 언어로 작성되어 있기 때문에 컴퓨터가 바로 이해할 수 없으며 따라서 실행할 수도 없다.<br>
컴퓨터는 오로지 이진수로 된 기계어밖에 알아듣지 못하기 때문이다.<br>
<br>
그래서 소스 코드를 컴퓨터에 이해할 수 있는 기계어코드로 번역해야하는데, 이 동작을 컴파일(Compile)이라고 한다.<br>
컴파일이란 소스에 작성된 명령어들을 컴퓨터 언어인 기계어로 번역하는 작업이며, 컴파일을 하는 프로그램을 **컴파일러**라고 부른다.<br>
<br>
그리고 이 컴파일을 실행할 때 목적 프로그램이란 것을 생성하게 되는데,<br>
목적 프로그램이란 원시 프로그램(Source Program)이 언어 번역기에 의해 기계어로 번역 된 상태의 프로그램을 말한다.<br>
<br>
런타임 상황에서는 이 목적 프로그램 안에 이미 기계어로 모든 소스코드가 변환되어 있기 때문에 빠르게 실행할 수 있다.
```
정보!
컴파일러는 무조건 기계어로 번역을 할 필요는 없다.
정확한 컴파일의 뜻은 컴파일이란 어떤 언어의 코드를 다른 언어로 바꿔주는 과정으로
예를 들어 자바에서 C언어로 번역하는 프로그램도 컴파일러다.
```


## 🤖 인터프리터(Interpreter)
인터프리터 언어는 소스 코드(프로그래머가 작성한 소스코드)를 기계어로 변환하는 과정없이 한줄 한줄 해석하여 바로 명령어를 실행하는 언어를 말한다.<br>
<br>
위 컴파일러에서 언급했듯, 인터프리터는 한줄 한줄 해석과 실행을 동시에 하기 때문에 목적 프로그램을 생성하지 않는다.<br>
<br>
그리고 런타임 상황에서 인터프리터는 목적 프로그램을 생성하지 않기 때문에 실행 속도가 느리다.
<br><br>

## 🙋🏻‍♂️ : 언뜻보기에는 컴파일러가 인터프리터보다 실행 속도가 빠르기 때문에 좋아보이는데, 그럼에도 불구하고 인터프리터도 사용하는 이유가 무엇인가요?

컴파일러는 플랫폼, 즉 하드웨어에 종속적이지만, 인터프리터는 모든 플랫폼에 종속되지 않는 특징이 있기 때문이다.<br><br>
전 세계에는 수많은 CPU가 존재한다.<br>
이들 중에서는 서로 호환이 되는 CPU가 있을 것이고 그렇지 않은 CPU도 존재할 것이다.<br><br>
예를 들어 호환되지 않은 두 CPU가 있다고 가정을 해보자.<br>
한 CPU에서 돌아가는 프로그램을 만들고 컴파일러를 통해 실행파일을 만들고 이를 또 다른 CPU에서 실행시키면 실행이 되지 않는다.<br><br>
하지만 인터프리터는 해당 프로그램을 번역하는 플랫폼의 환경에 맞게 변환을 하기 때문에 잘 작동할 것이다.<br>

## 컴파일러와 인터프리터 차이점

||컴파일러|인터프리터|
|-----|:-----:|:-----:|
|번역단위|전체|한 행(줄)|
|목적 프로그램|⭕️|❌|
|실행속도|빠름|느림|
|번역속도|느림|빠름|
|언어|C,JAVA|Python,Ruby|