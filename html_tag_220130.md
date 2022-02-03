# form 태그

> 사용자에게 어떠한 입력(input)을 받기 위한 태그.
> 다양한 속성이 존재한다.

- action : input값을 처리하기 위해 필요한 주소(백엔드)값을 넣는 속성
- method : input 값을 서버에 전송할 http 메소드
  [HTML:폼(form)이해](https://www.nextree.co.kr/p8428/)

추가> 
[form 태그와 input 태그의 관계](https://github.com/sukyungdev/TIL/blob/main/form_and_input.md)

## 1. input 태그

> 사용자에게 input을 받기 위한 창(필드,입력창)를 생성하는 태그.  
> type이란 속성을 꼭 이용하자!(받고싶은 정보에 알맞은 창이 생성된다)  
> 종료태그가 없다.

### 1.1 input 태그의 다양한 속성

- type : 정보의 특성에 어울리는 형태의 창 생성
- placeholder : input 태그에 사용자에 무엇도 입력하지  
  않았을 때 나타나는 설명 문구
- minlenght : 입력값의 최소 문자길이 설정
- maxlenght : 입력값의 최대 문자길이 설정
- required : 사용자가 인풋값을 비우고 다음 단계로  
  넘어가지 못하도록 설정
  ***

- disabled : 특정 인풋태그를 사용 불가로 만든다.
- value : input 태그 안에 값을 넣어 둔다.(복사 가능)
  > placeholder와는 다른 속성이다. placeholder는 텍스트가 아닌  
  > 말 그대로 보이기만 하는 안내 문구이다. 그러나 value는 텍스트로  
  > input 창 안에 값으로 들어가 있다.

### 1.2 input type속성의 다양한 속성값

값을 효율적으로 받기 위해서 값에 알맞은 다양한 type 속성값이 있다.

```html
<input type="email" />
```

email을 입력받기 위한 속성. @를 입력하지 않으면 알려준다.

```html
<input type="password" />
```

password를 입력받기 위한 속성. 사용자가 입력하는 값을 보이지 않도록 처리

```html
<input type="url" />
```

url을 입력받기 위한 속성. url형식이 아니면 알려준다.

```html
<input type="number" />
```

숫자를 입력받기 위한 속성. 숫자가 아니면 입력되지 않는다.

- min 속성 : type이 number 일때 사용가능. 최소값 이상을 입력할 수 없다.
- max 속성 : type이 number 일때 사용가능. 최대값 이상을 입력할 수 없다.

> 글자수가 아닌 값이다!

```html
<input type="file" />
```

파일을 입력받기 위한 속성. 파일을 사용자가 선택해서 업로드 할 수 있다.

- accept 속성 : 파일의 확장자 지정 가능.

## 2. label 태그

> form 태그의 자식 태그(요소)에 이름을 붙이는 태그.  
> 사용자 편의를 위해서 사용된다.  
> for 속성을 이용해서 이름을 붙이고 싶은 요소와 연결시킬 수 있다.

이름을 붙이고 싶은 요소와 id값이 같아야 하며, for 속성을 이용해서 결합한다.  
label 태그를 클릭하면, 연결된 요소에 포커싱이 된다.

> 주로 input 태그에 많이 사용되는 것 같다.

```html
<label for="name">이름</label>
<input type="text" id="name" />
```
## 2. select 태그

> drop down menu 양식을 만들기 위한 태그.  
> 자식태그 option 태그를 이용해서 drop down 메뉴를 만들 수 있다.

```html
<select>
  <option>선택1</option>
  <option>선택2</option>
  <option>선택3</option>
</select>
```

관련 속성

- name : radio 태그처럼 같은 그룹이라는 것을 나타내는 속성.  
  select 태그에만 적용해도 된다.
- value : 서버에 어떤 선택지가 선택되었는지 전송하는 속성. option 태그에 적용.
- multiple : 다중선택을 만들기 위한 속성. select 태그에 적용.

```html
<select name="선택지">
  <option value="1">선택1</option>
  <option value="2">선택2</option>
  <option value="3">선택3</option>
</select>
```

## 2. button 태그

> button을 만들기 위한 태그.
> type 속성을 만드시 넣어줘야 한다.

```html
<button>버튼</button>
```

type 속성 종류

- button : 가장 일반적이고 많이 사용되는 속성.
- submit : form 양식을 제출할때 사용되는 속성.
- reset : 다시쓰기(reset)를 위한 속성.
