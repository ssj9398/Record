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