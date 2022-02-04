# Media 태그

> 오디오와 비디오, 이미지등 미디어를 input하기 위한 태그.

## 1. audio 태그

> 오디오를 넣기 위한 태그.

### 1.1 audio 태그 사용방법 01

```html
<audio src=""></audio>
```

src라는 넣고 싶은 오디오 파일의 주소가 꼭 필요하다.

_관련속성_

- controls : 오디오 컨트롤 속성 만들기
- autoplay : 오디오 자동재생
  > 2022.02월 기준 현재 chrome이 audio 자동재생을 막아놓았다.
  > audio를 자동재생 하기 위해서는 다른 방법이 필요한 것 같다.

### 1.2 audio 태그 사용방법 02

```html
<audio>
  <source src="주소적기" type="audio/wav" />
  <source src="주소적기" type="audio/mpeg" />
  <source src="주소적기" type="audio/ogg" />
</audio>
```

src와 type이라는 속성을 꼭 적이줘야 한다.
이쪽이 좀더 안정적인 방법이다.

_왜 안정적인 방법일까?_

웹 브라우저마다 지원하는 오디오 인코딩 방식이 다르기 때문이다!  
02의 방법을 쓰면 웹 브라우저 방식마다 맞춰 알맞은 인코딩 방식의  
오디오를 재생할 수 있다.

## 1. video 태그

> 오디오 태그와 방식이 똑같다.

### 1.1 audio 태그 사용방법 01

```html
<video src=""></video>
```

_관련속성_

- controls : 비디오 컨트롤 속성 만들기
- autoplay : 비디오 자동재생
  > 2022.02월 기준 현재 video 태그는 autoplay를 이용한  
  > 자동재생이 정상적으로 작동한다.

### 1.2 audio 태그 사용방법 02

```html
<audio>
  <source src="주소적기" type="audio/wav" />
  <source src="주소적기" type="audio/mpeg" />
  <source src="주소적기" type="audio/ogg" />
</audio>
```

오디오 태그와 같은 이유로 사용방법 02가 좀 더 안정적이다.
