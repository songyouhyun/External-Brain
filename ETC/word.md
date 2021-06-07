### 모듈(Module)이란?
- 기본적으로 제공하는 기능들을 모아놓은 각각의 그룹들

### API(Application Programming Interface)란?
- 소프트웨어가 다른 소프트웨어로부터 지정된 형식으로 요청,명령 받을 수 있는 수단

### DBMS(DataBase Management System)란?
- 말그대로 데이터베이스를 관리하는 시스템
- 사용자와 DB사이에서 사용자의 요구에 따라 데이터를 생성해주고, DB를 관리해주는 소프트웨어
- DBMS는 데이터를 계층 또는 탐색 형식으로 저장한다. 파일 시스템을 사용해 저장하며 따라서 테이블 간에는 아무 관계 없다.

### 런타임이란?
- 프로그래밍 언어가 구동되는 환경

### 인프라란(Infrastructure)?
- 애플리케이션을 가동시키기 위해 필요한 하드웨어나 OS, 미들웨어, 네트워크 등 시스템의 기반

### 아키텍처(Architecture)란?
- 최적화를 목표로 두고 시스템 구성과 동작원리 그리고 시스템의 구성환경등을 설명 및 설계하는 청사진 또는 설계도

### 리얼 타임(Real time)이란?
- 실시간 컴퓨팅을 의미한다.
- 사용할 수 있는 자원이 한정되어 있는 상황에서 작업 수행이 요청되었을 때, 이를 제한된 시간안에 처리해 결과를 내주는 것을 말한다.

### 트리(Tree)란?
- 그래프의 일종으로, 여러 노드가 한 노드를 가리킬 수 없는 구조
- 간단하게는 회로가 없고, 서로 다른 두 노드를 잇는 길이 하나뿐인 그래프
<div align="center">

  ![image](https://user-images.githubusercontent.com/68471917/113801304-87d80500-9793-11eb-8551-98bf42812764.png)
</div>

### 해시 함수(hash function)란?
- 임의의 길이의 데이터를 고정된 길이의 데이터로 매핑하는 함수이다.
- 해시 함수에 의해 얻어지는 값은 해시 값, 해시 코드, 해시 체크섬 또는 간단하게 해시라고 한다.

### 다이제스트(digest)란?
- 수학적인 연산을 통해 원본 메세지를 변환하여 암호화된 메세지이다.

### Salt란?
- 단방향 해시 함수에서 다이제스트를 생성할 때 추가되는 바이트 단위의 임의의 문자열이다.

### OpenAPI란?
- 누구나 사용할 수 있도록 공개된 API
`e.g.) 구글 맵, 공공 데이터 등`

### 마이크로 서비스란?
- 하나의 큰 애플리케이션을 여러 개의 작은 애플리케이션으로 쪼개어 변경과 조합이 가능하도록 만든 아키텍처

### Claim이란?
- 청구하다, 주장하다, 요청하다, 요구하다 등의 뜻을 가지고 있음
- request와 전반적으로 비슷한 의미를 가짐

### 포맷(format)이란?
- 형식, 양식, 체제, 서식 등의 뜻을 가지고 있음

### TCP/IP란?
- 컴퓨터와 컴퓨터간에 데이터를 전송 할 수 있도록 하는 장치로 인터넷이라는 거대한 통신망을 통해 원하는 정보(데이터)를 주고 받는 기능을 이용하는 응용 프로토콜

### 인코딩이란?
- 정보의 형태나 형식을 변환하는 처리나 처리 방식
- 내용에는 변화가 없다
- 암호화로는 사용 불가능
- 종류로는 **ASCII , URL , HTML , Base64 , MS Script** 인코딩이 있다.

### E2E Test(End To End Test)란?
- Endpoint(종단) 간 테스트로 사용자의 입장에서 사용자가 사용하는 상황을 가정하고 테스트 하는 것을 의미

### `@`데코레이터(Decorator)란?
- 데코레이터는 클래스에 함수 기능을 추가할 수 있게 한다.

### 스크립트 언어란?
- 응용 소프트웨어를 제어하는 컴퓨터 프로그래밍 언어를 가리킨다.
- 소스 코드를 컴파일하지 않고 인터프리터로 소스 코드를 한줄한줄 읽어 바로 실행하는 방식으로 동작한다.

### CLI(Command Line Interface)란?
- 직역하자면 '명령 줄 인터페이스'라는 뜻이다.
- 텍스트 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식을 뜻한다.
- **Window**에서는 `명령 프롬프트(CMD)`를 사용하고, **Mac**이나 **Linux**에서는 `Terminal`을 사용한다.

### GUI(Graphic User Interface)란?
- 사용자가 편리하게 사용할 수 있도록 CLI창을 아이콘 따위의 그래픽으로 나타낸 것이다.
- ~~흔히들 구이라고 말한다.~~

### 사이드 이펙트(Side Effect)란?
- 요구되어지는 이펙트 이외의 다른 이펙트가 발생하는 현상
- 개발 영역에서는 버그(Bug)로 치부되기도 함
- 이러한 사이드 이펙트를 줄이기 위해서는 예측이 가능한 환경을 만들어야 함
독립성, 약한 의존성, 명시적, 접근제한자, 기능의 분리 등등으로 사이드 이펙트를 줄이면 안정성을 확보할 수 있음
- 최소한으로 발생하는 특정 위치로 한정시키는 것도 방법이다.