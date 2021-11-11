
* 컬럼을 지정하는 식별자를 줄이기 위해서 테이블의 별칭을 사용
~~~
SELECT N.ID, N.WRITER_ID, M.NAME FROM MEMBER M INNER JOIN NOTICE N ON M.ID = N.WRITER_ID
~~~
