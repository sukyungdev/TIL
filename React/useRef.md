# React Hooks - useRef

## useRef란?

```javascript
const ref = useRef(value); // ref = {current : value}
```

하나의 오브젝트, 안에 current라는 값을 가지고 있다.  
useRef를 사용하면 ref object를 반환한다.  
인자로 넣어준 value값을 오브젝트 안에 저장된다.

> ref object는 수정이 가능

```javascript
ref.current = "2"; // {current : "2"}
```

ref는 컴포넌트의 전 생애 주기 동안 유지가 된다.

> 컴포넌트가 계속 렌더링되어도, 컴포넌트가 unMount 되기 전까지는 유지가 된다.

## useRef는 언제 사용하면 좋을까?

### 1. 어떤 값을 저장하는 공간(변수관리)

> 변화는 감지해야 하지만 그 변화가 렌더링을 발생시키면 안되는 어떤 값을 다룰때

```
본질적으로 useRef는 .current 프로퍼티에 변경 가능한 값을 담고 있는 “상자”와 같습니다.

그렇지만, ref 속성보다 useRef()가 더 유용합니다. 이 기능은 클래스에서 인스턴스 필드를 사용하는 방법과 유사한 어떤 가변값을 유지하는 데에 편리합니다.

- React 공식문서-
```

#### State와의 차이

-   state 값의 변경
    state는 값이 변경이 되면 자동으로 컴포넌트가 다시 렌더링 된다.  
    (내부에 있는 변수도 다시 초기화된다.)  
    이는 원하지 않는 렌더링을 일으킬 수 있다.

-   ref 값의 변경
    ref의 변경은 컴포넌트가 다시 렌더링 되지않는다. (변수 값도 유지됨)  
    값이 변화되어도 렌더링을 발생 시키지 않기 때문에 효율적이다.  
    **state가 변화되거나 컴포넌트가 rerendering되어도 ref안의 값은 변하지 않는다.**

> 변경시 렌더링을 발생시키지 않아야하는 값을 다루는데 아주 유용하다.

#### 컴포넌트 내부의 변수의 ref의 차이

함수가 다시 불릴때(리렌더링 될때) 변수값은 모두 초기화 되지만, ref는 초기화 되지 않는다.

#### 예제

-   ref, state, 변수의 비교
    [codeSandBox](https://codesandbox.io/s/pedantic-phoebe-v8gnif?file=/src/App.js)

```javascript
import { useState, useEffect, useRef } from "react";

function App() {
    const [count, setCount] = useState(1);
    const renderCount = useRef(1);

    useEffect(() => {
        renderCount.current = renderCount.current + 1;
        console.log(renderCount.current);
    });

    return (
        <div className="App">
            <p>Count: {count}</p>
            <button onClick={() => setCount(count + 1)}> count 올려</button>
        </div>
    );
}

export default App;
```

-   위와 같은 상황에서 state를 사용한다면 useEffect는 무한으로 실행된다.

[[React] useRef 200% 활용하기](https://velog.io/@juno7803/React-useRef-200-%ED%99%9C%EC%9A%A9%ED%95%98%EA%B8%B0)

## DOM요소에 접근

ref는 객체이며, DOM을 할당할수도 있다.

> Vanilla JS의 document.querySelector와 비슷한 느낌의 역할.

```javascript
const ref = useRef(value); // ref = {current : value}
```

ref 오브젝트를 접근하고자 하는 요소 태그에 ref속성으로 넣어주면  
해당요소에 접근할수 있다.

```javascript
<input ref={ref} />
```

#### 예제

```javascript
import { useRef, useEffect } from "react";

function App() {
    const inputRef = useRef();

    useEffect(() => {
        console.log(inputRef);
        inputRef.current.focus();
    }, []);

    const login = () => {
        alert(`환영합니다. ${inputRef.current.value}!`);
        inputRef.current.focus();
    };

    return (
        <div className="App">
            <input ref={inputRef} type="test" placeholder="username" />
            <button onClick={login}>로그인</button>
        </div>
    );
}

export default App;
```

## 참고자료 (reference)

[Hooks API Reference](https://ko.reactjs.org/docs/hooks-reference.html)  
[[React] useRef 200% 활용하기](https://velog.io/@juno7803/React-useRef-200-%ED%99%9C%EC%9A%A9%ED%95%98%EA%B8%B0)  
[10. useRef 로 특정 DOM 선택하기](https://react.vlpt.us/basic/10-useRef.html)  
[useRef 사용법 정리](https://sezzled.tistory.com/123)  
[useRef 완벽 정리 1# 변수 관리](https://www.youtube.com/watch?v=VxqZrL4FLz8)  
[useRef 완벽 정리 2# DOM 요소 접근](https://www.youtube.com/watch?v=EMK8oUUwP5Q)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
