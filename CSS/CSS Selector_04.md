# CSS Selector_04

User Action Pseudo-Classes Selector(동적 가상 클래스 선택자)

> Dynamic Pseudo-Class 라고도 부른다.

동적 가상 클래스 선택자?  
어떤 상태와 조건을 만족할때 사용하는 클래스 선택자.  
**사용자의 행동에 따라 다른 속성을 부여하는 선택자.**

동적 가상 클래스 선택자의 종류  
[동적 의사 클래스](http://www.tcpschool.com/css/css_selector_dynamic)

# 많이 사용하는 동적 가장 클래스 선택자

## :hover

마우스 커서가 특정 요소의 영역에 올라갔을때 다른 속성을 부여한다.

```html
<section>
  <h1>User Action Pseudo-Classes Selector</h1>
  <a href="">:hover</a>
  <input type="text" placeholder=":active" />
</section>
```

```css
/* tagname:hover */
a:hover {
  background-color: #fc5780;
}
```

[CSS :hover Selector](https://www.w3schools.com/cssref/sel_hover.asp)

<img src="" alt="" width="300px"/>

## :active

마우스 커서가 특정 요소를 누르고 있을때 다른 속성을 부여한다.

```css
/* tagname:active */
a:active {
  background-color: #f32e60;
}
```

:active는 :hover 가상 클래스가 있는 경우 :hover의 뒤에 와야 한다.  
[CSS :active Selector](https://www.w3schools.com/cssref/sel_active.asp)

> <img src="" alt="" width="300px"/>

## :focus

focus를 가지고 있는 요소에 다른 속성을 부여한다.

```css
/* tagname:focus */
input:focus {
  border-color: #00dda6;
}
```

:focus는 키보드 입력이나 기타 사용자 입력이 가능한 요소에만 적용된다.  
[CSS :focus Selector](https://www.w3schools.com/cssref/sel_focus.asp)

<img src="" alt="" width="300px"/>

## 참고자료 (reference)

[CSS :hover Selector](https://www.w3schools.com/cssref/sel_hover.asp)  
[동적 의사 클래스](http://www.tcpschool.com/css/css_selector_dynamic)
[CSS :active Selector](https://www.w3schools.com/cssref/sel_active.asp)
[CSS :focus Selector](https://www.w3schools.com/cssref/sel_focus.asp)

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
