# ์ฟ ํค๐ช(Cookie)์ ์ธ์๐(Session)
์ฟ ํค์ ์ธ์์ HTTP์ ํน์ง์ธ **Stateless**(๋ฌด์ํ), ์ฆ ์ํ๋ฅผ ๊ธฐ์ตํ์ง ๋ชปํ๋ ํด๋ผ์ด์ธํธ ๋๋ฌธ์ ์ํ๋ฅผ ๊ธฐ์ตํ๊ธฐ ์ํด ๋์์ต๋๋ค.<br><br>
์ํ๋ฅผ ๊ธฐ์ตํ์ง ๋ชปํ์ฌ ์ ๋ณด๊ฐ ์ ์ง๋์ง ์๊ฒ๋๋ฉด ๋งค๋ฒ ํ์ด์ง๋ฅผ ์ด๋ํ  ๋๋ง๋ค ๋ก๊ทธ์ธ์ ๋ค์ ํ๊ฑฐ๋,<br>
์ํ์ ์ ํํ๋๋ฐ ๊ตฌ๋งค ํ์ด์ง์์ ์ ํํ ์ํ์ ์ ๋ณด๊ฐ ์๊ฑฐ๋ ํ๋ ๋ฑ์ ์ผ์ด ๋ฐ์ํ  ์ ์์ฃ .
## ์ฟ ํค๋โ
> **์๋ฒ๊ฐ ํด๋ผ์ด์ธํธ(๋ธ๋ผ์ฐ์ )์ ๋ก์ปฌ์ ๋ณด๋ด์ด ์๋ฒ์ ๋ถ๊ฐ์ ์ธ ์์ฒญ์ด ์์ ๋, ๋ค์ ์๋ฒ๋ก ๋ณด๋ด์ฃผ๋ ๋ฌธ์์ด ์ ๋ณด์๋๋ค.**

<br>

## ๐ ์ฟ ํค ๊ตฌ์ฑ ์์
* **์ด๋ฆ**(Key) : ๊ฐ๊ฐ์ ์ฟ ํค๋ฅผ ๊ตฌ๋ณํ๋ ๋ฐ ์ฌ์ฉ๋๋ ์ด๋ฆ
* **๊ฐ**(Value) : ์ฟ ํค๊ฐ ๊ฐ๊ณ  ์๋ ๊ฐ
* **์ ํจ์๊ฐ** : ์ฟ ํค์ ์ ์ง์๊ฐ
* **๋๋ฉ์ธ** : ์ฟ ํค๋ฅผ ์ ์กํ  ๋๋ฉ์ธ
* **๊ฒฝ๋ก** : ์ฟ ํค๋ฅผ ์ ์กํ  ์์ฒญ ๊ฒฝ๋ก

## ๐ญ ์ฟ ํค ๋์ ์๋ฆฌ
<div class="center">
    <img src="./img/Cookie.png">
</div>

1. ํด๋ผ์ด์ธํธ๊ฐ ํ์ด์ง๋ฅผ **์์ฒญ**ํ๋ค.(์ฌ์ฉ์๊ฐ ์นํ์ด์ง์ ์ ๊ทผ)
2. ์น ์๋ฒ๋ ์ฟ ํค๋ฅผ ์์ฑํ๋ค.
3. HTTP header์ ์ฟ ํค๋ฅผ ๋ฃ์ด **์๋ต**ํ๋ค.
4. ๋๊ฒจ๋ฐ์ ์ฟ ํค๋ ํด๋ผ์ด์ธํธ๊ฐ ๊ฐ์ง๊ณ  ์๋ค๊ฐ ๋ก์ปฌ pc์ ์ ์ฅ<br>
(๋ค์ ์๋ฒ์ ์์ฒญํ  ๋ ์์ฒญ๊ณผ ํจ๊ป ์ฟ ํค๋ฅผ ์ ์กํ๋ค.)
5. ๋ธ๋ผ์ฐ์ ๊ฐ ์ข๋ฃ๋์ด๋ **์ฟ ํค ๋ง๋ฃ ๊ธฐ๊ฐ**์ด ๋จ์ ์๋ค๋ฉด ํด๋ผ์ด์ธํธ์์ ๋ณด๊ด<br>
(์ฟ ํค ๋ง๋ฃ ๊ธฐ๊ฐ์ ์ต์์ ํตํด ์ค์ ํ  ์ ์์ต๋๋ค.)
6. ๋์ผ ์ฌ์ดํธ ์ฌ๋ฐฉ๋ฌธ์ ํด๋ผ์ด์ธํธ์ PC์ ํด๋น ์ฟ ํค๊ฐ ์๋ ๊ฒฝ์ฐ, ์์ฒญ ํ์ด์ง์ ํจ๊ป ์ฟ ํค๋ฅผ ์ ์กํ๋ค.
<br>

