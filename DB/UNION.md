## UNION ALL
* 테이블 간의 레코드를 합치는 작업
* 컬럼의 개수와 자료형을 맞춰야 한다.
~~~
SELECT ID, NAME FROM MEMBER 
UNION ALL
SELECT WRITER_ID, TITLE FROM NOTICE;
~~~

## UNION
* 테이블 간 레코드를 합치는 작업, 중복 값 제거
* 컬럼의 개수와 자료형을 맞춰야 한다.
~~~
SELECT ID, NAME FROM MEMBER 
UNION 
SELECT WRITER_ID, TITLE FROM NOTICE;
~~~

## MINUS
* 왼쪽 테이블에서 오른쪽 테이블 레코드를 제거
* 컬럼의 개수와 자료형을 맞춰야 한다.
~~~
SELECT ID, NAME FROM MEMBER 
MINUS
SELECT WRITER_ID, TITLE FROM NOTICE;
~~~

## INTERSECT
* 공통 분모를 출력한다.
* 컬럼의 개수와 자료형을 맞춰야 한다.
* ~~~
SELECT ID, NAME FROM MEMBER 
INTERSECT
SELECT WRITER_ID, TITLE FROM NOTICE;
~~~
