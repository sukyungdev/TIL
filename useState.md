# React Hooks - useState

## State란?

컴포넌트의 렌더링 결과물에 영향을 주는 객체(컴포넌트의 상태)  
컴포넌트의 동적인 값

-   state가 변경되는 컴포넌트는 리렌더링된다.
-   state는 props와 달리 컴포넌트 안에서 관리된다.(변수처럼)

> ul로 구현하고 싶은 데이터는 state로 만들자!

## useState란?

React의 Hooks중 하나.  
State를 컴포넌트에서 생성하고 관리할수 있는 함수를 제공한다.

## useState 사용하기

```javascript
//const [state이름, state를 업데이트 시키는 함수(setter 함수)] = useState(초기값)
const [state, setState] = useState("hello");
```

> 초기값 hello가 담긴 state와 state를 변경시킬수 있는 setState를 반환.

## useState 사용하기 - 예제

```javascript
import { useState } from "react"; // import
import "./styles.css";
import React from "react";

export default function App() {
    const [number, setNumber] = useState(1);

    const click = () => {
        let newNumber;
        number >= 12 ? (newNumber = 1) : (newNumber = number + 1);
        setNumber(newNumber);
    };
    console.log("업데이트");

    return (
        <div className="App">
            <h1>Counter : {number}</h1>
            <button onClick={click}>+</button>
        </div>
    );
}
```

[codeSandBox](https://codesandbox.io/s/jovial-joliot-009c6z?file=/src/App.js:0-346)

> 버튼을 눌러서 number가 변경될 때마다 컴포넌트는 리렌더링 된다.
> setNumber 함수를 이용해서 number값을 변경할수 있다.

-   setter 함수에 콜백함수를 넣는 경우

    변하는 state가 이전 state와 관련이 있는 경우 콜백함수를 이용해서  
    새로운 state를 리턴한다.

```javascript
const handleUpload = () => {
    setNames((prevState) => {
        return [input, ...prevState];
    });
};
```

-   useState에 콜백함수를 넣는 경우

    초기값에 무거운 작업이 있을 경우 콜백함수를 이용하면 처음 렌더링될때만  
    실행이 된다.

```javascript
const [state, setState] = useState(() => {
    return work();
});
```

## 참고자료 (reference)

[useState 15분만에 마스터하기 | 리액트 훅스 시리즈](https://www.youtube.com/watch?v=G3qglTF-fFI)  
[[React] 컴포넌트의 State 란?](https://velog.io/@hidaehyunlee/React-State-%EB%9E%80)  
[useState 를 통해 컴포넌트에서 바뀌는 값 관리하기](https://react.vlpt.us/basic/07-useState.html)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
