## 집계 함수
* COUNT, SUM, MIN, MAX, AVG
***

[코드]
~~~
SELECT COUNT(ID) FROM NOTICE;
~~~
[결과]   
![image](https://user-images.githubusercontent.com/58898466/140885682-9509b9b9-4f2e-446d-a207-5f5785b5b768.png)


* 위의 결과는 레코드의 전체 개수를 알려주는 단일 값을 반환한다.
* 만약에 작성자 별로 묶어서 개수를 집계하고 싶다면 그 때 GROUP BY 절을 사용할 수 있다.

 ***

[코드]
~~~
SELECT COUNT(ID) FROM NOTICE GROUP BY WRITER_ID;
~~~
[결과]   
![image](https://user-images.githubusercontent.com/58898466/140886557-0a2d5960-05fd-4885-9302-960263232ee5.png)

* 이렇게 작성자별로 묶어서 개수를 집계하게 되면 단일 값이 아니라 각 작성자별 게시글 개수가 나오기 때문에 목록이 출력된다.
* 그 목록에서 집계된 내용이 각각 어떤 작성자의 게시글 수인지를 알고 싶다면 SELECT 절에 GROUP BY 절에 사용된 기준 필드를 같이 출력할 수 있다.

 ***

[코드]
~~~
SELECT WRITER_ID, COUNT(ID) FROM NOTICE GROUP BY WRITER_ID;
~~~
[결과]   
![image](https://user-images.githubusercontent.com/58898466/140886570-9d813a73-5f9e-47ff-836f-647fc5e8e322.png)

* 그리고 마지막으로 위의 결과에서 컬럼명에 집계함수가 사용되는 것은 그 결과를 프로그래밍에서 사용할 때는 불편하므로 별칭을 COUNT로 해서 쿼리를 만들면 작성자별로 묶은 집계값 완전하게 만들어진다.

 ***

[코드]
~~~
SELECT WRITER_ID, COUNT(ID) COUNT FROM NOTICE GROUP BY WRITER_ID;
~~~
[결과]   
![image](https://user-images.githubusercontent.com/58898466/140886587-7a55961f-90b4-472e-b326-6e86f852e874.png)

***

## 실행 순서
* FROM > CONNECT BY > WHERE > GROUP BY > HAVING > SELECT > ORDER BY
