# Javascript ES6 new feature01

Javascript ES6이란?

javascript의 두번째 개정판.(새로운 버전의 자바스크립트)  
새롭게 추가된 문법 중 자주 쓰이는 문법들을 간단히 정리.

## 객체 초기화(shorthand property)

변수명과 객체의 키값을 동일하고 하고 싶은 경우 사용 가능.

```javascript
// 기존의 방식
let name = "a";
let version = 5;

let test = {
  name: name,
  version: version,
};
console.log(test);

//ES6
let name = "a";
let version = 5;

let test = { name, version };
console.log(test);
```

## 구조분해할당(Destructuring)

배열(또는 객체)의 각각의 값을 간단하게 변수로 분해하여  
할당할수 있다.

```javascript
// 기존의 방식
let arr = [1, 2, 3];

let a = arr[0];
let b = arr[1];
let c = arr[2];

console.log(a, b, c);

//es6
let arr = [1, 2, 3];
let [a, b, c] = arr;

console.log(a, b, 3);
```

## ...(Rest destructuring)

...(Rest destructuring)이란?

배열(또는 객체)에서 ...(Rest)을 이용한 할당.

```javascript
let user = {
  name: "a",
  height: 160,
  age: 17,
};

let { name, ...rest } = user;

console.log(name); // a 출력
console.log(rest); // { height: 160, age: 17 } 출력
```

> name값을 제외한 나머지가 rest안에 들어간다.
> 특정한 값만 변수에 할당하고 싶을때 사용하면 good!

## spread

퍼뜨리다, 펼치다 라는 뜻. 배열(또는 객체)를 펼칠수 있는 문법.

```javascript
//spread 활용하기

let color01 = ["blue", "pink"];
let color02 = ["yellow", "white"];
let color03 = ["black", "green"];

let color123 = [...color01, ...color02, ...color03];
console.log(color123);
```

## Template Literal

``(벡틱)을 이용한 문자열 작성 방식.

```javascript
let name = "name";
//기존방식
console.log("안녕하세요. 제 이름은", name, "입니다.");
console.log("안녕하세요. 제 이름은 " + name + " 입니다.");
//ES6
console.log(`안녕하세요. 제 이름은 ${name} 입니다.`);
```

## 참고자료 (reference)

[Javascript ES6](https://www.w3schools.com/js/js_es6.asp)  
[07. spread 와 rest](https://learnjs.vlpt.us/useful/07-spread-and-rest.html)  
[[JavaScript / ES6] Spread와 Rest의 차이](https://seokzin.tistory.com/entry/JavaScript-ES6-Spread%EC%99%80-Rest%EC%9D%98-%EC%B0%A8%EC%9D%B4?category=695590)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
