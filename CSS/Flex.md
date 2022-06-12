# CSS Flex

Flex란?
레이아웃 배치, 정렬을 위해 고안되었다.

> Flexbox, Flexible Box라고도 한다.
> float보다 훨씬 강력하고 편리하다.

[브라우저 지원](https://caniuse.com/?search=flex)

## Flex 레이아웃 설정을 위한 속성

### display: flex

flex를 사용하기 위해 먼저 선언해야 하는 속성.
정렬하고자 하는 요소의 **부모요소에 선언해야 한다.**

```css
.box {
  display: flex;
  /* display: inline-flex; */
}
```

### flex-direction

어느 방향으로 정렬을 할지 정하는 속성.

```css
.box {
  display: flex;
  flex-direction: row; /* 가로 방향 */
  /* row-reverse : 가로 반대 방향 */
  /* column : 세로 방향 */
  /* column-reverse : 세로 반대 방향 */
}
```

### Axis

flex를 사용할시 생기는 축(눈에 보이지 않음)
flex-direction에 따라서 방향이 달라진다.

1. Main Axis
   요소가 배치된 방향의 축.
   flex-direction의 방향을 따른다.

2. Cross Axis
   메인축과 수직인 축.

[이번에야말로 CSS Flex를 익혀보자](https://studiomeal.com/archives/197)

### flex-warp

정렬을 한줄로 할지 여러줄로 할지 정하는 속성.(줄바꿈 관련)

- nowrap: 기본값, 모든 요소를 한 줄로 정렬한다.
- wrap: 공간이 부족할시 여러줄로 정렬한다. (여러줄을 만든다.)

```css
.box {
  display: flex;
  flex-direction: row; /* 가로 방향 */
  flex-wrap: nowrap; /*한 줄로 배치*/
}
```

### flex-grow

flex를 선언했을 때 공간이 남은 경우, 남은 공간을 어떻게 채울지 비율을 설정하는 속성.

> Flexbox에 빈공간이 있을경우, flex-grow를 이용하면 공간을 채울 수 있다.

- flex-grow를 선언하지 않은 경우

  <img src="https://user-images.githubusercontent.com/96860670/173233724-253f432c-727b-4754-9f81-c4901986f5cb.png" alt="image" width="300px">

- flex-grow를 선언한 경우

  <img src="https://user-images.githubusercontent.com/96860670/173233803-45ab7701-5bd4-4911-b556-a58e9a4ce8b8.png" alt="image" width="300px">

```css
.container div:first-child {
  background-color: blue;
  flex-grow: 1; /* 원하는 요소에 flex-grow 설정*/
}
```

- 각각 요소에 선언 가능

  <img src="https://user-images.githubusercontent.com/96860670/173233851-77917f85-36ca-485b-a1f7-9c2d0dd93baf.png" alt="image" width="300px">

```css
.container div:first-child {
  background-color: blue;
  flex-grow: 2;
}

.container div:last-child {
  background-color: green;
  flex-grow: 1;
}
```

### flex-shrink

flex를 선언했을 때 공간이 부족한 경우, 요소의 비율 축소와 관련된 속성.

- flex-shrink를 선언하지 않고 비율이 축소될 경우, 동일한 비율로 요소가 축소된다.

  <img src="https://user-images.githubusercontent.com/96860670/173234181-64d19fab-c15f-4d31-9d90-9983c2f58659.png" alt="image" width="300px">

```css
.container div:first-child {
  background-color: skyblue;
  /* flex-shrink: 2; */
}
```

- flex-shrink를 선언한 경우, 요소가 다른 비율로 축소된다.

    <img src="https://user-images.githubusercontent.com/96860670/173234197-69fbf089-ce0f-4a5e-8a02-79f58177d973.png" alt="image" width="300px">

  ```css
  .container div:first-child {
    background-color: skyblue;
    flex-shrink: 2;
  }
  ```

- 각각 요소에 선언 가능.

  <img src="https://user-images.githubusercontent.com/96860670/173234331-92a014ab-76aa-43d0-9019-38dd6131dab0.png" alt="image" width="300px">

```css
.container div:first-child {
  background-color: skyblue;
  flex-shrink: 2;
}

.container div:nth-child(2) {
  background-color: rgb(255, 181, 213);
  flex-shrink: 2;
}
```

## 참고자료 (reference)

[이번에야말로 CSS Flex를 익혀보자](https://studiomeal.com/archives/197)  
[flexbox로 만들 수 있는 10가지 레이아웃](https://d2.naver.com/helloworld/8540176#ch2)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
