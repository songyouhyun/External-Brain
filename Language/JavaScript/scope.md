# π­ μ€μ½ν(Scope)λ?
<div align="center">
    <img src="JS.png">
</div>

JavaScriptλ₯Ό λ°°μ°λ €κ³  νλ€λ©΄ **κΌ­ κΌ­ κΌ­ νμμ **μΌλ‘ λ°°μμΌνλ κ°λμΈ μ€μ½νμ λν΄μ μμλ³΄λ €κ³  νλ€.<br>
μ°μ , μ΄ μ€μ½νκ° λ¬΄μ¨ λ»μΈμ§ μ λλ μμμΌμ§ μ€λͺμ΄ κ°λ₯ν  κ² κ°λ€.
<br>

## TL;DRπ₯΅
> μ€μ½νμλ μ μ­ μ€μ½νμ μ§μ­ μ€μ½νλ‘ 2κ°μ§ μ’λ₯κ° μλ€.<br>
> **μ μ­ μ€μ½ν(Global Scope)** λ λ§ κ·Έλλ‘ μ μ­μ μ μΈλμ΄μμ΄ μ΄λ κ³³μμλ μ§ ν΄λΉ λ³μμ μ κ·Όν  μ μλ€λ μλ―Έμ΄κ³ ,<br>
> **μ§μ­ μ€μ½ν(Local Scope)** λ ν΄λΉ μ§μ­μμλ§ μ κ·Όν  μ μμ΄ μ§μ­μ λ²μ΄λ κ³³μμ  μ κ·Όν  μ μλ€λ μλ―Έμ΄λ€.<br>
> μ€μ½νλ₯Ό λλλ κΈ°μ€μ λΈλ‘(**`{}`**)μ΄λΌκ³  μκ°νλ©΄ μ΄ν΄νκΈ° νΈνλ€.

<br><br>

## μ΄λ€ κ²μ μ€μ½νλΌκ³  νλκ°? π§
> κ° μμλ λ³μ λ±μ μμλ€μ΄ νμ©λ μμ­μ λ³΄κ³  **μ€μ½ν(Scope)** λΌκ³  νλ€.
> β οΈ μ°Έκ³ ! μλ°μ€ν¬λ¦½νΈμμ κ°μ²΄λ ν¨μλ λͺ¨λ λ³μ(variable)λΌκ³  νλ€.

( + νμ§λ§ **μ μΈμ μμ μ λ°λΌ κ°μ΄ λ¬λΌμ§ μ μκΈ° λλ¬Έμ** λ²μλΌκ³ λ§ μκ°νλκ±΄ μννλ€)<br>
<br>

ν­μ νλ λ§μ΄μ§λ§ μ¬κΈ°κΉμ§μ μ€λͺμΌλ‘ μ΄ν΄κ° λλ€λ©΄ λΆλ½λ€.<br>
λ΄ λλ λ λ§μ μλ£μ λ μΉμ ν μ€λͺμ μνκ³ , λλμ΄ μ΄ν΄λ₯Ό μ±κ³΅νλ€.<br>
<br>
κ°μΈμ μΌλ‘ λλ κΈμ νμ€ν μμκ° μμΌλ©΄ μ΄ν΄κ° μλλ€.<br>
κ·Έλμ λλ λ μ νν μ€λͺνκΈ° μν΄μ μμλ₯Ό κ°μ Έμλ€.

```javascript
const name = "λμ μ±"

function Person(){
    const name = "λ°λ΄ν";
    console.log(name);
}
Person();               // κ²°κ³Ό κ° : λ°λ΄ν
console.log(name);      // κ²°κ³Ό κ° : λμ μ±
```

μ μ½λλ₯Ό μ΄ν΄λ³΄μ.<br>
λκ°μ΄ `name`μ΄λΌλ λ³μλ₯Ό μΆλ ₯νμλλ°, λ€λ₯Έ κ²°κ³Όκ°μ΄ λμλ€.<br>
λ μ νν λ§ν΄λ³΄μλ©΄ Personν¨μ λ°μ μλ `name`μλ κ°μ΄ λ€μ΄κ°μ§ μμλ€κ³  νλ κ² λ§μ κ²μ΄λ€.<br>
μ΄λ»κ² λ μΌμΈκ°....?π¨<br>

---
<br><br>

# μ§μ­(local)πκ³Ό μ μ­(global)π
    μλ°μ€ν¬λ¦½νΈμμ μ€μ½νλ μ§μ­μ€μ½νμ μ μ­μ€μ½νλ‘ 2κ°μ§ νμμ΄ μλ€.
