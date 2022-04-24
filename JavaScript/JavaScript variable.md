# Javascript variable

자바스크립트에는 변수는 선언하는 3가지 방법이 있다.

- const
- let
- var

## const

상수(변하는 않는 수)를 선언할 때 사용.

- 재할당 불가능.

```javascript
const a = 5;
console.log(5);
a = 10; //TypeError: Assignment to constant variable.
```

- 블록 레벨 스코프 (코드 블록 안에서 선언된 변수는 지역 변수).
- 중복 선언 불가.
- **호이스팅이 발생하지 않는 것처럼 보인다.**

## let, var

변수를 선언할 때 사용.

## let과 var의 차이?

var이 먼저 나온 변수 선언 방식.

### var

- 재할당 가능.

- 중복 선언 가능.

```javascript
var a = 5;
var a = 10;
console.log(a);
```

> 위의 코드가 에러없이 동작한다.

- 함수 레벨 스코프 (함수 내부의 변수를 제외하고는 모두 전역변수).

```javascript
for (var i = 1; i < 5; i++) {
  console.log(i);
}

var b = i + 1;
console.log(b);
```

- 호이스팅의 대상.

```javascript
console.log(a);
var a = 5;
```

### let

- 재할당 가능.

- 중복 선언 불가.

```javascript
let a = 5;
let a = 10; //SyntaxError: Identifier 'a' has already been declared
```

- 블록 레벨 스코프 (코드 블록 안에서 선언된 변수는 지역 변수).

```javascript
for (let i = 1; i < 5; i++) {
  console.log(i);
}

let b = i + 1; //ReferenceError: i is not defined
```

- **호이스팅이 발생하지 않는 것처럼 보인다.**
  > 실제로는 호이스팅이 발생하나, 값을 참조하지 못해서(TDZ)  
  > 호이스팅이 일어나지 않는 것처럼 보인다.

```javascript
console.log(a); //ReferenceError: Cannot access 'a' before initialization
let a = 5;
```

## 참고자료 (reference)

[[자바스크립트] 변수 선언 방식 차이: var / let / const](https://curryyou.tistory.com/192)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
