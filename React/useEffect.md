# React Hooks - useEffect

## useEffect란?

useEffect가 등장하면서 함수 컴포넌트안에서 컴포넌트 생명주기(lifeCycle)를  
다룰 수 있게 되었다.

### 컴포넌트 생명주기(lifeCycle)?

React 컴포넌트들은 생명주기가 있다.

<img src="https://raw.githubusercontent.com/donavon/hook-flow/master/hook-flow.png" width ="" alt="" />

<img src="https://velog.velcdn.com/images%2Fsukong%2Fpost%2F46aeb296-b83b-49dc-a8b8-384509735f5b%2Fimage.png" width="" alt="" />

-   1단계 : Mount(생성)
    -   컴포넌트가 페이지에 처음 렌더링이 될때
-   2단계 : Update(변화)
    -   state가 변경될 경우
    -   부모 컴포넌트가 re-rendering될 경우
-   3단계 : Unmount(소멸)
    -   컴포넌트가 DOM에서 제거되는 과정

useEffect를 사용하면 컴포넌트의 상태 변화 타이밍에 특정 작업을 실행할수 있다.  
(함수 기반 컴포넌트)

## useEffect 사용하기

### 1. 콜백함수를 인자로 받는 경우

-   useEffect는 기본적으로 콜백함수를 인자로 받는다.
    -   콜백함수 내부에 원하는 작업 작성

```javascript
useEffect(() => {
    // 원하는 작업 코드 작성
});
```

#### 언제 실행 되나요?

-   componentMount(처음 렌더링)
-   componentUpdate(컴포넌트가 재렌더링 될때)

#### 예제

```javascript
import { useEffect, useState } from "react";
import "./styles.css";

export default function App() {
    const [count, setCount] = useState(1);
    const handleCount = () => {
        setCount(count + 1);
    };

    //렌러링 될 때마다 실행
    useEffect(() => {
        console.log("rendering");
    });

    return (
        <div className="App">
            <h2>{count}</h2>
            <button onClick={handleCount}>+</button>
        </div>
    );
}
```

---

### 2. 콜백함수와 배열을 인자로 받는 경우

-   useEffect의 배열은 dependency array라고도 한다.

```javascript
useEffect(() => {
    //원하는 작업 코드 작성
}, [value]);
```

#### 언제 실행 되나요?

-   componentMount(처음 렌더링)
-   array안의 값(value)가 바뀔때

#### 예제

```javascript
import { useEffect, useState } from "react";
import "./styles.css";

export default function App() {
    const [count, setCount] = useState(1);
    const [name, setName] = useState("");

    const handleCount = () => {
        setCount(count + 1);
    };

    const handleInputChange = (e) => {
        setName(e.target.value);
    };

    //Mount + [value]에 따른 변화
    useEffect(() => {
        console.log("name 변화");
    }, [name]);

    return (
        <div className="App">
            <h2>{count}</h2>
            <button onClick={handleCount}>+</button>
            <br />
            <input type="text" value={name} onChange={handleInputChange} />
            <p>{name}</p>
        </div>
    );
}
```

---

### 3. 반약 빈 배열을 전달한다면?

```javascript
useEffect(() => {
    //원하는 작업 코드 작성
}, []); // 빈 배열 전달
```

-   componentMount(처음 렌더링) 될때만 실행

#### 예제

```javascript
//Mount때만 실행
useEffect(() => {
    console.log("Mount");
}, []);
```

## Clean Up

useEffect 콜백함수 안의 작업을 해제하는 코드

```javascript
useEffect(() => {
    //원하는 작업 코드 작성
    return () => {
        //원하는 작업 해지
    };
}, []);
```

-   리턴 함수는 해당 컴포넌트가 unMount 될때  
    혹은 다음 렌더링시 불릴 useEffect가  
    실행되기 전에 실행이 된다.

    ```
    React가 effect를 정리(clean-up)하는 시점은 정확히 언제일까요? React는 컴포넌트가 마운트 해제되는때에 정리(clean-up)를 실행합니다. 하지만 위의 예시에서 보았듯이 effect는 한번이 아니라 렌더링이 실행되는 때마다 실행됩니다.
    React가 다음 차례의 effect를 실행하기 전에 이전의 렌더링에서 파생된 effect 또한 정리하는 이유가 바로 이 때문입니다. 이것이 버그를 방지하는 데에 어떻게 도움이 되는지 그리고 성능 저하 문제가 발생할 경우 effect를 건너뛰는 방법에 대해서 이다음으로 논의해봅시다.

    - 출처 : React 공식문서(Using the Effect Hook)
    ```

### 예제

[예제 코드](https://codesandbox.io/s/snowy-night-eix38d?file=/src/component/Timer.js)

## 참고자료 (reference)

[useEffect 깔끔하게 마스터하기 | 리액트 훅스 시리즈](https://www.youtube.com/watch?v=kyodvzc5GHU)  
[[React] 리액트의 생명주기와 Hook](https://velog.io/@sukong/REACT-%EB%A6%AC%EC%95%A1%ED%8A%B8%EC%9D%98-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0%EC%99%80-useEffect-Hook)  
[Using the Effect Hook](https://ko.reactjs.org/docs/hooks-effect.html)  
[[React]useEffect와 컴포넌트 생명주기](https://charles098.tistory.com/176)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
