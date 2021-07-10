# DB
1. 오라클 날짜타입
- data -> string 타입으로 바꾸기
-  타입 바꿔서 비교 예시 TO_CHAR(column,'YYYYMMDD')> 20210430

2. 컬럼에 있는 내용 중 숫자만 뽑기
- select regexp_replace(column,'[^0-9]') as AliasName from TableName

3. Group by로 중복 찾기
```
SELECT COLUMN_NAME , COUNT(*) FROM TABLE_NAME GROUP BY COLUMN_NAME HAVING COUNT(*) > 1 ;
```

4. mysql 유저생성, 권한
```
ceate user USER_ID@localhost identified by 'USER_PASSWORD';
grant all privileges on DATABASE_NAME.* to USER_ID@localhost;
```

5. Oracle 용량
```
  1. select sum(bytes)/1024/1024/1024 ||'GB' from dba_data_files;  -- 전체용량
  2. select sum(bytes)/1024/1024/1024 ||'GB' from dba_segments;    -- 사용중
  3. select sum(bytes)/1024/1024/1024 ||'GB' from dba_free_space;  -- 잔여량
```

6. Oracle 테이블 복사
    1) 구조만 복사
```
create table table_name_copy as select * from table_name where 1=2;
```

    2) 구조와 로우 복사

```
create table table_name_copy as select * from table_name;
```

7. TRUNCATE
- delete와 유사한 것으로 차이점은 로그를 쌓지 않아 속도가 빠름
- 복구불가 확실한 것만 해야함
- ex)
```
TRUNCATE table table_name;
```
