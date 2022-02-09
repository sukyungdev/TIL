# WAI-ARIA and alt

WAI-ARIA 와 alt 속성에 관해 알아보았다.

---

## ARIA 란 무엇인가?

간단하게 설명하면 웹 환경에서 사용자들의 접근성을 높이기 위한 규칙  
(표준 기술 규격)이다.

- 왜 사용하는가?  
  스크린리더 및 보조기기 등에서 의미를 추가하여  
  접근성을 향상시키기 위해서 사용한다.  
  사용자의 조건을 차별하지 않고 동등한 웹서비스를  
  제공하기 위한 사용자 친화적 기술이다.

[ARIA](https://developer.mozilla.org/ko/docs/Web/Accessibility/ARIA)  
[WAI-ARIA 웹퍼블리싱](https://www.biew.co.kr/entry/WAI-ARIA-%EC%9B%B9%ED%8D%BC%EB%B8%94%EB%A6%AC%EC%8B%B1)  
[WAI-ARIA란?](https://story.pxd.co.kr/1588)

```html
<strong aria-label="검색 돋보기">검색 돋보기</strong>
```

> 이번에 알게 된 것인데 ARIA의 기능이 상당이 많다.  
> 위의 예시는 ARIA기능의 아주 일부이다.

---

그렇다면ARIA와 alt의 차이는 무엇인가? 라는 생각이 들었다.  
alt태그도 스크린리더에서 사용할 수 있고, 접근성을 위해 사용된다.  
그렇다면 동시에 사용해도 되는 것일까?

## alt 란 무엇인가?

img 태그에서 사용되며, 이미지가 나타나지 못할 때나, 스크린 리더등 이미지가  
나타나지 못할때 해당 이미지의 **대체 텍스트**로 사용되는 속성이다.

즉 alt는 **img 태그에서** 사용되는 속성이다.  
만일 img 태그에서 alt태그를 사용하는 경우 ARIA는 생략해도 괜찮을것 같다.

> 참고로 alt태그를 사용하지 않는 경우에도 alt="" 이렇게 사용해야 한다.

[alt 속성](https://ko.wikipedia.org/wiki/Alt_%EC%86%8D%EC%84%B1)  
[&lt;img&gt; 태그의 alt 속성](http://tcpschool.com/html-tag-attrs/img-alt)

## 참고자료 (reference)

[ARIA](https://developer.mozilla.org/ko/docs/Web/Accessibility/ARIA)  
[WAI-ARIA 웹퍼블리싱](https://www.biew.co.kr/entry/WAI-ARIA-%EC%9B%B9%ED%8D%BC%EB%B8%94%EB%A6%AC%EC%8B%B1)  
[WAI-ARIA란?](https://story.pxd.co.kr/1588)  
[alt 속성](https://ko.wikipedia.org/wiki/Alt_%EC%86%8D%EC%84%B1)  
[&lt;img&gt; 태그의 alt 속성](http://tcpschool.com/html-tag-attrs/img-alt)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
