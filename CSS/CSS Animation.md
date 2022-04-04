# CSS Animation

## Use for Animation

Animation은 관련 속성들이 많다.

## animation-name

@keyframes를 이용해서 애니메이션을 만들고 만든 애니메이션을 요소에 설정한다.

### @keyframes

```css
@keyframs name01 {
  from {
    /* 시작 */
  }

  to {
    /* 변화 */
  }
}
```

> from, to 대신에 0%,50%,100% 같은 퍼센트도 사용가능.

### example

```css
.box {
  position: relative;
  width: 50px;
  height: 50px;
  background-color: #ff568c;
  animation-name: move-box;
}

@keyframes name01 {
  from {
    right: 0;
    width: 50px;
  }

  to {
    right: 100px;
    width: 30px;
  }
}
```

### animation-duration

애니메이션의 지속시간, 단위(ms, s) 사용.

```css
animation-duration: 1500ms;
```

### animation-timing-function

변화가 일어나는 속도의 변화(변화의 리듬)

> transtion의 timing-function과 비슷하다.

```css
animation-timing-function: ease-in;
```

### animation-delay

변화가 시작되는 시간을 조정 (딜레이 시킨다.)

> transtion의 delay와 비슷하다.

```css
animation-delay: 1000ms;
```

### animation-iteration-count

animation의 반복 횟수을 설정하는 속성.

정수를 적거나, 특정 키워드를 적어서 사용한다.

```css
transition: background-color 1000ms, color 2000ms ease-in 500ms;
```

### animation-direction

animation 사이클 방향을 설정하는 속성.  
[animation-direction](https://developer.mozilla.org/ko/docs/Web/CSS/animation-direction)

```css
animation-direction: alternate; /* 정방향과 역방향이 번갈아가며 반복 */
```

## example

```html
<body>
  <div class="box"></div>
</body>
```

```css
.box {
  position: relative;
  width: 100px;
  height: 100px;
  background-color: #ff568c;
  animation-name: move01;
  animation-duration: 1500ms;
  animation-timing-function: ease-in;
  animation-delay: 1000ms;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

@keyframes move01 {
  from {
    right: 0;
    width: 100px;
    height: 100px;
  }

  to {
    right: 100px;
    width: 50px;
    height: 50px;
  }
}
```

<img src="https://user-images.githubusercontent.com/96860670/161555335-861a78b7-811e-4258-8ec5-b7ad4968c4cc.gif" width = "350px" alt="" />

## 참고자료 (reference)

[animation-direction](https://developer.mozilla.org/ko/docs/Web/CSS/animation-direction)  
[animation](https://developer.mozilla.org/ko/docs/Web/CSS/animation)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
