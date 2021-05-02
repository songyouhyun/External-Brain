## 🔎 DOM은 어떻게 사용할까?
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>문서객체 모델(DOM)</title>
        <script type="text/javascript"></script> 
    </head>
    <body>
        <h1 id="header_1">HEADER-1</h1>
        <h1 id="header_2">HEADER-2</h1>
        <hr>
    </body>
</html>
```

지금부터 이 HTML코드에 JavaScript를 통해서 동적으로 문서객체를 생성해볼 것이다.
<br>
```javascript
var header = document.createElement('h2');
```
우선 document 객체에 접근해서 `<h2>` 태그를 생성한다.
<br>
```javascript
var textNode = document.createTextNode('Hello World');
```
그 다음은 document 객체에 접근해서 TextNode를 생성하고 'Hello World' 라는 String을 넣어준다.
<br>

```javascript
header.appendChild(textNode);
```
위에서 생성한 `<h2>`태그에 자식노드를 추가하고 있습니다.
그런데 그 추가되는 자식노드가 아까 위해서 생성한 Text Node이다.
<br>
```javascript
document.body.appendChild(header);
```
document객체를 통해서 body객체에 접근한다.
그리고 body객체에 자식 노드를 추가하고 있는데,
이 header가 아까 `<h2>` 태그를 생성해서 TextNode까지 추가했던 header이다.
이렇게 추가하고 나면 아래의 그림처럼 문자가 추가된 것을 확인할 수 있다.
<img src="https://mblogthumb-phinf.pstatic.net/MjAxNzA0MDFfNzEg/MDAxNDkxMDQwNTUxMTcy.lIXCbVwmjy3FRsgX002tQqU60Dy31ZmEHgTU9_Uvzlwg.xo1hhRaFeu3K9qFfvFfGc1Q8dm3fKbAn8HN7EBgYTu0g.PNG.magnking/image.png?type=w800">

최종적으로 JavaScript를 추가한 코드이다.
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>문서객체 모델(DOM)</title>
        <script type="text/javascript">
                //1. 문서 객체 생성
                var header = document.createElement('h2');  // h2 태그 생성

                var textNode = document.createTextNode('Hello World');

                //2. 노드(요소/텍스트)를 연결.
                header.appendChild(textNode);

                //3. body 문서 객체에 header 문서 객체를 추가.
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