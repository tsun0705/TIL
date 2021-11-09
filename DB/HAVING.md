## HAVING
* GROUP BY에 조건절을 사용할 수 있다.
* WHERE 절에서는 집계 함수 사용 불가능하기 때문에 HAVING절로 대체
***

* 회원별 게시글 수를 조회 단. 게시글 조회수가 2이하인 레코드만 출력
~~~
SELELCT WRITER_ID, COUNT(ID) FROM MEMBER GROUP BY WRITER_ID HAVING COUNT(ID) <= 2
~~~
