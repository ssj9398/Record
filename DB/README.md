# DB
1. ����Ŭ ��¥Ÿ��
- data -> string Ÿ������ �ٲٱ�
-  Ÿ�� �ٲ㼭 �� ���� TO_CHAR(column,'YYYYMMDD')> 20210430

2. �÷��� �ִ� ���� �� ���ڸ� �̱�
- select regexp_replace(column,'[^0-9]') as AliasName from TableName