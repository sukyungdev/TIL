# CSS Selector_02

CSS Combinators(조합 선택자 - 자식, 자손 ,형제)

자식, 자손, 형제의 개념

```html
<section>
  <h1>Hello!</h1>
  <ol>
    <li>
      <h1>Welcome</h1>
      <p>Welcome my TIL repository!</p>
    </li>
    <li class="thankyou">
      <p>Thank you</p>
    </li>
    <li>
      <strong>sukyungdev</strong>
    </li>
    <li>
      <p>2022.02.21</p>
    </li>
  </ol>
</section>
```

- h1와 ol은 section tag의 자식
- li은 section tag의 자손
- h1과 ol은 형제 (ol 안의 li tag는 모두 형제 관계)
- 자손이란 개념은 자식을 포함한다.

## child selector(자식 선택자)

```css
/*parent > child*/
section > h1 {
  color: #00ffff;
}
```

부모태그의 직계 자식만 선택하여 속성 적용

## descendant selector(자손 선택자)

```css
/*parent descendant*/
section h1 {
  color: #00ffff;
}
```

부모태그의 자손을 모두 선택하여 속성 적용(자식을 포함한다.)

## sibling selector(형제 선택자)

### sibling selector 01

```css
/*selector1 ~ selector2*/
.thankyou ~ li {
  color: #ff00c8;
}
```

.thankyou 다음의 형제 태그(li)들에 스타일을 부여한다.

<img src="https://user-images.githubusercontent.com/96860670/154978267-3f05a233-d904-4de1-a4c7-96fa37992acb.png" alt="" width="250px"/>

### sibling selector 02

```css
/*selector1 + selector2*/
.thankyou + li {
  color: #ff00c8;
}
```

<img src="https://user-images.githubusercontent.com/96860670/154978691-5d4a2b54-b615-4e7f-ad38-6c27d75148f4.png" alt="" width="250px"/>

.thankyou 다음의 **바로 인접한 하나의** 형제 태그(li)에 스타일을 부여한다.

## 참고자료 (reference)

[CSS 선택자 (Selector) - 조합 선택자 (자식, 자손, 형제)](https://amaze9001.tistory.com/45)  
[CSS Combinators](https://www.w3schools.com/css/css_combinators.asp)  
[General sibling combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_combinator)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
