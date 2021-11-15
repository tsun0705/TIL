## Data Dictionary
* 데이터베이스 자원을 효율적으로 관리하기 위한 다양한 정보를 저장하는 테이블

## Data Dictionary View
* 데이터 사전의 내용을 사용자가 이해할 수 있는 내용으로 변환하여 제공
* USER_XXX, ALL_XXX, DBA_XXX 등으로 내용 검색

~~~
SELECT * FROM USER_TABLE
SELECT * FROM USER_TAB_COLUMNS WHERE TABLE_NAME = 'MEMBER';
~~~
