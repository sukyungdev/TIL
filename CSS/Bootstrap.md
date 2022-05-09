# Bootstrap

## Bootstrap이란?

Component와 반응형 그리드 시스템을 제공하는 프론트엔드개발 프레임워크

## Bootstrap 사용준비(CSS)

1. 아래 사이트에 접속해서 CSS 파트의 코드 복사.  
   [Introduction](https://getbootstrap.com/docs/5.1/getting-started/introduction/)

2. html 문서 head 태그 안에 붙여넣기.

## Bootstrap 사용하기

1. 우선 container를 만든다.

```html
<div class="container"></div>
```

2. container안에 row를 만든다.
   row: 하나의 가로줄.

```html
<div class="container">
  <div class="row"></div>
</div>
```

3. row안에 col-oo을 만든다.

   oo안에 원하는 col의 개수(칸을 몇개 차지할 것인가)를 적는다.

```html
<div class="container">
  <div class="row">
    <!-- 컬럼수가 1개 -->
    <div class="col-1"></div>
  </div>
</div>
```

3. col-oo안에 원하는 내용을 채운다.

```html
<div class="container">
  <div class="row">
    <!-- 컬럼수가 1개 -->
    <div class="col-1">
      <p>Hello</p>
    </div>
  </div>
</div>
```

> bootstrap은 총 12 칸으로 이루어져 있다.

### 주의사항

```html
<div class="container">
  <div class="row">
    <!-- 컬럼수가 1개 -->
    <div class="col-1">
      <p>Hello</p>
    </div>
  </div>
</div>
```

**위와 같은 구조를 반드시 유지해야 한다.**  
container의 자식은 row.  
row의 자식은 col-1.  
col-1안에 원하는 요소 작성.

> col과 container는 브라우저 사이즈에 따라 반응형으로 동작한다.

## col의 크기 바꾸기

브라우저 사이즈에 따라서 col의 크기를 바꿀수 있다.

```html
<div class="container">
  <div class="row">
    <!-- 브라우저 사이즈에 따른 칸수 변화-->
    <div class="col-12 col-sm-6 col-md-4 col-lg-2 col-xl-1">
      <p>column</p>
    </div>
  </div>
</div>
```

- col-12 : mobile size(576px이하)에서 12칸.
- col-sm-6 : small size(576px이상)에서 6칸.
- col-md-4 : medium size(768px이상)에서 4칸.
- col-lg-2 : large size(992px이상)에서 2칸.
- col-xl-1 : x-large size(1200px이상)에서 1칸.

[Grid system](https://getbootstrap.com/docs/5.1/layout/grid/)

## 참고자료 (reference)

[[Bootstrap] 부트스트랩이란?](https://ict-nroo.tistory.com/21)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
