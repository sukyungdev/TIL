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

### .slice()

slice("시작인덱스", "개수").  
시작 인덱스에서 개수 만큼의 요소를 제거하는 함수.  
원본 배열에 변화가 있다.

```javascript
let a = ["candy", "cake", "Chocolate", "strawberry"];

a.splice(0, 2);
console.log(a); //[ 'Chocolate', 'strawberry' ]
```

## 참고자료 (reference)

[[JavaScript] 자바스크립트 배열(Array) 생성 및 사용법 쉽게 정리](https://gent.tistory.com/294)  
[[JS] 자바스크립트 배열관련 메소드 총정리](https://velog.io/@younoah/JS-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%B0%B0%EC%97%B4%EA%B4%80%EB%A0%A8-%EB%A9%94%EC%86%8C%EB%93%9C-%EC%B4%9D%EC%A0%95%EB%A6%AC)  
[[자바스크립트 스터디]배열 내장함수](https://velog.io/@moonsemi1230/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8A%A4%ED%84%B0%EB%94%94%EB%B0%B0%EC%97%B4-%EB%82%B4%EC%9E%A5%ED%95%A8%EC%88%98)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
