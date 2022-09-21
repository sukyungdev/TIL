# React hooks - useMemo

useMemo 개념정리한 글입니다.

## useMemo란?
컴포넌트 성능을 최적화하는 hooks.  
Memo는 Memoization의 약자.

## Memorization이란?

```
  함수 호출의 결과를 저장하고 동일한 입력이 다시 발생할때 캐시된 결과를 
  반환하여 컴퓨터 프로그램의 속도를 높이는데 주로 사용되는 최적화 기술 입니다.
  - wikipedia -
```
동일한 값을 리턴하는 함수를 반복적으로 호출하는 상황일 때,  
값을 메모리에 저장해서 필요할 때마다 다시 계산하지 않고 재사용하는 기법.

> 자주 사용하는 값을 캐시에 저장해서 재사용하는 기법.

## 예시

> 모든 함수형 컴포넌트는 함수이고, 렌더링(함수 호출)이 이루어진다.  
> 함수는 호출될때마다 모든 내부 변수들이 초기화 된다. 

- useMemo 미사용
```javascript
function Component(){
  const value = calculate();
  return <div>value</div>;
}

function calculate () {
  return 10;
}

```
컴포넌트는 state와 props로 인한 렌더링이 수시로 일어난다.  
컴포넌트가 렌더링이 될때마다 value 변수는 다시 초기화되고, calculate 함수는 반복호출된다.  
값이 항상 바뀌는게 아니라면 비효율적이다.

- useMemo 사용

```javascript
function Component(){
  const value = calculate();
  return <div>value</div>;
}

function calculate () {
  return 10;
}

```

처음에 계산한 결과값을 메모리에 저장해서 이전에 렌더링 될때와 값이 동일할 경우   
컴포넌트가 반복적으로 렌더링이 되어도 함수를 다시 호출하지 않고  
이전에 이미 계산된 결과값을 메모리에서 꺼내서 재사용할 수 있게 해준다.  

## 구조 
```
“생성(create)” 함수와 그것의 의존성 값의 배열을 전달하세요. 
useMemo는 의존성이 변경되었을 때에만 메모이제이션된 값만 다시 계산 할 것입니다. 
이 최적화는 모든 렌더링 시의 고비용 계산을 방지하게 해 줍니다.

- React 공식 문서 -
```
```javascript
const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
```
- 첫번째 인자 : 콜백함수 -> 우리가 Memoization의 해줄 값을 계산해서 리턴해주는 함수
- 두번째 인자 : 배열(의존성 배열) -> 배열 안의 있는 요소가 업데이트가 일어날때만 다시 
  콜백함수를 호출해서 Memoization의 값을 업데이트해서 다시 Memoization 해준다.

### 만일 빈 배열이라면?
- 두번째 인자가 빈 배열이라면 맨 처음 컴포넌트가 마운트 되었을때만 값을 계산하고   
이후에는 항상 Memoization 된 값을 꺼내와서 사용.

## 주의사항
무분별하게 사용하면 성능에 무리가 갈 수 있다.
- 값을 재활용하기 위해서 따로 메모리를 소비해서 저장을 하기 때문에   
  불필요한 값들까지 모두 Memoization 하면 좋지 않다.
- 코드의 유지보수가 어려워질수 있다.

**필요할 때만 적절하게 사용하는 것이 좋다.**

## 참고자료 (reference)

[useMemo 제대로 사용하기 | 리액트 훅스 시리즈](https://www.youtube.com/watch?v=e-CnI8Q5RY4)  
[Hooks API Reference](https://ko.reactjs.org/docs/hooks-reference.html#usememo)    
[React Hooks: useMemo 사용법](https://www.daleseo.com/react-hooks-use-memo/)  
[Memoization](https://en.wikipedia.org/wiki/Memoization)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
