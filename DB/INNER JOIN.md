## INNER JOIN
* 참조키를 기준으로 일치하는 행만 조인
* 서로 관계가 있는 레코드는 INNER 관계가 없는 레코드는 OUTER
~~~
SELECT * FROM MEMBER INNER JOIN NOTICE ON MEMBER.ID = NOTICE.WRITER_ID
~~~

* 컬럼을 지정하는 식별자를 줄이기 위해서 테이블의 별칭을 사용
~~~
SELECT N.ID, N.WRITER_ID, M.NAME FROM MEMBER M INNER JOIN NOTICE N ON M.ID = N.WRITER_ID
~~~
