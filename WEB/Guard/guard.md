# Guard ๐ฐ

## ๐๐ปโโ๏ธ ๊ฐ๋์ ์ฃผ์ ๋ชฉ์ 

---

guard๋ ๋ฐ์ดํฐ๊ฐ ์ ๋๋ก ์ค๋ ค์๋์ง๋ ์ฒดํฌํ  ์ ์์ง๋ง, ๋ฐ์ดํฐ ์ฒดํฌ๋ `class-validator` ๋ก ๋์  ํ  ์ ์๊ธฐ ๋๋ฌธ์,
guard๋ ์ฃผ๋ก ์์ฒญ์ด ์ปจํธ๋กค๋ฌ์ ์ ๊ทผํ๊ธฐ ์ ์ **๊ถํ**์ด ์๋์ง๋ฅผ ํ์ธํ๋ค.

## ๐ ๊ฐ๋์ ํน์ง

---

- guard๋ ์ฃผ๋ก **๊ถํ** ๋ฐ **๋ก๊ทธ์ธ ์ฌ๋ถ**๋ฅผ ํ์ธํ๋ค.
- guard๋ **401**(Unauthorized)์ด๋ **403**(Forbidden)๊ณผ ๊ฐ์ ์๋ฌ๋ฅผ ์ฒ๋ฆฌํ๋ค.
- guard๋ **Interceptor**๋ณด๋ค ๋จผ์  ์คํ๋๋ค.
- guard์์ ๊ฑธ๋ฌ์ง๋ฉด **Exception Filter**๋ก ์ฎ๊ฒจ์ง๋ค.

## โ๏ธ Error

---

#### 401 (Unauthorized)
> ํด๋น ๋ฆฌ์์ค์ ์ ํจํ ์ธ์ฆ ์๊ฒฉ ์ฆ๋ช์ด ์๊ธฐ ๋๋ฌธ์ ์์ฒญ์ด ์ ์ฉ๋์ง ์์์์ ๋ํ๋๋๋ค.

#### 403 (Unauthorized)
์๋ฒ์ ์์ฒญ์ด ์ ๋ฌ๋์์ง๋ง, ๊ถํ ๋๋ฌธ์ ๊ฑฐ์ ๋์๋ค๋ ๊ฒ์ ์๋ฏธํฉ๋๋ค.

### ๊ทธ๋ ๋ค๋ฉด ์ด ๋์ ์ฐจ์ด์ ์? ๐คทโโ๏ธ

     401(Unauthorized)์ ๊ฒฝ์ฐ์๋ ์ธ์ฆ์ด ๊ฐ๋ฅํ์ง๋ง,
     403(Forbidden)์ ๊ฒฝ์ฐ, ๋ก๊ทธ์ธ ๋ก์ง(ํ๋ฆฐ ๋น๋ฐ๋ฒํธ๋ก ๋ก๊ทธ์ธ ํ์)์ฒ๋ผ ๋ฐ์ํ์ฌ
     ์ฌ์ธ์ฆ(re-authenticating)์ ํ๋๋ผ๋ ์ง์์ ์ผ๋ก ์ ์์ ๊ฑฐ์ ํฉ๋๋ค.