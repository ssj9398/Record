# DB
### 오라클 날짜타입
- data -> string 타입으로 바꾸기
-  타입 바꿔서 비교 예시 TO_CHAR(column,'YYYYMMDD')> 20210430

### 컬럼에 있는 내용 중 숫자만 뽑기
- select regexp_replace(column,'[^0-9]') as AliasName from TableName

### Group by로 중복 찾기
```
SELECT COLUMN_NAME , COUNT(*) FROM TABLE_NAME GROUP BY COLUMN_NAME HAVING COUNT(*) > 1 ;
```

### mysql 유저생성, 권한
```
ceate user USER_ID@localhost identified by 'USER_PASSWORD';
grant all privileges on DATABASE_NAME.* to USER_ID@localhost;
```

### Oracle 용량
```
  1. select sum(bytes)/1024/1024/1024 ||'GB' from dba_data_files;  -- 전체용량
  2. select sum(bytes)/1024/1024/1024 ||'GB' from dba_segments;    -- 사용중
  3. select sum(bytes)/1024/1024/1024 ||'GB' from dba_free_space;  -- 잔여량
```

### Oracle 테이블 복사
#### 구조만 복사
```
create table table_name_copy as select * from table_name where 1=2;
```

#### 구조와 로우 복사

```
create table table_name_copy as select * from table_name;
```

### TRUNCATE
- delete와 유사한 것으로 차이점은 로그를 쌓지 않아 속도가 빠름
- 복구불가 확실한 것만 해야함
- ex)
```
TRUNCATE table table_name;
```

### DB_LINK
#### 전체 DB LINK 조회 쿼리
```
   SELECT * FROM ALL_DB_LINKS;
```
#### DB LINK 생성 방법
```
    CREAE DATABASE LINK "링크명"

    CONNECT TO "계정 ID"

    IDENTIFIED BY "계정 PW";
```
#### DB_LINK 삭제 방법
```
    DROP DATABASE LINK "링크명";
```

#### db Link 동일 서버일 경우

1. 계정 생성
```
 CREATE PUBLIC DATABASE LINK LINK_TEST
CONNECT TO 계정ID IDENTIFIED BY PW USING 'linkTest';
```

2. tnsnames.ora 수정
```
linkTest= 
	(DESCRIPTION= 
  	(ADDRESS_LIST= 
    	(ADDRESS=(PROTOCOL= TCP)(HOST={호스트IP1})(PORT={호스트 포트1})) 
    ) 
    (CONNECT_DATA= 
    	(SERVICE_NAME=orcl) // SID명으로 대체 가능 
    ) 
  )
```
3. 혹시나 안된다면 환경변수 설정 해주기