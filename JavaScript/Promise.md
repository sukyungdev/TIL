# Promise

Promise에 관한 간단 정리.

## Promise란?

비동기를 간단하게 처리하기 위해 사용되는 객체.

- 비동기란?
  [동기 비동기 / Blocking 과 Non-Blocking](https://sukyungdev.github.io/posts/Post-21/)

```
프로미스는 Promise 생성자 함수를 통해 인스턴스화한다.
Promise 생성자 함수는 비동기 작업을 수행할 콜백 함수를 인자로 전달받는데
이 콜백 함수는 resolve와 reject 함수를 인자로 전달받는다.

- 모던 자바스크립트 -
```

```javascript
// Promise 객체의 생성
const promise = new Promise((resolve, reject) => {});
```

> Promise를 생성하면 콜백함수가 바로 실행된다.

```javascript
const promise = new Promise((resolve, reject) => {
  console.log('Promise');
});
```

## Promise의 상태

Promise는 비동기 처리의 성공/실패 상태 값을 갖는다.

- Pending(대기) : 초기 상태
- Fulfilled(실행) : 성공적으로 실행된 상태
- Reject(실패) : 실패 상태

```javascript
// Promise 객체의 생성
const promise = new Promise((resolve, reject) => {
  // 비동기 작업을 수행한다.

  if (/* 비동기 작업 수행 성공 */) {
    resolve('result');
  }
  else { /* 비동기 작업 수행 실패 */
    reject('failure reason');
  }
});
```

비동기 작업이 성공하면 resolve(fulfilled 상태), 실패하면 reject(rejected 상태)함수를 호출한다.

```
비동기 처리에 성공하면 resolve 메소드를 호출한다.
이때 resolve 메소드의 인자로 비동기 처리 결과를 전달한다.
이 처리 결과는 Promise 객체의 후속 처리 메소드로 전달된다.
만약 비동기 처리에 실패하면 reject 메소드를 호출한다.
이때 reject 메소드의 인자로 에러 메시지를 전달한다.
이 에러 메시지는 Promise 객체의 후속 처리 메소드로 전달된다.

- 모던 자바스크립트 -
```

## Promise의 후속 처리 메소드

프로미스로 구현된 비동기 함수를 호출하는 측에서는  
프로미스 객체의 후속 처리 메소드(then, catch, finally)를 통해  
비동기 처리 결과와 에러 메세지를 전달받아 처리한다.

- then(성공) : 반환값을 처리(두 번째 콜백 함수는 실패(rejected)일때 실행)
- catch(실패) : 에러 처리
- finally : 성공/실패 여부와 상관없이 무조건 실행

> 에러처리는 명확한 가독성과 첫 번째 콜백함수에서의 에러 처리를 위해 then 보다 catch를 추천한다.

## Promise 체이닝

비동기 함수의 결과를 가지고 비동기 함수를 호출할 경우, Promise는 후속 처리 메소드를 체이닝하여  
프로미스를 반환하는 여러개의 비동기 함수를 연결하여 사용할 수 있다.(결과 변경, 에러 처리) .

```javascript
new Promise(function (resolve, reject) {
  setTimeout(() => resolve(1), 1000); // (*)
})
  .then(function (result) {
    // (**)

    alert(result); // 1
    return result * 2;
  })
  .then(function (result) {
    // (***)

    alert(result); // 2
    return result * 2;
  })
  .then(function (result) {
    alert(result); // 4
    return result * 2;
  });
```

## Promise.all/Promise.race

Promise의 정적 메소드

### Promise.all

```
이 메서드는 여러 프로미스의 결과를 집계할 때 유용하게 사용할 수 있습니다.
일반적으로 다음 코드를 계속 실행하기 전에 서로 연관된 비동기 작업 여러 개가
모두 이행되어야 하는 경우에 사용됩니다.

- mdn -
```

여러개의 비동기 작업을 모두 병렬 처리를 할때 사용.(결과값을 배열에 담아서 반환)

- 처리 순서 보장.
- 에러가 있을 경우 에러 반환.

```javascript
Promise.all([
  new Promise((resolve) => setTimeout(() => resolve(1), 3000)), // 1
  new Promise((resolve) => setTimeout(() => resolve(2), 2000)), // 2
  new Promise((resolve) => setTimeout(() => resolve(3), 1000)), // 3
])
  .then(console.log) // [ 1, 2, 3 ]
  .catch(console.log);
```

### Promise.race

```
race 함수는 인자로 주어진 iterable의 프로미스 중
가장 먼저 완료(settle)되는것과 같은 방식으로 완료(이행/거부)되고,
같은 결과값을 전달하는 Promise를 반환합니다.

- mdn -
```

- 가장 먼저 처리된 결과를 반환.
- 에러가 있을 경우 에러 반환.

```javascript
Promise.race([
  new Promise((resolve) => setTimeout(() => resolve(1), 3000)), // 1
  new Promise((resolve) => setTimeout(() => resolve(2), 2000)), // 2
  new Promise((resolve) => setTimeout(() => resolve(3), 1000)), // 3
])
  .then(console.log) // 3
  .catch(console.log);
```

## 참고자료 (reference)

[프로미스](https://poiemaweb.com/es6-promise)  
[[JavaScript] 프로미스(Promise)란](https://yoo11052.tistory.com/155)  
[프라미스 체이닝](https://ko.javascript.info/promise-chaining)  
[Promise.all()](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise/all)  
[Promise.race()](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise/race)  
[[10분 테코톡] 안의 비동기 처리 - Promise](https://www.youtube.com/watch?v=EWaeItyWYJw)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
