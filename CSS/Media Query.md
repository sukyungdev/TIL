# CSS Media Query

Media Query란?  
반응형 웹(Responsive Web)을 만들기 위해 CSS에서 작성하는 선언.

반응형 웹(Responsive Web)이란?  
해당 웹페이지의 크기(viewport)에 따라 다르게 보이는 웹.

[반응형 웹 디자인](https://business.adobe.com/kr/glossary/responsive-web-design.html)

## viewport meta

media query와 함께 반응형 웹을 만들기 위해 필요한
HTML 태그.

> head 태그 안에 입력해야 한다.

[반응형 웹 뚝딱 만들기 (1) - 뷰포트 메타태그와 미디어 쿼리](https://nykim.work/84)

```html
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>
```

## media query

@media screen을 이용해서 선언.

```css
@media screen and (min-width: 350px) {
  /* 브라우저 가로 사이즈 350px 이상일때 아래 CSS style 적용 */
}

@media screen and (max-width: 350px) {
  /* 브라우저 가로 사이즈 350px 이하일때 아래 CSS style 적용 */
}
```

### example

HTML Code
```html
<body>
    <div class="box"></div>
</body>
```

CSS Code
```css
* {
  box-sizing: border-box;
  margin: 0;
}

.box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100vh;
  background-color: #fd9ac8;
}

.box::after {
  display: block;
  content: 'Desktop';
  font-size: 50px;
}

@media screen and (max-width:768px) {
  .box {
    background-color: #d365ff;
  }

  .box::after {
    content: 'tablet';
  }
}

@media screen and (max-width:375px) {
  .box {
    background-color: #558ffa;
  }

  .box::after {
    content: 'moblie';
  }
}

```
<img src="https://user-images.githubusercontent.com/96860670/159125328-b4f66191-b749-4b94-ab7e-e69626d7d97e.gif" alt="" width="450px" />

## 참고자료 (reference)

[반응형 웹 디자인](https://business.adobe.com/kr/glossary/responsive-web-design.html)  
[반응형 웹 뚝딱 만들기 (1) - 뷰포트 메타태그와 미디어 쿼리](https://nykim.work/84)  
[Responsive Web ① – 반응형 웹을 위해 개발자가 꼭 알아야 하는 기술들](https://www.samsungsds.com/kr/insights/Responsive_web_1.html)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
