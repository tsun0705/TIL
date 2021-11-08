## SELECT > FROM > WHERE > GROUP BY > HAVING > ORDER BY

## ORDER BY
* ASC (오름차순), DESC (내림차순)   
* 생략시 오름차순
* 이름을 기준으로 역순으로 정렬
~~~
SELECT * FROM MEMBER ORDER BY NAME DESC;
~~~
* 회원중에서 '박'씨 성을 가진 회원을 조회 (나이를 오름차순으로 정렬)
~~~
SELELCT * FROM MEMBER WHERE NAME LIKE '박%' ORDER BY AGE ASC;
~~~
