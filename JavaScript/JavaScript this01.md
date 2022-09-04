# JavaScript this 01

## this란?

JavaScript에서 this는 객체를 가리키는 키워드다.

어떠한 객체를 가리킬까?  
this를 어떤 방법으로 호출했느냐에 따라서 달라진다.

```
대부분의 경우 this의 값은 함수를 호출한 방법에 의해 결정됩니다.

- mdn -
```

## this가 가리키는 객체를 정하는 방법(규칙)

### 1. this를 전역에서 단독으로 사용한 경우

window 객체를 가리킨다.

> window 객체 : 모든 객체를 가지고 있는 브라우저에서 제공하는 전역객체

```javascript
console.log(this); //Window {...}
```

### 2. 함수에서의 this

this는 현재 함수를 실행하고 있는 객체를 가리킨다. (함수의 주인에게 바인딩)

#### 2-1. 전역 범위에서 선언된 함수의 this

window 객체를 가리킨다.

> 전역 범위의 함수는 window객체의 메소드

```javascript
function a() {
    console.log(this);
}

a(); //Window {...}
```

#### 2-2. 메서드에서 선언된 this

해당 메서드를 호출한 객체를 가리킨다. (해당 함수가 속성으로 있는 객체)

```javascript
let obj = {
    name: "a",
    print: function () {
        console.log(this);
    },
};

obj.print(); //obj
```

#### 메서드 내부에서의 콜백함수에서 선언된 this

Window 객체를 가리킨다.

> 콜백함수는 메서드라도 Window를 가리킨다.

```javascript
let obj = {
    name: "a",
    print: function () {
        setTimeout(function () {
            //내부함수
            console.log(this); // Window {...}
        }, 1000);
    },
};

obj.print();
```

#### 화살표 함수에서의 this

화살표함수의 this는 상위 스코프의 this를 가리킨다.

```javascript
let obj = {
    a: function () {
        console.log("a", this);
    },
    b: () => {
        console.log("b", this);
    },
};

obj.a(); // obj
obj.b(); // Window {...}
```

> 상위 스코프의 obj의 this가 Window 객체이므로 Window를 가리킨다.

## 참고자료 (reference)

[this](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/this)  
[JavaScript 개발자라면 꼭 알아야 할 this](https://wormwlrm.github.io/2019/03/04/You-should-know-JavaScript-this.html.html)  
[1. this에 관한 자바스크립트의 몇 가지 규칙](https://tevelop.tistory.com/1#toc-this%EC%97%90%20%EA%B4%80%ED%95%9C%20%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EC%9D%98%20%EB%AA%87%20%EA%B0%80%EC%A7%80%20%EA%B7%9C%EC%B9%99)  
[자바스크립트 this란 무엇인가?](https://www.youtube.com/watch?v=GteV4zfqPIk&t=1023s)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
