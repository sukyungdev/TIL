# git branch merge 하기

git branch는 merge(병합)이 가능하고, default branch를 change 할 수 있다.  
방법은 생각보다 간단하다.

---

## git branch merges

우선 현재 branch를 확인한다.

```
git branch
```

그다음 합치고 싶은 branch로 바꾼다.

```
git checkout <합치고 싶은 branch 이름>
```

> 만약 main 브랜치에 test 브랜치를 병합하고 싶으면  
> git checkout main 이렇게 입력해야 한다.

병합하고 싶은 브랜치를 병합한다.

```
git merge <합쳐지는 branch 이름>
```

> main 브랜치에 test 브랜치를 병합하고 싶으면  
> git merge test 이렇게 입력해야 한다.

마지막으로 git push를 하면 merge가 완료된다.

```
git push
```

## github default branch change

default branch를 바꿀수 있다.  
repository - Settings - Branches - Default Branch
![](https://user-images.githubusercontent.com/96860670/150489583-37c40130-13c5-4133-b424-a033e0176076.png)
파란색 원 부분의 화살표를 클릭하면 default branch를 바꿀수 있다.

## 참고자료 (reference)

[[Git] 5. Branch 병합하기](https://keepmind.net/branch-%EB%B3%91%ED%95%A9%ED%95%98%EA%B8%B0/)
[[Git] GitHub의 Default 브랜치(Branch) 변경하기](https://redcow77.tistory.com/454)

---

> 틀린점, 오타에 대한 것은 언제든지 알려주세요!
