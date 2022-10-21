# Arrow Function(화살표 함수)-01

Arrow Function(화살표 함수)란?

함수를 좀더 간결하게 표현하기 위해 나온 문법.(es6)

## 형식 비교

-   기존 자바스크립트 함수 형식.

```javascript
function hello() {
    console.log("hello");
}

hello();
```

-   화살표 함수 형식.

```javascript
let hello2 = () => {
    console.log("hello");
};

hello2();
```

위 두 함수는 모두 결과가 똑같다.

## 화살표 함수의 다양한 형식

### 1. 표현식에 따른 경우

#### 1.1 표현식이 한줄인 경우 {} 생략가능

```javascript
let hello2 = () => console.log("hello");

hello2();
```

#### 1.2 표현식이 두줄이상인 경우 {} 생략불가

> {}를 생략하면 error 처리.

```javascript
let aPlus = () => {
    let a = 1;
    a++;
    console.log(a);
};

aPlus();
```

### 2. 매개변수에 따른 경우

#### 2.1 매개변수가 1개인 경우 ()생략가능

```javascript
let plus = (num) => {
    let a = num * 2;
    console.log(a);
};

plus(5);
```

#### 2.2 매개변수가 2개 이상인 경우 ()생략불가

> ()를 생략하면 error 처리.

```javascript
let plus = (num1, num2) => {
    let a = num1 * num2;
    console.log(a);
};

plus(5, 7);
```

#### 2.3 매개변수가 없는 경우 ()생략불가

```javascript
let num = () => {
    console.log(1);
};

num();
```

### 3. return에 따른 경우

#### 3.1 함수 내부에 오로지 return만 있을 경우 return과 {}생략 가능

```javascript
// let num = () => {
//   return 5;
// };

// 위의 함수와 동일하다.
let num = () => 5;

console.log(num());
```

> 2022.10.21 예시추가

```javascript
elements.map((element) => {
    return element.length;
});

// 위의 함수와 동일
elements.map((element) => element.length);
```

## 참고자료 (reference)

[화살표 함수 기본](https://ko.javascript.info/arrow-functions-basics)  
[[ES6강좌] 2강 화살표함수(Arrow Function) - 오쌤의 니가스터디](https://ossam5.tistory.com/158)  
[Arrow function expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)  
[화살표 함수](https://poiemaweb.com/es6-arrow-function)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
