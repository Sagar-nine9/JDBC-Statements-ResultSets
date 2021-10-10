# JDBC-Statements-ResultSets


JDBC stands for Java Database Connectivity. JDBC is a Java API to connect and execute the query with the database. It is a part of JavaSE (Java Standard Edition). JDBC API uses JDBC drivers to connect with the database. There are four types of JDBC drivers:

JDBC-ODBC Bridge Driver,
Native Driver,
Network Protocol Driver, and
Thin Driver


Example of statement interface
import java.sql.*;  
class FetchRecord{  
public static void main(String args[])throws Exception{  
Class.forName("oracle.jdbc.driver.OracleDriver");  
Connection con=DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe","system","oracle");  
Statement stmt=con.createStatement();  
  
//stmt.executeUpdate("insert into emp765 values(33,'Irfan',50000)");  
//int result=stmt.executeUpdate("update emp765 set name='Vimal',salary=10000 where id=33");  
int result=stmt.executeUpdate("delete from emp765 where id=33");  
System.out.println(result+" records affected");  
con.close();  
}}  
