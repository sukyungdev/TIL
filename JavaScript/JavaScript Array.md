# Javascript array

array(배열)이란?

하나의 변수에 여러개의 값을 담기 위한 자료형.

```javascript
let a = ["candy", "cake", "Chocolate"];
```

> 배열의 선언에는 다른 방법도 존재한다.

## 배열의 index(인덱스)

모든 배열의 요소(아이템)에는 변호가 부여된다.  
**요소의 시작 번호는 0이다.**  
시작번호가 1이 아니라 0이라는 것을 기억하자.

```javascript
let a = ["candy", "cake", "Chocolate"];
console.log(a[0]); // candy 출력
```

index를 이용해서 각 요소에 접근가능.

```javascript
a[0] = "strawberry";
console.log(a[0]);
```

## 배열 함수

배열을 편리하게 사용하기 위한 함수.  
[[JS] 자바스크립트 배열관련 메소드 총정리](https://velog.io/@younoah/JS-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%B0%B0%EC%97%B4%EA%B4%80%EB%A0%A8-%EB%A9%94%EC%86%8C%EB%93%9C-%EC%B4%9D%EC%A0%95%EB%A6%AC)

### .pop()

배열의 끝 요소 삭제.

```javascript
let a = ["candy", "cake", "Chocolate"];

console.log(a.pop()); //Chocolate
console.log(a); //[ 'candy', 'cake' ]
```

### .push()

배열의 끝에 요소 추가.

```javascript
let a = ["candy", "cake", "Chocolate"];

console.log(a.push("strawberry")); //4
console.log(a); //[ 'candy', 'cake', 'Chocolate', 'strawberry' ]
```

### .indcludes()

배열에 어떠한 요소가 있는지 확인해주는 함수.

```javascript
let a = ["candy", "cake", "Chocolate"];

console.log(a.includes("strawberry")); //false
console.log(a.includes("candy")); //true
```

### .indexOf()

특정 배열 요소의 인덱스를 반환하는 함수.

```javascript
let a = ["candy", "cake", "Chocolate"];

console.log(a.indexOf("cake")); //1
```

### .slice()

slice("시작인덱스", "끝인덱스").  
시작 인덱스부터 끝 인덱스까지를 **복사하여 반환하는 함수.**  
원본 배열은 변화가 없다.

```javascript
let a = ["candy", "cake", "Chocolate", "strawberry"];

console.log(a.slice(0, 2)); //[ 'candy', 'cake' ]
console.log(a); //[ 'candy', 'cake', 'Chocolate', 'strawberry' ]
```

> 끝 인덱스는 생략 가능.

### .splice()

slice("시작인덱스", "개수").  
시작 인덱스에서 개수 만큼의 요소를 제거하는 함수.  
원본 배열에 변화가 있다.

```javascript
let a = ["candy", "cake", "Chocolate", "strawberry"];

a.splice(0, 2);
console.log(a); //[ 'Chocolate', 'strawberry' ]
```  
### forEach

기존의 for문을 대체해서 사용 가능.

```javascript
let arr = [1, 2, 3, 4, 5];

// for (let i = 0; i < arr.length; i++) {
//     console.log(arr[i]);
// }

// for문과 동일한 결과
arr.forEach((item) => {
    console.log(item);
});
```

### map

원본 배열의 요소에 콜백함수를 수행한 후, 값을 리턴하는 함수.

> 새로운 배열 생성

```javascript
let arr = [1, 2, 3, 4, 5];
// let newsArr = [];

// arr.forEach((item) => {
//   newsArr.push(item * 10);
// })
// console.log(newsArr);

// 위의 코드와 동일한 결과
let newArr = arr.map((item) => {
    return item * 10;
});

console.log(newArr);
```

### includes

배열이 특정한 값과 일치한 값을 포함하고 있는지 확인하는 함수.

```javascript
let arr = [1, 2, 3, 4, 5];
let two = 2;

// arr.forEach((item) => {
//   if (item === 2){
//     console.log("true");
//   };
// });

//위의 코드와 동일한 결과
console.log(arr.includes(two));
```

### indexOf

특정한 값과 일치한 값의 인덱스를 봔환하는 함수.
값이 없는 경우에는 -1 반환.

```javascript
let arr = [1, 2, 3, 4, 5];
let two = 2;

console.log(arr.indexOf(two)); //1
```

### findIndex

배열 안의 요소가 객체나 배열일 경우, indexOf로는 인덱스를 찾을 수 없다.
그럴때 findIndex를 사용한다.

```javascript
const arr = [
    { number: 1 },
    { number: 2 },
    { number: 3 },
    { number: 4 },
    { number: 5 },
];

console.log(arr.findIndex((item) => item.number === 5));
```

### find

특정한 값의 요소 자체를 찾을 수 있다.

```javascript
const arr = [
    { number: 1 },
    { number: 2 },
    { number: 3 },
    { number: 4 },
    { number: 5 },
];

console.log(arr.find((item) => item.number === 5));
```

### filter

특정 조건을 만족하는 값들을 배열로 반환.

```javascript
const arr = [
    { number: 1, color: "white" },
    { number: 2, color: "black" },
    { number: 3, color: "blue" },
    { number: 4, color: "yellow" },
    { number: 5, color: "white" },
];

console.log(arr.filter((item) => item.color === "white"));
```

## 참고자료 (reference)

[[JavaScript] 자바스크립트 배열(Array) 생성 및 사용법 쉽게 정리](https://gent.tistory.com/294)  
[[JS] 자바스크립트 배열관련 메소드 총정리](https://velog.io/@younoah/JS-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%B0%B0%EC%97%B4%EA%B4%80%EB%A0%A8-%EB%A9%94%EC%86%8C%EB%93%9C-%EC%B4%9D%EC%A0%95%EB%A6%AC)  
[[자바스크립트 스터디]배열 내장함수](https://velog.io/@moonsemi1230/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8A%A4%ED%84%B0%EB%94%94%EB%B0%B0%EC%97%B4-%EB%82%B4%EC%9E%A5%ED%95%A8%EC%88%98)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
