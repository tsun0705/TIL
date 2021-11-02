## INSERT
* 데이터 삽입하기
~~~
-- INSERT 규칙
INSERT INTO 테이블 VALUES 값 목록 

-- 모든 필드 값을 입력하기
INSERT INTO MEMBER VALUES('abc', '123', '홍길동' , '남성', '1996-01-01', '010-1111-1111', 'abc@naver.com', '2021-11-02'); 

-- 원하는 필드만, 원하는 순서대로 입력하기
INSERT INTO MEMBER(ID, PWD) VALUES('abc', '123');
빈 칸은 NULL 값
~~~

## SELECT
* 데이터 출력하기
~~~
-- 멤버 테이블 모든 컬럼 출력
SELECT * FROM MEMBER; 

-- 원하는 컬럼 출력
SELECT ID, NAME, PWD FROM MEMBER;

-- 원하는 컬럼명으로 출력 (as 생략 가능) & 빈 공백 포함 시 "USER ID"
SELECT ID as USER_ID, NAME, PWD FROM MEMBER;
~~~

## UPDATE
* 데이터 수정하기
* WHERE절이랑 같이 사용
~~~
-- 모든 행의 PWD를 '111'로 변경하기
UPDATE MEMBER SET PWD='111'; 

-- WHERE절이랑 같이 사용해야함
UPDATE MEMBER SET PWD='333', NAME='손오공' WHERE ID='dragon';
~~~

## DELETE
* 데이터 삭제하기
* WHERE절이랑 같이 사용
~~~
DELETE MEMBER WHERE ID='dragon';
~~~
