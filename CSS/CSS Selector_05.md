# CSS Selector_05

CSS Specificity(CSS 특수성) - CSS 선택자 우선순위

CSS 선택자 우선순위?

CSS 선택자들은 각각 우선순위가 있다.  
동일한 HTML요소를 선택하는 CSS 선택자가 2개 이상일 경우  
순위에 따라 스타일이 적용된다.

점수/순위의 개념이다.

# CSS 기본 적용 개념

```css
h1 {
  color: blue;
}

h1 {
  color: pink;
}
```

아래의 pink 컬러가 적용이 된다.

> CSS는 기본적으로 아래의 스타일(최근 스타일)이 적용이 된다.

# CSS 선택자 우선순위 중요도

id > class > type

## id selector

**1 순위**
class selector, type selector 보다 우선적으로 적용된다.

```css
#hello {
  color: blueviolet;
}

.one.two.three {
  color: pink;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155867866-e6bf24ce-733a-4bea-b465-e43508f198c3.png" alt="" width="150px" />

class selector의 개수와 상관없이 1순위인 id selector의 스타일이 우선적용.

## class selector

**2 순위**
type selector 보다 우선적으로 적용된다.

```css
.one.two.three {
  color: pink;
}

h1 {
  color: blue;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155867885-c606f901-8493-42b3-897d-3520e35c7f6e.png" alt="" width="150px" />

Pseudo-Class Selectors(가상 클래스 선택자)도 동일한 순위로 적용.

## type selector

**3 순위**
가장 마지막으로 적용되는 selector.

## example

```html
<section>
  <ol id="abcde" class="english">
    <li>a</li>
    <li>b</li>
    <li>c</li>
    <li>d</li>
    <li>e</li>
  </ol>
</section>
```

### 1. 다음중 적용되는 스타일은?

```css
#abcde.english li {
  color: skyblue;
}

#abcde.english {
  color: blueviolet;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155867901-417716e9-d14e-4a28-9e0a-9f9f743a4dc8.png" alt="" width="70px">

1,2,3 순위가 같이 있기 때문에 skyblue 색상이 적용.

### 2. 첫번째 li의 색상은?

```css
#abcde.english li:first-child {
  color: blueviolet;
}

#abcde.english li {
  color: skyblue;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155867982-1383996c-6dba-4e8f-89f7-625fb4312d0d.png" alt="" width="70px">

첫번째 스타일 : 1순위 1개, 2순위 2개, 3순위 1개  
두번째 스타일 : 1순위 1개, 2순위 개, 3순위 1개  
첫번째 스타일의 우선순위가 더 높으므로 blueviolet 색상이 적용.

## 예외

예외적인 요소 존재(inline style, !important)

### inline style

HTML 문서에 직접 스타일을 주는 방법.  
id, class, type selector에 **상관없이** 우선순위로 먼저 적용.(id 보다 순위가 높다. 0순위)

```html
<section>
  <h1 id="hi" style="color: gold;">Hello</h1>
</section>
```

<img src="https://user-images.githubusercontent.com/96860670/155867953-5affa04a-1f5b-49eb-b1cf-602752ac67df.png" alt="" width="150px" />

### !important

CSS 속성에 !important 선언.
inline style, id, class, type에 상관없인 **무조건 우선적용**

```css
h1 {
  color: blue !important;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155867965-2548b11e-5c7b-4ea5-893c-68e3707b3a5f.png" alt="" width="150px" />

> inline style, !important는 꼭 필요한 경우가 아니면 사용을 자제하는 것이 좋다.

## 참고자료 (reference)

[CSS Specificity](https://www.w3schools.com/css/css_specificity.asp)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
