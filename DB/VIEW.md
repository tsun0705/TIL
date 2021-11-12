## VIEW
* 쿼리의 실행 결과를 화면에 저장하는 논리적 가상 케이블이다.
* 보안 및 정보 조회 편의성 향상

## VIEW OPTION
* OR REPLACE - 이미 존재한 뷰일 경우 뷰를 갱신
* WITH READ ONLY - 읽기 전용으로 생성하여 조회만 가능
***

* VIEW 생성
~~~
CREATE [OR REPLACE] VIEW 뷰이름 AS 서브쿼리 [WITH READ ONLY]
~~~

* VIEW 수정
~~~
UPDATE 뷰이름 SET 변경할 컬럼 = 변경할 값 WHERE 조건
~~~
