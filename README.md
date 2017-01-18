# Jdbc_Coding
Writing connection code

import java.sql.*;
public class JavaTest
{
public static void main(String[] args)throws Exception
{
Driver d=new OraclecJdbcDriver;
DriverManager.registerDriver(d);
Connection con=DriverManager.getConnection("Jdbc:Oracle:thin:@localhost:8080:xe","system","manager");
Statement st=con.createStatement();
String ddl="create table Emp(Id number(5),Name varchar2(30))";
st.execute(ddl);
string dmlinsert="insert into Emp values(1,"Tauseef")";
st.executeQuery(dmlinsert);
con.close();
