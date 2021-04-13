# 인증과 인가란?
<div align="center">
    <img src="auth.png">
</div>

## 🍎 인증(Authentication) & 인가(Authorization)
인증과 인가는 API에서 가장 많이 구현되는 기능 중 하나

### 인증(Authentication)

* 유저의 identification을 확인하는 절차, 쉽게 설명하면 유저의 Id와 Password를 확인하는 절차

* 인증을 하기 위해선 먼저 유저의 Id와 Password를 생성할 수 있는 기능이 필요하다.

#### 📍 로그인 절차
1. 유저 Id와 Password 생성
1. 유저 Password 암호화 후 DB에 저장
1. 유저가 입력한 Password 암호화 후 암호화 돼서 DB에 저장된 유저 Password와 일치여부 비교
1. 일치하면 로그인 성공
1. 로그인 성공 후 access token을 클라이언트에게 전송
1. 로그인 성공 후에는 request에 access token을 첨부해서 서버에 전송함으로써 매번 로그인 할 필요가 없도록 한다.
<br>
#### 📍 유저 Password 암호화
* 유저의 비밀번호는 꼭 암호화 해서 DB에 저장해야 한다!

* 암호화에는 단방향 해쉬 함수(one-way hash function)가 일반적으로 쓰인다.

* 단방향 해시 함수는 원본 메시지를 변환하여 암호화된 메시지인 다이제스트(digest) 를 생성한다.<br>원본 메시지를 알면 암호화된 메시지를 구하기는 쉽지만 암호화된 메시지로는 원본 메시지를 구할 수 없어서 단방향성(one-way) 이라고 한다.