## ๐ถ ์ฟ ํค์ ํน์ง
<br>

* ๋ฐ์ดํฐ ํํ๋ Key,Valueํํ๋ก String ๋ฌธ์ด๋ฉฐ, 4KB์ด์ ์ ์ฅ์ด ๋ถ๊ฐํฉ๋๋ค.
* ๋ธ๋ผ์ฐ์ ๋ง๋ค ์ ์ฅ๋๋ ์ฟ ํค๋ ๋ค๋ฆ๋๋ค. ์๋ฒ์์๋ ๋ธ๋ผ์ฐ์ ๊ฐ ๋ค๋ฅด๋ฉด **๋ค๋ฅธ ์ฌ์ฉ์**๋ก ์ธ์ํฉ๋๋ค.<br>
`(ํฌ๋กฌ์ผ๋ก ๋จ๊ธด ์ฟ ํค๋ ์ธํฐ๋ท ์ต์คํ๋ก์ด์์ ์ฌ์ฉํ  ์ ์์ต๋๋ค.)`
* ์ฟ ํค๋ ์๋ฒ๋ฅผ ๋์ ํด์ ์ด๋ฌํ ์ ๋ณด๋ค์ ์น ๋ธ๋ผ์ฐ์ ์ ์ ์ฅํด์ค๋๋ค. ๊ทธ๋ฆฌ๊ณ  ์ฌ์ฉ์๊ฐ ์์ฒญ์ ํ  ๋ ๊ทธ ์ ๋ณด๋ฅผ ํจ๊ป ๋ณด๋ด์ ์๋ฒ๊ฐ ์ฌ์ฉ์๋ฅผ ์๋ณํ  ์ ์๊ฒ ํด์ค๋๋ค.
* ๋ธ๋ผ์ฐ์ ์ ์ ์ฅ๋๊ธฐ๋๋ฌธ์ ์์๋ก ๊ณ ์น๊ฑฐ๋ ์ง์ธ ์ ์๊ณ , ๊ฐ๋ก์ฑ๊ธฐ๋ ์ฌ์ ๋ณด์์ด ์ทจ์ฝํฉ๋๋ค.
<br>

---
## ์ธ์์ด๋โ
> **์ผ์  ์๊ฐ๋์ ๊ฐ์ ํด๋ผ์ด์ธํธ(์ ํํ๊ฒ ๋ธ๋ผ์ฐ์ ๋ฅผ ๋งํ๋ค)๋ก ๋ถํฐ ๋ค์ด์ค๋
์ผ๋ จ์ ์๊ตฌ๋ฅผ ํ๋์ ์ํ๋ก ๋ณด๊ณ  ๊ทธ ์ํ๋ฅผ ์ผ์ ํ๊ฒ ์ ์ง์ํค๋ ๊ธฐ์ **์๋๋ค.
<br>

๋ํ ์ฌ๊ธฐ์ ์ผ์  ์๊ฐ์ด๋ ํด๋ผ์ด์ธํธ๊ฐ ์น ๋ธ๋ผ์ฐ์ ๋ฅผ ํตํด ์น ์๋ฒ์ ์ ์ํ ์์ ์ผ๋ก๋ถํฐ ์น ๋ธ๋ผ์ฐ์ ๋ฅผ ์ข๋ฃํจ์ผ๋ก์จ ์ฐ๊ฒฐ์ ๋๋ด๋ ์์ ์ ๋งํ๋ฉฐ<br>
์ฆ, ํด๋ผ์ด์ธํธ๊ฐ ์น์๋ฒ์ ์ ์ํด ์๋ ์ํ๋ฅผ ํ๋์ ๋จ์๋ก ๋ณด๊ณ  **์ธ์**์ด๋ผ๊ณ  ์นญํ๋ค๋ ๊ฒ์ด์ฃ .<br>

์ด ์ธ์์ด๋ผ๋ ๊ฒ๋ ์ฟ ํค๋ฅผ ๊ธฐ๋ฐ์ผ๋ก ๋์จ ๊ฒ์ผ๋ก,
์ฟ ํค์ ์ธ์์์ด๋๋ฅผ ์ค์ด์ ์๋ตํ  ๋ ํจ๊ป ์ ๋ฌ๋ฉ๋๋ค.
<br><br>

## ๐ญ ์ธ์ ๋์ ์๋ฆฌ
<div class="center">
    <img src="./img/Session.png">
</div>

1. ํด๋ผ์ด์ธํธ๊ฐ ํ์ด์ง๋ฅผ ์์ฒญํ๋ค.(์ฌ์ฉ์๊ฐ ์น์ฌ์ดํธ ์ ๊ทผ)

