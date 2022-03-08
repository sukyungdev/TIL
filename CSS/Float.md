# CSS Float

block요소 가로배치를 위한 속성

# Float 특징

요소에 float를 적용하면, 요소는 float(뜨는) 상태가 된다.

- 부모요소와 형제요소는 float상태가 된 요소를 인식하지 못한다.

  - 부모요소의 height값이 줄어든다.

- float된 요소는 자동으로 display 속성이 block으로 된다.

  - 이렇게 block이 된 요소는 옆자리에 다른 요소를 둘 수 있다.
  - 남은 공간을 자동으로 margin으로 채우지 않는다.

```css
div {
  float: left; /*요소를 왼쪽으로 배치*/
}

div {
  float: right; /*요소를 오른쪽으로 배치*/
}
```

## Float의 영향

float된 요소를 부모요소는 인식하지 못하기 때문에 레이아웃에 영향을 준다. s
때문에 float를 적용한 후 해지하는 것이 꼭 필요하다.

> block 요소들은 float된 요소를 인식하지 못한다.  
> 그러나 inline 요소는 인식 가능.  
> inline 요소는 float 된 요소를 피해서 흐르게 된다.

## float 해지

대표적인 2가지 방법 소개

### 1. 부모요소에 overflow: hidden;

```css
.parent {
  overflow: hidden;
}
```

이렇개 하면 부모요소는 float된 자식요소를 인식하고, 레이아웃이 정상적으로 된다.

### 2. clearfix

clear 속성 사용.

```css
div {
  clear: left;
}
```

clear 속성이 적용된 요소는 float의 영향을 받지 않으며, 부모요소가 자식요소의 자리를 인식하게 된다.(clear 된 요소 포함)

- left, right, both 값이 있다.
- clear는 block 요소만 적용할 수 있다.

### 가상요소를 이용한 clearfix(추천)

```css
.box::after {
  content: "";
  display: block;
  clear: left;
}
```

HTML 문서에 별도로 태그를 추가하지 않고, css로 clearfix를 하는 방법.

## 참고자료 (reference)

[CSS float란?](https://velog.io/@shin6403/CSS-float%EB%9E%80)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
