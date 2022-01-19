# git add -A 와 git add .의 차이

> git 관련 공부를 하다 git add -A와 git add . 의 차이가 궁금해졌다.  
> 찾아보니 스택오버플로우에 같은 질문을 하신 분이 있었다.

---

## 질문에 달린 답변

[Difference between "git add -A" and "git add ."](https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add)

> git version에 따라 조금 달라지는 것 같다. 최신 버전을 기준으로 작성하겠다.

즉 간단하게 정리하자면

- git add -A : 수정된 파일, 삭제된 파일, 새로운(new) 파일 모든 stage area로 이동.

- git add . : 수정된 파일, 삭제된 파일, 새로운(new) 파일 모든 stage area로 이동.
  > git add . 같은 경우는 version 1.~ 에서는 삭제된 파일은 stage 하지 않았으나  
  > version 2.~ 부터는 git add -A와 거의 같은 역할을 하는 듯하다.
- git add --ignore-removal . : 삭제된 파일을 제외하고 stage area로 이동.
- git add -u : 새로 생성된 파일을 제외하고 stage area로 이동.

내가 한 작업에 따라 적절히 사용하면 좋을 것 같다.

## 참고자료 (reference)

[Difference between "git add -A" and "git add ."](https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