2. ์๋ฒ๋ ์ ๊ทผํ ํด๋ผ์ด์ธํธ์ Request-Header ํ๋์ ์๋ Cookie๋ฅผ ํ์ธํ์ฌ,
ํด๋ผ์ด์ธํธ๊ฐ ํด๋น session-id๋ฅผ ๋ณด๋๋์ง ํ์ธํ๋ค.

3. session-id๊ฐ ์กด์ฌํ์ง ์๋๋ค๋ฉด, ์๋ฒ๋ session-id๋ฅผ ์์ฑํด ํด๋ผ์ด์ธํธ์๊ฒ ๋๋ ค์ค๋ค.

4. ์๋ฒ์์ ํด๋ผ์ด์ธํธ๋ก ๋๋ ค์ค session-id๋ฅผ ์ฟ ํค๋ฅผ ์ฌ์ฉํด ์๋ฒ์ ์ ์ฅํ๋ค.

5. ํด๋ผ์ด์ธํธ๋ ์ฌ์ ์ ์, ์ด ์ฟ ํค๋ฅผ ์ด์ฉํ์ฌ session-id ๊ฐ์ ์๋ฒ์ ์ ๋ฌํ๋ค.

<br>

## ๐ถ ์ธ์์ ํน์ง
* ์ ๋ณด๋ค์ ์๋ฒ์ ์ ์ฅํ๊ธฐ ๋๋ฌธ์ ๋ณด์์ฑ์ด ์ฟ ํค๋ณด๋ค ์ฐ์ํฉ๋๋ค.
* ์ธ์ ์์ด๋๋ ์น ๋ธ๋ผ์ฐ์  ๋น 1๊ฐ์ฉ ์์ฑ๋์ด ๊ฐ ํด๋ผ์ด์ธํธ์๊ฒ ๊ณ ์  ID๋ฅผ ๋ถ์ฌํฉ๋๋ค.
* ์น ์ปจํ์ด๋์ ์ ์ฅ๋๋ฉฐ ๋ธ๋ผ์ฐ์  ์ข๋ฃ์ ์๋ฉธ๋๋ค.
* ๋ก๊ทธ์ธํ ์ฌ์ฉ์์ ๋ํด์๋ง ์ธ์์ ์์ฑํ๋ ๊ฒ์ด ์๋๋ผ, ๋ก๊ทธ์์ํ๋ฉด ์๋ก์ด ์ฌ์ฉ์๋ก ์ธ์ํด์ ์๋ก์ด ์ธ์์ด ์์ฑ๋ฉ๋๋ค.
* ์๋ฒ์์๋ ํด๋ผ์ด์ธํธ๋ฅผ ๊ตฌ๋ถํ๊ธฐ ์ํด ์ธ์ ID๋ฅผ ๋ถ์ฌํ๋ฉฐ ์น ๋ธ๋ผ์ฐ์ ๊ฐ ์๋ฒ์ ์ ์ํด์ ๋ธ๋ผ์ฐ์ ๋ฅผ ์ข๋ฃํ  ๋๊น์ง ์ธ์ฆ์ํ๋ฅผ ์ ์งํ๋ค.
* ์ธ์ ID๋ก ํด๋ผ์ด์ธํธ๋ฅผ ๊ตฌ๋ถํด ํด๋ผ์ด์ธํธ์ ์๊ตฌ์ ๋ง๋ ์๋น์ค๋ฅผ ์ ๊ณตํ๋ค.
* ๋ณด์ ๋ฉด์์ ์ฟ ํค๋ณด๋ค ์ฐ์ํ์ง๋ง ์ฌ์ฉ์๊ฐ ๋ง์์ง์๋ก ์๋ฒ ๋ฉ๋ชจ๋ฆฌ๋ฅผ ๋ง์ด ์ฐจ์งํ๊ฒ ๋๋๋ฐ, ์ด๋ ์๋ฒ ๋ถํ๋ฅผ ์ผ์ผํด

## ๐ช ์ฟ ํค์ ์ธ์ ์ฐจ์ด์ (์ ๋ฆฌ)

|์ ๋ชฉ|Cookie|Session|
|------|---|---|
|์ ์ฅ์์น|ํด๋ผ์ด์ธํธ|์๋ฒ|
|์ ์ฅํ์|text|Object|
|๋ฆฌ์์ค|ํด๋ผ์ด์ธํธ์ ๋ฆฌ์์ค|์๋ฒ์ ๋ฆฌ์์ค|
|์ฉ๋์ ํ|๋๋ฉ์ธ๋น 20๊ฐ, 1์ฟ ํค๋น 4KB|์ ํ์์|
|๋ง๋ฃ์์ |์ฟ ํค ์ ์ฅ์ ์ค์ <br>(์ค์  ์์ ์ ๋ธ๋ผ์ฐ์  ์ข๋ฃ์ ๋ง๋ฃ)|์๋ฒ์์ ์ฐ๊ฒฐ์ด ๋์ด์ง ๋|
