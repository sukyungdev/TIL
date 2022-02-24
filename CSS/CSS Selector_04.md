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

<img src="https://user-images.githubusercontent.com/96860670/155544313-ae152456-366f-4a41-b0e1-729b21213763.gif" alt="" width="500px" />. 

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

<img src="https://user-images.githubusercontent.com/96860670/155544934-005a8ebe-08b4-44ec-ae65-cf7a2352ac16.gif" alt="" width="500px" />. 

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

<img src="https://user-images.githubusercontent.com/96860670/155545454-56e557e8-9a10-4d67-83fe-2d214c8eba6d.gif" alt="" width="500px" />. 

## 참고자료 (reference)

[CSS :hover Selector](https://www.w3schools.com/cssref/sel_hover.asp)  
[동적 의사 클래스](http://www.tcpschool.com/css/css_selector_dynamic)
[CSS :active Selector](https://www.w3schools.com/cssref/sel_active.asp)
[CSS :focus Selector](https://www.w3schools.com/cssref/sel_focus.asp)

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
