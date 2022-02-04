# 그외 태그

## abbr 태그

> 부가적인 설명을 위한 태그. 줄임말 태그.
> 설명을 하고 싶은 용어(약자)에 사용한다.

```html
<p>
  <abbr title="United States">U.S</abbr>
</p>
```

title 속성에 약자의 설명을 써놓으면 커서를 올렸을 때
설명이 나타난다.

## pre 태그

> 텍스트에 사용된 여백과 줄바꿈이 모두 나타나는 태그.

```html
<pre>
  안녕 
     하세 요.
</pre>
```

따로 <br />태그를 사용하지 않고도 여백과 줄바꿈이  
그대로 나타난다.

## code 태그

> code를 사용하기 위한 태그.

```html
<code>var a = 2;</code>
```

code 태그를 pre 태그로 감싸서 사용하는 경우가 많다.

- 코드는 띄어쓰기가 중요하기 때문이다.
- 여러줄의 코드를 사용할 경우 pre 태그로 감싸서
  사용하는 것이 좋다.

[<code>: 인라인 코드 요소](https://developer.mozilla.org/ko/docs/Web/HTML/Element/code)
