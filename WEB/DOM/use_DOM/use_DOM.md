## ๐ DOM์ ์ด๋ป๊ฒ ์ฌ์ฉํ ๊น?
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>๋ฌธ์๊ฐ์ฒด ๋ชจ๋ธ(DOM)</title>
        <script type="text/javascript"></script> 
    </head>
    <body>
        <h1 id="header_1">HEADER-1</h1>
        <h1 id="header_2">HEADER-2</h1>
        <hr>
    </body>
</html>
```

์ง๊ธ๋ถํฐ ์ด HTML์ฝ๋์ JavaScript๋ฅผ ํตํด์ ๋์ ์ผ๋ก ๋ฌธ์๊ฐ์ฒด๋ฅผ ์์ฑํด๋ณผ ๊ฒ์ด๋ค.
<br>
```javascript
var header = document.createElement('h2');
```
์ฐ์  document ๊ฐ์ฒด์ ์ ๊ทผํด์ `<h2>` ํ๊ทธ๋ฅผ ์์ฑํ๋ค.
<br>
```javascript
var textNode = document.createTextNode('Hello World');
```
๊ทธ ๋ค์์ document ๊ฐ์ฒด์ ์ ๊ทผํด์ TextNode๋ฅผ ์์ฑํ๊ณ  'Hello World' ๋ผ๋ String์ ๋ฃ์ด์ค๋ค.
<br>

```javascript
header.appendChild(textNode);
```
์์์ ์์ฑํ `<h2>`ํ๊ทธ์ ์์๋ธ๋๋ฅผ ์ถ๊ฐํ๊ณ  ์์ต๋๋ค.
๊ทธ๋ฐ๋ฐ ๊ทธ ์ถ๊ฐ๋๋ ์์๋ธ๋๊ฐ ์๊น ์ํด์ ์์ฑํ Text Node์ด๋ค.
<br>
```javascript
document.body.appendChild(header);
```
document๊ฐ์ฒด๋ฅผ ํตํด์ body๊ฐ์ฒด์ ์ ๊ทผํ๋ค.
๊ทธ๋ฆฌ๊ณ  body๊ฐ์ฒด์ ์์ ๋ธ๋๋ฅผ ์ถ๊ฐํ๊ณ  ์๋๋ฐ,
์ด header๊ฐ ์๊น `<h2>` ํ๊ทธ๋ฅผ ์์ฑํด์ TextNode๊น์ง ์ถ๊ฐํ๋ header์ด๋ค.
์ด๋ ๊ฒ ์ถ๊ฐํ๊ณ  ๋๋ฉด ์๋์ ๊ทธ๋ฆผ์ฒ๋ผ ๋ฌธ์๊ฐ ์ถ๊ฐ๋ ๊ฒ์ ํ์ธํ  ์ ์๋ค.
<img src="https://mblogthumb-phinf.pstatic.net/MjAxNzA0MDFfNzEg/MDAxNDkxMDQwNTUxMTcy.lIXCbVwmjy3FRsgX002tQqU60Dy31ZmEHgTU9_Uvzlwg.xo1hhRaFeu3K9qFfvFfGc1Q8dm3fKbAn8HN7EBgYTu0g.PNG.magnking/image.png?type=w800">

์ต์ข์ ์ผ๋ก JavaScript๋ฅผ ์ถ๊ฐํ ์ฝ๋์ด๋ค.
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>๋ฌธ์๊ฐ์ฒด ๋ชจ๋ธ(DOM)</title>
        <script type="text/javascript">
                //1. ๋ฌธ์ ๊ฐ์ฒด ์์ฑ
                var header = document.createElement('h2');  // h2 ํ๊ทธ ์์ฑ

                var textNode = document.createTextNode('Hello World');

                //2. ๋ธ๋(์์/ํ์คํธ)๋ฅผ ์ฐ๊ฒฐ.
                header.appendChild(textNode);

                //3. body ๋ฌธ์ ๊ฐ์ฒด์ header ๋ฌธ์ ๊ฐ์ฒด๋ฅผ ์ถ๊ฐ.
                document.body.appendChild(header);
        </script>
    </head>
    <body>
        <h1 id="header_1">HEADER-1</h1>
        <h1 id="header_2">HEADER-2</h1>
        <hr>
    </body>
</html>
```