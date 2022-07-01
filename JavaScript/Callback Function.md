# Callback Function(콜백 함수)

## Callback Function 이란?

-   다른 함수의 인자로서 사용(전달)되는 함수
    > 뒤에서 호출되는(callback) 함수

```javascript
function iceCreamMaker(order, fruitIceCream, otherIceCream) {
    if (order == "fruit") {
        fruitIceCream();
    } else {
        otherIceCream();
    }
}

function strawberryIceCream() {
    console.log("딸기 아이스크림을 만들었습니다.");
}

function appleIceCream() {
    console.log("사과 아이스크림을 만들었습니다.");
}

function grapeIceCream() {
    console.log("포도 아이스크림을 만들었습니다.");
}

function vanillaIceCream() {
    console.log("바닐라 아이스크림을 만들었습니다.");
}

function greenTeaIceCream() {
    console.log("녹차 아이스크림을 만들었습니다.");
}
//iceCream의 매개변수로서 다른 함수가 들어갔다.
iceCreamMaker("fruit", strawberryIceCream, vanillaIceCream);
```

JavaScript에서의 함수는 다른 함수나 변수의 값으로 들어갈수 있다.(함수 표현식)  
이러한 특징을 응용한 것이 콜백함수이다.

> 콜백 함수를 이용하면 여러 유연한 작업이 가능하다.

## 참고자료 (reference)

[Callback function example](https://stackoverflow.com/questions/22442321/callback-function-example)  
[콜백 함수(Callback)의 정확한 의미는 무엇일까?](https://satisfactoryplace.tistory.com/18)
[Callback함수란?? 뭔데??](https://velog.io/@ko1586/Callback%ED%95%A8%EC%88%98%EB%9E%80-%EB%AD%94%EB%8D%B0)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
