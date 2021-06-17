# NPM이란?
<div align="center">
    <img src="./img/logo.png">
</div>

> npm은 **Node Packaged Manager**의 약자입니다.

직역하자면 ***노드 패키지 관리자*** 라는 뜻을 가지고 있는데요. 이렇게 들어서는 돈통 무슨 말인지 모를 것입니다.
그럼 이해를 위해서 단어를 하나씩 듣어보도록 하죠.<br><br>

먼저 Node는 여러분들도 아시는 자바스크립트 [런타임](https://github.com/songyouhyun/External-Brain/blob/master/ETC/word.md#%EB%9F%B0%ED%83%80%EC%9E%84%EC%9D%B4%EB%9E%80) 환경인 Node.js를 가리킵니다.<br>
그리고 Package는 npm에 업로드된 노드[모듈](https://github.com/songyouhyun/External-Brain/blob/master/ETC/word.md#%EB%AA%A8%EB%93%88module%EC%9D%B4%EB%9E%80)에 몇 가지 정보를 추가한 것으로,
결국 모듈이지만 조금 더 큰 단위라고 볼 수 있습니다.<br>
마지막으로 Manage는 이러한 것들을 관리해준다는 것입니다.<br>
대충 감이 오시나요?<br><br>

세상에는 많은 자바스크립트 프로그래머들이 있고, 그들이 자바스크립트를 더 편하게 사용할 수 있게 유용한 자바스크립트 모듈들을  패키지화하여서 이미 만들어 두었습니다.<br>
그리고 npm은 이러한 것들을 모아둔 저장소 역할을 하며 설치/관리를 수행할 수 있는 CLI를 제공하죠.<br><br>

npm은 세계 최대 규모의 패키지들을 보유하고 있습니다.<br>
또한 npm을 통해 자신의 프로젝트에서 사용 중인 패키지들의 버전 업데이트도 관리할 수 있습니다.<br><br>

가장 중요한 것은 결국 이 npm도 **의존성 관리 도구**의 한 종류라는 것입니다.<br>

~~(이 의존성 관리 도구에 대해서는 나중에 자세히 다루도록 하겠습니다.😅)~~

## 📌 의존성 관리 도구 종류
<B>

- Python - pip, pyenv
- Java - Maven
- React - yarn
- PHP - Composer
- Node.js - npm

## 🎮 패키치 설치 명령 옵션
|npm i 옵션|의미|단축 명령|
|:---:|---|:---:|
|--save|프로젝트를 실행할 때 필요한 패키지로 설치합니다. 패키지 정보가 package.json 파일의 'dependencies'항목에 등록됩니다.|-s|
|--save-dev|프로젝트를 개발할 때만 필요한 패키지로 설치합니다. 패키지 정보가 package.json 파일의 'devDependencies' 항목에 등록됩니다.|-d|
|--global|내 로컬 컴퓨터 전역에 필요한 패키지로 설치합니다.|-g|
