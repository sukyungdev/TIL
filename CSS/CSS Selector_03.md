# CSS Selector_03

Structural Pseudo-Classes Selector(구조적 가상 클래스 선택자)

구조적 가상 클래스 선택자?  
어떤 상태와 조건을 만족할때 사용하는 클래스 선택자.  
**특정 위치에 있는 요소를 선택할 수 있다.**

구조적 가상 클래스 선택자의 종류  
[구조 의사 클래스](http://www.tcpschool.com/css/css_selector_structure)

# 많이 사용하는 구조적 가장 클래스 선택자

## :first-child Selector

부모의 child 요소들중 첫번째 요소를 선택하는 선택자 (형제 요소중 가장 첫번째 요소)

```html
<section>
  <ul>
    <li>1 one</li>
    <li>2 two</li>
    <li>3 three</li>
    <li>4 four</li>
    <li>5 five</li>
  </ul>
</section>
```

```css
/* tagname:first-child */
li:first-child {
  color: #ff74ba;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155157353-14683a86-0d9e-4396-afe8-380b626cbc52.png" alt="" width="100px"/>

## :last-child Selector

부모의 child 요소들중 마지막 요소를 선택하는 선택자 (형제 요소중 가장 마지막 요소)

```html
<section>
  <ul>
    <li>1 one</li>
    <li>2 two</li>
    <li>3 three</li>
    <li>4 four</li>
    <li>5 five</li>
  </ul>
</section>
```

```css
/* tagname:last-child */
li:last-child {
  color: #23ff86;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155157431-afbd44dc-bb04-41e0-a961-8ae46ebf9619.png" alt="" width="100px"/>

## nth-child Selector

부모의 child 요소들중 n번째 요소를 선택하는 선택자 (형제 요소중 n번째 요소)

```html
<section>
  <ul>
    <li>1 one</li>
    <li>2 two</li>
    <li>3 three</li>
    <li>4 four</li>
    <li>5 five</li>
  </ul>
</section>
```

```css
/* tagname:nth-child(n) */
li:nth-child(3) {
  color: #269dff;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155157515-dc168831-9bca-45a1-93f2-cffb3862bf9e.png" alt="" width="100px"/>

nth-child selector는 값에 따른 응용이 가능하다.  
예를들면 홀수 짝수 값에 따라 속성을 다르게 부여할수 있다.

```css
li:nth-child(2n) {
  color: #269dff;
}

li:nth-child(2n-1) {
  color: #ff006a;
}
```

<img src="https://user-images.githubusercontent.com/96860670/155157657-80270210-dded-4648-8963-0c828a963776.png" alt="" width="100px"/>

## 참고자료 (reference)

[구조 의사 클래스](http://www.tcpschool.com/css/css_selector_structure)  
[CSS) nth-child, nth-of-type 다양한 활용방법](https://hi098123.tistory.com/323)  
[[CSS] :Nth-Child() 선택자에 대한 CSS 적용방법, 홀수 및 짝수번째 요소 선택](<https://webisfree.com/2015-10-10/[css]-nth-child()-%EC%84%A0%ED%83%9D%EC%9E%90%EC%97%90-%EB%8C%80%ED%95%9C-css-%EC%A0%81%EC%9A%A9%EB%B0%A9%EB%B2%95-%ED%99%80%EC%88%98-%EB%B0%8F-%EC%A7%9D%EC%88%98%EB%B2%88%EC%A7%B8-%EC%9A%94%EC%86%8C-%EC%84%A0%ED%83%9D>)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
