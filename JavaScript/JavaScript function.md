# Javascript function

funtion(함수)란?

어떠한 목적을 가진 단위(코드의 집합).
코드를 캡슐처럼 독립적으로 만든것.

## 함수 정의

함수의 정의는 function 키워드로 시작.

```javascript
function 함수이름(매개변수1, 매개변수2) {
  실행문;

  return 값;
}
```

> funtcion(){}는 함수 정의의 필수적 조건.

## 함수 호출

함수 정의 후, 함수를 실행하기 위해서는 함수 호출이 필요하다.  
()를 이용해서 함수를 호출한다.

```javascript
//함수 정의
function apple() {
  console.log("apple");
}

//함수 호출
apple();
```

## 매개 변수

매개 변수란?

함수가 필요한 값(정보)를 전달했을때, 함수 내부에서 그 값을 사용하기 위한 변수.

```javascript
function a(x, y) {
  //x, y는 매개변수이다.
  console.log(x, y);
}
```

### 매개변수와 인자(인수)와의 차이

- 매개변수는 인자를 전달받기 위한 변수.
- 인자는 함수를 호출할때 전달되는 값.

```javascript
function a(x, y) {
  // 매개변수 (argument)
  console.log(x + y);
}

a(5, 7); // 인자(parameter)
```

[argument와 parameter 차이점](http://taewan.kim/tip/argument_parameter/)

## return

함수에서 실행된 결과를 반환하는 것.

- return을 실행하게 되면 함수의 실행이 중단된다.
- return은 모든 타입의 값을 반환가능.

```javascript
function a(x, y) {
  return x + y;
}

const aReturn = a(5, 7);
console.log(aReturn);
```

## 추가

함수는 다른 함수나 변수 안에 들어갈수 있다.

```javascript
function a(x, y) {
  return x + y;
}

function b() {
  let number = a(5, 7);

  return number;
}

console.log(b());
```

## 참고자료 (reference)

[argument와 parameter 차이점](http://taewan.kim/tip/argument_parameter/)  
[Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
