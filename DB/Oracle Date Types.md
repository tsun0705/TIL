## Character 형식
~~~
'nEWlec'
'A'
'123'
~~~
* CHAR(n) : 고정된 문자열, size : 1byte
* VARCHAR2(n) : 가변 길이 문자열, 최대 n만큼 크기를 갖을 수 있다, size : 1byte
* NCHAR(n) : 전 세계 문자 표현, size : 2~3 byte / n개의 문자 입력 가능 
* NVARCHAR2(n) : 전 세계 문자 표현, size : 2~3 byte
* LONG
* CLOB : 대용량 텍스트 데이터 (최대 4G)
* NCLOB : 대용량 텍스트 유니코드 데이터 (최대 4G)

## Numeric 형식
~~~
38
3.85
3.85F
137
~~~
* NUMBER(n) : 최대 n자리로 이루어진 숫자
* NUMBER(n,2) : 소수점 2자리를 포함한 최대 n자리 숫자
* NUMBER(n,-2) : 소수점 -2자리에서 반올림하는 최대 n자리 숫자
* NUMBER : NUMBER(38,*)
* NUMBER(*,5) : NUMBER(38,5)

## Date 형식
~~~
'2021-11-02'
~~~
* 연도, 월, 일 표시


## TIMESTAMP
~~~
'2021-11-02 10.40.25.0000'
~~~
* 연도, 월, 일, 시간 표시


## byte
* 영어 1문자 = 1byte
* 그 외 다른 세계 1문자 = 3byte
