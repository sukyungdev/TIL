# Javascript Object

Object(객체)란?

자료형의 종류. 관련있는 데이터를 하나로 묶어서 표현하는 자료형.  
key(이름)과 value(값)으로 구성된 property(요소)의 집합이다.

```javascript
const a = {
  key: "value",
};
```

## 객체를 사용하면 어떤점이 좋을까?

대부분의 대상은 하나의 데이터가 아닌 여러 데이터로 이루어져 있고  
각 데이터간의 관계가 중요하다.

이러한 상황에서 객체는 데이터를 효과적으로 표현할수 있는 자료형이다.

## 객체의 선언

{}를 이용하여 선언한다.

```javascript
const user = {};
```

## 객체의 value(값) 가져오기(객체의 프로퍼티 참조)

크게 2가지 방법이 있다.

- object.keyName
- object['keyName']

```javascript
const user = {
  age: 20,
  name: "userName",
  phoneNumber: "010-0000-0000",
};

console.log(user.age); //20
console.log(user["age"]); //20
```

keyName을 이용해서 value를 불러올 수 있다.

## 객체의 프로퍼티 값(value) 재할당

key를 통해 새로운 value 선언 가능.

```javascript
const user = {
  age: 20,
  name: "userName",
  phoneNumber: "010-0000-0000",
};

user.age = 22;
console.log(user); //age의 value값이 22로 바뀐다.
```

## 추가

- 객체안에 함수가 value로 들어갈수 있다.

```javascript
const user = {
  age: 20,
  name: "userName",
  phoneNumber: "010-0000-0000",
  sayHello: function hello() {
    return "Hello!";
  },
};

console.log(user.sayHello()); //객체안에 있는 함수 호출.
```

- 객체는 배열의 요소로 들어갈수 있다.

```javascript
const user = [
  { name: "aa", age: 20 },
  { name: "bb", age: 22 },
  { name: "ab", age: 12 },
];

console.log(user);

for (let i = 0; i < user.length; i++) {
  console.log(user[i].name);
} //name의 value 호출
```

## 참고자료 (reference)

[[JavaScript] 객체(Object)의 정의와 사용법](https://velog.io/@bsjp400/JavaScript-%EA%B0%9D%EC%B2%B4Object%EB%9E%80)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