## μ§μ­(local) μ€μ½ν π
λΈλ‘(`{}`)μ μμ **μ§μ­ μ€μ½ν**λΌκ³  νκ³ , μ§μ­ μ€μ½νμμ μ μΈλ κ²λ€μ **μ§μ­ λ³μ**λΌκ³  νλ€.<br>
<br>

```javascript
const name = "λμ μ±"

function Person(){
    const name = "λ°λ΄ν";
    console.log(name);  // κ²°κ³Ό κ° : λ°λ΄ν
}

console.log(name);      // κ²°κ³Ό κ° : λμ μ±
``` 
μ μμ μ½λλ‘ μλ₯Ό λ€μλ©΄,<br>
Personν¨μ μμ **μ§μ­ μ€μ½ν**μ΄κ³ , Personν¨μ λ΄μμ μ μΈλ `name`λ³μλ μ§μ­μ€μ½ν λ΄μμ μ μΈλ λ³μμ΄λ―λ‘ **μ§μ­ λ³μ**λΌκ³  ν  μ μλ€.<br>
<br>

μλ°μ€ν¬λ¦½νΈλ ν¨μλ₯Ό μ μΈνλ©΄ ν¨μλ₯Ό μ μΈν  λλ§λ€ μλ‘μ΄ μ€μ½νλ₯Ό μμ±νκ² λλ€.<br>
κ·Έλ¬λ―λ‘ ν¨μ λͺΈμ²΄μ μ μΈν λ³μλ ν΄λΉ ν¨μ λͺΈμ²΄ μμμλ§ μ κ·Όν  μ μλλ°<br>
μ΄λ, μ΄ λͺΈμ²΄ μμ λ²μλ₯Ό **ν¨μ μ€μ½ν(function-scoped)** λΌκ³  νλ€. ν¨μ μ€μ½νκ° λ°λ‘ μ§μ­ μ€μ½νμ μ μ ν μλΌκ³  ν  μ μλ€.<br>
<br>

μ§μ­ μ€μ½ν μμμ μ μΈλ μ§μ­ λ³μλ λ³μκ° μ μΈλ ν¨μ λ΄, μ§μ­ μ€μ½ν μμμλ§ μ ν¨νλ©°, ν¨μκ° μ’λ£λλ©΄ λ©λͺ¨λ¦¬μμ μ¬λΌμ§λ€.<br>

μ¦, μ§μ­ λ³μλ€μ λΈλ‘ λ°μΌλ‘ λκ°κ² λλ©΄ μμ΄μ Έλ²λ¦°λ€.

    β» ν¨μμ λ§€κ°λ³μ λν ν¨μ λ΄μμ μ μλλ μ§μ­ λ³μμ²λΌ λμνλ€.
<br><br>

## μ μ­(global) μ€μ½ν π

κ·Έλ¦¬κ³  λΈλ‘(`{}`)μ λ°μ **μ μ­ μ€μ½ν**λΌκ³  νκ³ , μ μ­ μ€μ½νμμ μ μΈλ κ²λ€μ **μ μ­ λ³μ**λΌκ³  νλ€.<br>
μ΄λ¬ν μ μ­ λ³μλ νλ‘κ·Έλ¨μ μ΄λ μμ­μμλ μ κ·Όν  μ μμΌλ©°, μΉ νμ΄μ§κ° λ«νμΌλ§ λ©λͺ¨λ¦¬μμ μ¬λΌμ§λ€.<br>
<br>

μ΄μ  μ€μ½νμ λν΄μ μμμΌλ λ€μ ν λ² μ½λλ₯Ό λ³΄λ©°, μ λ¦¬λ₯Ό ν΄λ³΄λλ‘ νμ.
```javascript
const name = "λμ μ±"       // μ μ­ μ€μ½νμμ μ μΈλ μ μ­ λ³μ

function Person(){
    const name = "λ°λ΄ν";    // ν¨μ μ€μ½ν μμμ μ μΈλ μ§μ­ λ³μ
    console.log(name);      // κ²°κ³Ό κ° : λ°λ΄ν(μ§μ­ λ³μ)
}   // μ§μ­ λ³μ λ¬΄λ€

console.log(name);          // κ²°κ³Ό κ° : λμ μ±(μ μ­ λ³μ)
```

Personν¨μ λ°μμ μΆλ ₯ν `name`λ³μμμ **"λ°λ΄ν"** μ΄ μλ **"λμ μ±"** μ΄ μ°νκ² λ μ΄μ λ μ΄μ λ μ΄ν΄κ° λ  κ±°λΌκ³  λ―Ώλλ€.
