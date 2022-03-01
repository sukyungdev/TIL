# CSS Box Model

HTML 요소는 브라우저 엔진에서 모델링 될 때, Box로 표현이 된다.

Box Model
Box는 일정한 형태의 규격으로 구성되어 있다.

<img src="https://user-images.githubusercontent.com/96860670/156191608-3e34e64c-bba3-4af3-a085-744c44d663ab.png" alt="" width="250px" />

# Box Model의 규격

## Content

content가 있는 box.
가로는 width, 세로는 height 속성.

<img src="https://user-images.githubusercontent.com/96860670/156191823-e8f1fbc5-eeb4-4fbb-aa22-011f9446347a.png" alt="" width="250px" />

## Padding

content와 border사이에 있는 안쪽 여백.(공간)

<img src="https://user-images.githubusercontent.com/96860670/156191907-38fc33ef-97e3-41ca-b285-abf9dc015026.png" alt="" width="250px" />

## Border

테두리(굵기, 스타일, 색상 명시 필요)

```css
/*굵기 스타일 색상*/
h1 {
  border: 1px solid #000;
}

/*border을 사용하지 않을 경우*/
h1 {
  border: none;
}
```

<img src="https://user-images.githubusercontent.com/96860670/156192077-82589b0b-d832-4a6c-81c3-785b626f5d31.png" alt="" width="250px" />

## Margin

바깥쪽 여백, 요소와 요소 사이의 간격

> 눈에 보이지 않는 부분이다.

<img src="https://user-images.githubusercontent.com/96860670/156192115-433af669-08eb-4011-afbc-03fef20d4cbc.png" alt="" width="250px" />

## Short hand

padding과 maring은 top, right, bottom, left등 적어야 할 것이 많다.  
속도를 빠르게 하기 위해 Short hand가 존재한다.

top과 bottom이 세트.
right와 left가 세트.

1. 시계방향으로 top, right, left, bottom
2. top/bottom, right/left
3. top, right/left, bottom

```css
/**/
.hello {
  /* top right bottom left */
  padding: 10px 20px 30px 40px;
  /* top/bottom right/left */
  margin: 10px 20px;
  /* top right/left bottom */
  padding: 10px 30px 20px;
}
```

## 참고자료 (reference)

[CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp)  
[박스 모델(box model)](http://www.tcpschool.com/css/css_boxmodel_boxmodel)  
[CSS 박스 모델과 box-sizing 속성](https://www.daleseo.com/css-box-model/)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
