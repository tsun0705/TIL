## LISTAGG
* 여러행의 데이터를 하나의 행에 가로로 출력하기
* 중복 제거 시 서브 쿼리를 이용
~~~
SELECT
       LISTAGG(필드명, 구분자)
       WITHIN GROUP ( ORDER BY 정렬기준필드 ASC 또는 DESC)
FROM 테이블
~~~
*** 
## 예시
~~~
SELECT EMPNO, ENAME, JOB, DEPTNO FROM EMP;
-- 사원 테이블 / 사원원호(EMPNO), 사원명(ENAME), 직책(JOB), DEPTNO(부서번호)
~~~
![image](https://user-images.githubusercontent.com/58898466/149453379-a803c540-9c87-42bf-9fd7-bd80f19e540a.png)
***
~~~
SELECT DEPTNO, ENAME FROM EMP WHERE DEPTNO = 10; 
-- 10번 부서의 사원명
~~~
![image](https://user-images.githubusercontent.com/58898466/149453433-72d8f80d-7c0c-4ae2-b2ce-35646e6ad042.png)
***
~~~
SELECT DEPTNO, ENAME
FROM EMP
GROUP BY DEPTNO, ENAME
ORDER BY DEPTNO, ENAME;
-- 각 부서별 사원명
~~~
![image](https://user-images.githubusercontent.com/58898466/149453610-b8a8f0a7-2f58-455f-a871-d20d9a75e47b.png)
***
~~~
SELECT
       DEPTNO,
       LISTAGG(ENAME, ', ')
       WITHIN GROUP ( ORDER BY ENAME DESC)
       AS ENAMES
FROM EMP
GROUP BY DEPTNO;
--  각 부서별로 속해있는 사원을 한 행으로 출력
~~~
![image](https://user-images.githubusercontent.com/58898466/149453846-f054d1fb-1879-4291-8b65-64050d6eeea1.png)
***

## LISTAGG함수 실행 결과에서 중복 제거하기
~~~
SELECT JOB,
       LISTAGG(DEPTNO, ', ')
       WITHIN GROUP ( ORDER BY DEPTNO)
       AS DEPTS
FROM (
         SELECT DISTINCT JOB, DEPTNO
         FROM EMP
     )
GROUP BY JOB;
~~~
![image](https://user-images.githubusercontent.com/58898466/149454272-3a29a6c4-313e-4365-9a77-63df40e84e4c.png)

