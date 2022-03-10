# CSS Position

요소를 자유롭게 위치시키기 위한 속성

# position 값의 종류

static, relative, absolute, fixed, sticky

- position 값에 따라 **기준점이** 달라진다.

## static

HTML 모든 요소의 기본 position 값.

## relative

자신의 본래 위치를 기준점으로 하여 배치한다.  
float와 비슷한 상태가 되나, 다른 요소에 영향을 끼치지 않음. (레이아웃 붕괴 없음)

## absolute

자신의 조상요소 중에서 **position이 static이 아닌 요소를** 기준점으로 정한다.

- absolute를 사용할시, float와 비슷한 현상이 일어난다.

  - display가 block으로 변화
  - absolute로 인해 변화된 block은 옆에 다른 요소를 둘 수 있다.
  - 부모요소는 absolute된 요소를 인지하지 못한다.

- float와의 차이점
  - float와 달리 inline content가 absolute의 존재를 인식하지 않는다.

## fixed

기준점이 viewport.  
absolute와 동일한 현상이 일어난다.

viewport란?
브라우저 창의 전체 크기  
[Viewport 설정이 필요한 이유](https://velog.io/@huurray/Viewport-%EC%84%A4%EC%A0%95%EC%9D%B4-%ED%95%84%EC%9A%94%ED%95%9C-%EC%9D%B4%EC%9C%A0)

```css
.box {
  width: 200px;
  height: 200px;
  position: fixed;
  right: 0;
  background-color: pink;
}
```

<img src="https://user-images.githubusercontent.com/96860670/157706174-512a9449-75e4-47a6-b2a0-91a63dbc7473.png" alt="" width="300px" />

## sticky

평소에는 static의 상태.  
스크롤의 위치가 어떤 기준점에 다다르면 position: fixed; 처럼 위치하는 값

> 현재 sticky의 경우 지원하는 브라우저가 많지 않다.  
> [Can I use sticky?](https://caniuse.com/?search=sticky)

## top, right, bottom, left

position type 설정 후(기준점 설정), 요소의 위치를 옮기는 속성

> top/bottom 중에 하나, right/left 중에 하나를 사용하여 옮기는 것이 좋다.

## z-index

position이 적용된 요소의 수직 레벨을 나타내는 속성.(z축)  
[Using z-index](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/Adding_z-index)

## 참고자료 (reference)

[Viewport 설정이 필요한 이유](https://velog.io/@huurray/Viewport-%EC%84%A4%EC%A0%95%EC%9D%B4-%ED%95%84%EC%9A%94%ED%95%9C-%EC%9D%B4%EC%9C%A0)  
[CSS의 position 속성으로 요소 배치하기](https://www.daleseo.com/css-position/)  
[Using z-index](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/Adding_z-index)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
