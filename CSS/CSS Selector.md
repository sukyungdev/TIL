# CSS Selector

css는 html 문서의 요소를 선택하여 스타일 속성을 부여한다.  
때문에 html 요소를 정확히 선택하는 것이 중요하며 이를 위해  
다양한 선택자들이 있다.

## 1. Type Selector

html 태그를 직접 선택하여 속성을 부여하는 선택자
가장 기초적인 선택자이다.

```css
h1 {
  color: #ff0000;
}
```

## class Selector

html tag에 class 속성을 주고, css에서 class 속성의 속성값으로  
html 요소를 선택하여 style 속성을 부여하는 선택자.

css에서 선택할 때, **class 속성값 앞에 . 을 붙여서 선택한다.**

```html
<h1 class="name">sukyungdev</h1>
```

```css
.name {
  color: #ff0000;
}
```

> class 속성은 동일한 속성을 여러 요소에 줄 수 있다.(중복가능)  
> 한 요소가 여러개의 class를 가질 수 있다.

만약 class selector를 붙여서 사용할시 and(교집합) 의미를 가진다.

```css
/*class가 name이자 hello인 html 요소 선택*/
.name.hello {
  color: #ff0000;
}
```

## id Selector

html tag에 id 속성을 주고, css에서 id 속성의 속성값으로  
html 요소를 선택하여 style 속성을 부여하는 선택자.

css에서 선택할 때, **id 속성값 앞에 # 을 붙여서 선택한다.**

```html
<h1 class="name" id="myname">sukyungdev</h1>
```

```css
#myname {
  font-size: 25px;
}
```

> id 속성은 하나의 id 속성값만 있을 수 있다. (중복 불가능)
> 한 요소에는 하나의 id만 있다.

## 참고자료 (reference)

[CSS Selector Reference](https://www.w3schools.com/cssref/css_selectors.asp)  
[[CSS] Selector, Class와 Id의 차이점](https://joooing.tistory.com/entry/css-Selector)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
