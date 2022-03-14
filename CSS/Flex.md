# CSS Flex_01

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

### flex-direction: row;

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

## 참고자료 (reference)

[이번에야말로 CSS Flex를 익혀보자](https://studiomeal.com/archives/197)  
[flexbox로 만들 수 있는 10가지 레이아웃](https://d2.naver.com/helloworld/8540176#ch2)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
