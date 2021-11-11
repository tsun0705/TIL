## SELF JOIN
* 자기와 자기가 합쳐지는 조인
* 데이터가 서로 포함 관계를 갖는 경우
~~~
SELECT M.*, B.NAME BOSS_NAME FROM MEMBER M LEFT OUTER JOIN MEMBER B ON B.ID = M.BOSS_ID;
~~~
