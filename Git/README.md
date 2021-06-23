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