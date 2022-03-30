# CSS Transition

Transition란?  
Transition 뜻? : 다른 상태, 조건으로의 변화.  
어떤 속성의 값을 서서히 변화시키는 속성.

## Use for Transition

```css
transiton: property duration timing-funcion delay;
/* property와 duration은 필수 */
```

### Property

변화를 줄 CSS 속성을 뜻한다.

```css
transition: background-color;
```

> all을 사용하면 모든 property 선택이 가능하다.

### Duration

지속시간, 변화가 얼마동안 일어나야 하는지

```css
transition: background-color 3000ms;
```

> 단위는 ms, s를 사용(1000ms == 1s)s

### Timing-function

변화가 일어나는 속도의 변화(변화의 리듬)

- ease-in
- ease-out
- ease-in-out
- cubic-bezier(n, n, n, n) - 원하는 리듬을 만들때 사용  
  [cubic-bezier](https://cubic-bezier.com/#.17,.67,.83,.67)

```css
transition: background-color 3000ms ease-in;
```

### Delay

변화가 시작되는 시간을 조정 (딜레이 시킨다.)

```css
transition: background-color 3000ms ease-in 1500ms;
```

### 요소에 각각 transition을 주고 싶을 때

```css
transition: background-color 1000ms, color 2000ms ease-in 500ms;
```

## 참고자료 (reference)

[CSS / 애니메이션 / transition / 속성을 서서히 변화시키는 속성](https://www.codingfactory.net/10953)  
[트랜지션](https://poiemaweb.com/css3-transition)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
