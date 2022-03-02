# CSS Box Sizing

**Box-Sizing** s
css에서 box의 크기를 계산하는 방법을 지정하는 속성.

## content-box

기본적인 box-sizing 값.  
width와 height값이 content box크기로만 한정된다.  
<br />
때문에 padding값과 border값을 일일이 계산해서  
크기를 정해야 하는 불편함이 있다.

```css
div {
  box-sizing: content-box;
}
```

## border-box

padding과 border까지를 width와 height로 고려한다.  
크기를 조절하기 훨씬 쉽기 때문에 대부분의 경우 사용.

```css
div {
  box-sizing: border-box;
}
```

### content-box일 경우

<img src="https://user-images.githubusercontent.com/96860670/156378698-7e4cc4fb-542f-4895-b33b-f76bc4ee83bd.png" alt="" width="310px" />

### border-box일 경우

<img src="https://user-images.githubusercontent.com/96860670/156378765-1040eca0-600f-4698-aade-af2906e028c7.png" alt="" width="250px" />

> border-box가 훨씬 더 편리하다.

css 시작할때 전체 요소에 border-box를 선언하고 시작한다.

```css
* {
  box-sizing: border-box;
}
```

## 참고자료 (reference)

[box-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
