# 🗝 JWT
<div align="center">
    <img src="./img/cover.png">
</div>

### 1️⃣ JWT 개념
> **Json Web Token**의 약자로,
> Json 포맷을 이용하여 사용자에 대한 속성을 저장하는 [Claim]() 기반의 Web Token이다.

일반적으로 클라이언트와 서버, 서비스와 서비스 사이 통신 시 권한 인가(Authorization)를 위해 사용하는 토큰을 뜻합니다.

<br>

### 2️⃣ JWT 등장배경
일반적인 인증 로직을 보도록 합시다.

사용자가 ID, PW를 입력하고, 그 데이터가 서버로 전송이 됩니다.
서버에서는 전송받은 ID, PW를 **DB**에 조회하고 회원이면 로그인을 시켜줍니다.

그런데 문제는 여기서 생기게됩니다.
HTTP는 Stateless, 즉 사용자가 새로운 요청을 한다면 과거에 로그인한 사실을 기억하지 못합니다.
이 문제를 해결하기 위해서 예전에는 로그인 할 때 DB에 누가 로그인했는지 기록했습니다.


### 3️⃣ JWT 특징
- 

### 4️⃣ JWT 구조
<div align="center">
    <img src="./img/jwt.png">
</div>

#### 📍 HEADER(헤더)
-  헤더(Header)는 JWT를 어떻게 검증(Verify)하는가에 대한 내용을 담고 있다.
#### 📍 PAYLOAD(내용)
#### 📍 Signature(서명)