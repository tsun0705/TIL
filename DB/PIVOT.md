## PIVOT
* 행을 열로 변환해주는 함수
* 그룹함수는 SUM(), AVG(), COUNT() 등 컬럼을 묶어주는 함수들을 사용
~~~
SELECT *
  FROM ( 피벗 대상 쿼리문 )
 PIVOT ( 그룹합수(집계컬럼) FOR 피벗컬럼 IN (피벗컬럼값 AS 별칭 ... )
~~~
