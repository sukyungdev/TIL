# table tag

table tag에 관해 정리해 보았다.

---

## table tag?

**표**를 만들기 위한 태그.
<img src="https://user-images.githubusercontent.com/96860670/153883841-640fd1b1-b35d-419c-a17e-c59491df6752.png" alt=""  width="500px"/>

일단 표를 만들고 싶다면 &lt;table&gt;로 표를 만들기 시작한다.

## table 태그 안에 들어가는 태그

### 1. tr

테이블 가로줄(한줄)을 만드는 태그.

### 2. th

테이블 헤더를 만드는 태그.

### 3. td

테이블의 한 칸(셀)에 데이터를 넣는 태그.

> 열을 만드는 태그라고 이해하면 쉬울 것 같다.

기본적으로 table 태그로 표의 시작을 알리고, tr 태그로  
가로줄 한줄을 만든 다음, 표의 구조에 맞춰서 th와 td 태그로  
데이터를 넣어준다.

```html
<table>
  <tr>
    <th>제목1</th>
    <th>제목2</th>
    <th>제목3</th>
  </tr>
  <tr>
    <td>번호1</td>
    <td>내용1.1</td>
    <td>내용1.2</td>
  </tr>
  <tr>
    <td>번호2</td>
    <td>내용2.1</td>
    <td>내용2.2</td>
  </tr>
  <tr>
    <td>번호3</td>
    <td>내용3.1</td>
    <td>내용3.2</td>
  </tr>
</table>
```

결과  
<img src="https://user-images.githubusercontent.com/96860670/153883511-0f37c3c0-0828-41bc-8f09-04c0b9b8f03b.png" width="300px"/>

### 4. thead

테이블 헤더라는 것을 강조하는 명시적인 역할의 태그.

### 5.tbody

테이블의 데이터 부분을 강조하는 명시적인 역할의 태그.

### 6.tfoot

테이블의 총합 부분을 강조하는 명시적인 역할의 태그.

> 위의 태그들은 구조적으로 테이블을 만드는 것에 도움이 된다.

```html
<table>
  <thead>
    <tr>
      <th>제목1</th>
      <th>제목2</th>
      <th>제목3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>번호1</td>
      <td>내용1.1</td>
      <td>내용1.2</td>
    </tr>
    <tr>
      <td>번호2</td>
      <td>내용2.1</td>
      <td>내용2.2</td>
    </tr>
    <tr>
      <td>번호3</td>
      <td>내용3.1</td>
      <td>내용3.2</td>
    </tr>
  </tbody>
</table>
```

---

## 내용이 없을 경우

만약 테이블 셀의 내용이 없다고 해도 테이블 셀은  
테이블 헤더 개수에 맞춰 만들어야 한다.

```html
<table>
  <thead>
    <tr>
      <th>제목1</th>
      <th>제목2</th>
      <th>제목3</th>
      <th>제목4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>번호1</td>
      <td>내용1.1</td>
      <td>내용1.2</td>
      <td>내용1.3</td>
    </tr>
    <tr>
      <td>번호2</td>
      <td>내용2.1</td>
      <td>내용2.2</td>
      <td>내용2.3</td>
    </tr>
    <tr>
      <td>번호3</td>
      <td>내용3.1</td>
      <td>내용3.2</td>
      <td></td>
    </tr>
  </tbody>
</table>
```

결과  
<img src="https://user-images.githubusercontent.com/96860670/153884083-b8042112-a300-4705-b189-95e2e137cfcf.png" alt=""  width="300px"/>
