# Git 기록하기
1. Git bash를 이용하여 세팅해주자
- git config -- 계정정보 설정

- git config --global user.name "계정"

- git config --global user.email 이메일

- git init -- 깃 초기화

- git add . -- 로컬 저장소커밋 (.띄어쓰기 해야함)

- git commit -m "First commit   --커밋

- git remote add origin #URL#  -- Repository 등록

- git push -u origin master  -- git push

2. VsCode에서 커밋하고 git에서 확인 했을때 한글이 깨질 경우
- 간혹 cmd가 문제일때 나타나며 해결 방법으로는 cmd열고 set_LC_ALL = ko_KR. UTF-8을 치고 다시 커밋하면 잘 된다.


3. 마크다운 문법
- 헤더 (Header)
```
===, ---, #
```

- 강조 ()
```
**굵은 글씨**
~~취소선~~
`강조할 단어`
```

- 소스코드 블럭
```
- ```
```

- 링크
```
링크를 괄호로 감싸준다.
```

- 목록
```
1.,  * 
```

- 수평선
```
* * *

***

*****

- - -

---------------------------------------
```

4. git 현재 연결된 repository url 확인
- git remote -v

5. git push 취소하기
  1. git reset HEAD^       //가장 최근 commit 취소
  2. git commit -m "message"   // 다시 커밋
  3. git push -f origin branchname

6. git 과거에 일어난일 되돌리는 방법
  1. reset - 과거 시간으로 되돌리기
    1. hard옵션 - 돌아가려는 이력 이후의 모든내용 지워버림 
    2. soft옵션 - 돌아가려는 이력 이후의 내용 유지 git add 된 상태
    3. mixed옵션 - 돌아가려는 이력 이후의 내용 유지 하는데 git add는 안된 상태
  2. revert - 특정 기록을 없던일로 만들기
  - push를 한 상태라면 revert를 사용해야함! (내 로컬git만 과거로 돌아가기 때문)
    