# How to install PostgreSQL ๐
> ๋ณธ ๊ธ์ MacOS์์ ์ค์นํ๊ณ  ์์ผ๋ฉฐ, [Homebrew](https://brew.sh/index_ko)๋ผ๋ ํจํค์ง ๊ด๋ฆฌ์๋ฅผ ์ฌ์ฉํ์ฌ installํฉ๋๋ค.

<br>

## PostgreSQL install

```shell
$ brew search postgresql
```
๋จผ์ , **hombrew๐บ** ์ `postgresql` ํจํค์ง๊ฐ ์๋์ง๋ถํฐ ํ์ธํ๋ค.

<img src="./img/postgresql_search.png">

๋ฒ์ ์ ๋ค์ ์ ์ง ์๊ณ  postgresql์ด๋ผ๊ณ  ์๋ ฅํ๋ฉด default๊ฐ์ผ๋ก ๊ฐ์ฅ ์ต์  ๋ฒ์ ์ ํจํค์ง๊ฐ ์ค์น๋๋ค.

```shell
brew install postgresql
```
<br>

## Install confirm
```
postgres --version
```
ํน์
```
postgres -V
```
์ค์น๊ฐ ์ ์์ ์ด๋ผ๋ฉด ์ ๋ช๋ น์ด๋ฅผ ํตํด `postgresql`๊ฐ ์ ์ค์น๋์๋์ง์ ์ด๋ค ๋ฒ์ ์ด ์ค์น๋์๋์ง ํ์ธํ  ์ ์๋ค.

<img src="./img/postgresql_version.png">
<br>

## Postgresql Start
์ค์น๋๊ฒ ํ์ธ์ด ๋์๋ค๊ณ  ํด์, ๋ฌดํฑ๋๊ณ  DB๋ช๋ น์ด๋ฅผ ์๋ ฅํ๋ฉด ์๋ฌ๊ฐ ๋  ๊ฒ์ด๋ค.
postgresql์ server๋ฅผ ์ผ์ผํ๋ค.

```
brew services start postgresql
```

<img src="./img/postgresql_start.png">

<br>

server๋ฅผ ๋๋ ๋ช๋ น์ด๋ ์ด ๋ฐ๋์ด๋ค.
```
brew services stop postgresql
```
