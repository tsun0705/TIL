~~~
ResultSet rs = st.executeQuery(sql); -- SELECT

int rs = st.executeUpdate(sql); -- INSERT, UPDATE, DELETE 등 조작
~~~
***
~~~
String title = "TEST2"
String writeID = "newlec"
String content = "hahaha"
String file = "";



String url = "jdbc:oracle:thin:@localhost:포트/서비스이름";
String sql = "INSERT INTO NOTICE ( "+" title, "+" wirte_id, "+" content, "+" files "+") VALUES (?, ?, ?, ?)";

Class.forName("oracle.jdbc.driver.OracleDriver");
Connection con = DriverManager.getConnection(url, "ID", "PW");
PreparedStatement st = con.preparedStatement(sql);
st.setString(1, title);
st.setString(2, writeID);
st.setString(3, content);
st.setString(4, files);

int result = st.executeUpdate();

System.out.println(result);

st.close();
con.close();

-- 출력 값 : 1
~~~
