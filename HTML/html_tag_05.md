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

[&lt;code&gt;: 인라인 코드 요소](https://developer.mozilla.org/ko/docs/Web/HTML/Element/code)

# script 태그

문서내에 javascript 코드를 입력하거나 파일을 첨부하기 위한 태그.

- javascript 코드 입력

```html
<script>
  코드 작성
</script>
```

- javascript 파일 첨부

```html
<script src="파일 주소 입력"></script>
```

> css처럼 문서내에 직접 javascript 코드를 입력하는 것 보다  
> 외부 파일을 첨부하는 방식이 더 효율적이고, 수정이 쉽다.

**script 태그는 body 태그 내부에서 가장 아래에 작성하는 것이 좋다.**

> script 태그(javascript)는 구동에 시간이 걸린다.(구동 시간 동안 정지)  
> 때문에 효율적인 코드를 위하여 body 태그 맨 아래에 작성한다.

[HTML에 자바스크립트를 연결하는 세 가지 방법](https://oneroomtable.tistory.com/entry/HTML%EC%97%90-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%A5%BC-%EC%B6%94%EA%B0%80%ED%95%98%EB%8A%94-%EC%84%B8-%EA%B0%80%EC%A7%80-%EB%B0%A9%EB%B2%95-script-%ED%83%9C%EA%B7%B8-%EC%84%A4%EB%AA%85)  
[script 태그는 어디에 위치해야 할까요?](https://velog.io/@takeknowledge/script-%ED%83%9C%EA%B7%B8%EB%8A%94-%EC%96%B4%EB%94%94%EC%97%90-%EC%9C%84%EC%B9%98%ED%95%B4%EC%95%BC-%ED%95%A0%EA%B9%8C%EC%9A%94)

