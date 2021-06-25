# DB
1. ����Ŭ ��¥Ÿ��
- data -> string Ÿ������ �ٲٱ�
-  Ÿ�� �ٲ㼭 �� ���� TO_CHAR(column,'YYYYMMDD')> 20210430

2. �÷��� �ִ� ���� �� ���ڸ� �̱�
- select regexp_replace(column,'[^0-9]') as AliasName from TableName

3. Group by�� �ߺ� ã��
```
SELECT COLUMN_NAME , COUNT(*) FROM TABLE_NAME GROUP BY COLUMN_NAME HAVING COUNT(*) > 1 ;
```

4. mysql ��������, ����
```
ceate user USER_ID@localhost identified by 'USER_PASSWORD';
grant all privileges on DATABASE_NAME.* to USER_ID@localhost;
```

5. Oracle �뷮
```
  1. select sum(bytes)/1024/1024/1024 ||'GB' from dba_data_files;  -- ��ü�뷮
  2. select sum(bytes)/1024/1024/1024 ||'GB' from dba_segments;    -- �����
  3. select sum(bytes)/1024/1024/1024 ||'GB' from dba_free_space;  -- �ܿ���
```