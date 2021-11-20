## JDBC
* 자바 프로그램 안에서 SQL을 실행하기 위해 데이터베이스를 연결해주는 응용프로그램 인터페이스
***
## JDBC Driver
* 자바에서 제공하는 JDBC 맞춤 구현체
***
## 구동 순서 
* 드라이버 로드하기
* 연결 생성하기
* 문장 연결하기
* 결과집합 사용하기
~~~
Class.forName("oracle.jdbc.driver.OracleDriver");
Connection con = DriverManager.getConnection(...);
Statement st = con.createStatement();
ResultSet rs = st.executeQuery(sql);
rs.next();
String title = rs.getString("title");
~~~
