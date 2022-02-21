<head> 태그 안에서 사용되는 태그.

---

# meta 태그

meta 태그란?

- <head></head> 태그 사이에 오는 태그.
- 직접적으로 보이지는 않지만, 문서의 정보나 설정을
  담고 있다.(metadata)

## meta 태그의 속성.

- charset : 문서의 문자 인코딩 방식 지정.
- name : 어떤 정보(metadata)의 형태인지 정보의 이름을 명시.
- content : 실제 metadata의 컨텐츠(값).

[head 태그에는 무엇이 있을까? HTML의 메타데이터](https://developer.mozilla.org/ko/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)
[HTML <meta> 태그 기초](https://blogpack.tistory.com/1067)

```html
<meta charset="UTF-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta name="description" content="" />
```

> description 속성은 SEO를 위해 정확한 설명을 써주는 것이 좋다.  
> name 속성을 사용하면, content 속성도 사용해야 한다.

# title 태그

웹 브라우저의 탭에서 나타내는 제목을 설정하는 태그.

```html
<title>Hello World</title>
```

[<title> 태그](https://ofcourse.kr/html-course/title-%ED%83%9C%EA%B7%B8)

# link 태그

문서에 다른 문서를 input하기 위해 사용하는 태그.  
주로 css 문서를 input 하기 위해 사용한다.

```html
<link rel="stylesheet" href="./스타일시트_주소_입력하기" />
```

[HTML <link> 태그](http://www.tcpschool.com/html-tags/link)

# style 태그

문서에 style을 적용하기 위한 태그.(내부 css)

> 내부 css를 사용하는 방법은 비추천한다.
> link 태그를 사용해 css를 적용하는 방법이 더 효율적이고, 추후 수정에도 간편하다.
