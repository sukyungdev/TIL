# CSS Box Display

CSS Box(Display)의 type에 따라서 box model의 작동 방식이 달라진다.

# Box(Display) Type

block, inline, inline block

## block

```css
div {
  display: block;
}
```

가로전체를 차지하는 display 속성.
다른 요소들이 자신의 줄(공간)에 오지 못하도록 한다.

- 별도의 width를 설정하지 않은 경우, 부모의 content-box의 width가 된다.
- 별도의 width를 설정할 경우, 남은 공간은 margin으로 채운다.
  > 아래의 요소가 자신의 공간에 오지 못하도록 한다.
- width, height, padding, border, margin 전부 적용가능.
- 별도의 height를 설정하지 않은 경우, 자식 요소의 height합이 부모 요소의 height가 된다.

### margin: 0 auto;

block type(요소)을 가운데 정렬하기 위한 방법.  
top/bottom에 0, right/left에 auto를 주어서 가운데 정렬.

```css
div {
  margin: 0 auto;
}
```

## Inline

한줄로 나란히 배치되는 성격의 display 속성.(쭉 나열되다가 공간이 부족하면 아랫줄로 이동).

- width, hegiht, padding-top, padding-bottom, border-top, border-bottom,  
  margin-top, margin-bottom 사용불가.

```css
div {
  display: inline;
}
```

## Inline Block

inline의 성격에 block의 성격이 더해진 type.

- 배치되는 성격 + 공간 차지
- width, hegiht, padding-top, padding-bottom, border-top, border-bottom,  
  margin-top, margin-bottom 사용가능.

```css
div {
  display: inline-block;
}
```

## 참고자료 (reference)

[[CSS] display 속성: inline, block, inline-block](https://www.daleseo.com/css-display-inline-block/)  
[display 속성](https://ofcourse.kr/css-course/display-%EC%86%8D%EC%84%B1)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
