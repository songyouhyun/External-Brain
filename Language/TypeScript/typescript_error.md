# ⚠️ TypeScript 2.7 이상 버전에서 나는 에러 [TS2564]
TS2564 : `Property '' has no initializer and is not definitely assigned in the constructor.`

<details>
<summary>해석</summary>
<div markdown="1">

`''속성에는 이니셜 라이저가 없으며 생성자에 확실히 할당되지 않았습니다.`

</div>
</details>
<br>

위 오류는 2.7.2에부터 도입된 strict class checking으로 인한 오류이다.
> TypeScript 2.7에는 --strictPropertyInitialization이라는 새 플래그가 도입되었다.<br>
> 이 플래그는 클래스의 각 인스턴스 속성이 생성자 본문 또는 속성 이니셜 라이저에서 초기화되는지 확인하는 검사를 수행한다.<br>
> 출처 : [TypeScript 공식 문서](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-7.html)

위 말을 보고 한번에 이해가 된다면 부럽다.<br>
<br>
나는 이해가 되지 않아 더 많은 자료를 찾아보았다.<br>
그리고 내가 이해한 오류에 대한 설명을 써보려고 한다.<br>
<br>
tsconfig.json에 보면 컴파일러 옵션에 `--strictPropertyInitialization`옵션이 켜진 상태인걸 볼 수 있다.<br><br>
이 옵션은 직역하자면 `엄격한 속성 초기화` 라는 뜻인데,<br>
이 옵션이 켜진 환경에선 undefined를 포함하지 않는 클래스 속성이 반드시 속성 선언 또는 생성자, 두 장소 중 한 곳에서 초기화 되어야 한다.<br><br>
말 그대로 엄격하다😱😨😰<br>
<br>
생성자와 속성 선언 두 곳 모두에서 초기화되지 않는 경우 속성 값이 undefined 일 가능성이 존재하게 되고,<br>
따라서 타입스크립트는 그 정보가 타입에 포함되어 있지 않다면 타입 에러를 낸다.<br>
예를 들자면 이렇다.<br><br>

```TypeScript
class User{
    private password: string;
}
// error TS2564: Property 'password' has no initializer and is not definitely assigned in the constructor.
```
password는 속성 선언에서도, 생성자에서도 초기화되지 않고 있으므로 접근되는 시점에 undefined 일 수 있다.<br>
이 값은 string 타입이 아니므로 타입 에러가 발생하는 것이 당연하다.
<br>

# 📕 해결책 1
**tsconfig.json에 아래 명렁어를 추가**
```json
{
    "compilerOptions" : {
    ...
    "strictPropertyInitialization" : false
    }
}
```
    
사실 난 이 해결책보다는 아래의 해결책을 추천한다.
<br>

# 📗 해결책 2
**선택 속성 또는 확정적 할당 단언을 제공**
```TypeScript
class User {
    // 실제 상황을 정확히 반영하기 위해 password을 선택 속성으로 선언한다.
    private password?: string;
    // or
    private password2: string | undefined;
}
```
password가 undefined여서 생기는 에러가 아니라고 확신한다면, 속성 이름 뒤에 뱅 기호(!)를 붙여 확정적 할당 단언을 제공할 수 있다.<br><br>
즉 `password: T`를 `password!: T`로 변경한다. 이 경우 컴파일러는 password의 초기화 체크를 건너뛴다.
<br>

# 📘 해결책 3
플래그를 설정하고, 코드를 바꾸는 것으로 충분하지 않은 경우 일시적 TypeScript의 버전을 2.6으로 다운그레이드 하고 오류가 지속되는지 확인바랍니당.
