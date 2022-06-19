# java2

/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B

Problem Statement - 

Write a java program to write byte into a file.

Objective -  

To understand the concept of FileOutputStream by writing byte into a file.

Explaination -

Java FileOutputStream is an output stream used for writing data to a file.
*/

import java.io.FileOutputStream;  
public class F1 {  
public static void main(String args[]){    
try{    
FileOutputStream fout=new FileOutputStream("D:\\testout.txt");    
fout.write(65);    
fout.close();    
System.out.println("success...");    
}
	   catch(Exception e)
	     {System.out.println(e);}    
}    
}  

/* 
Output -
success...

*/

The content of a text file testout.txt is 

A



/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B

Problem Statement - 

Write a java program to write array bytes into a file.

Objective -  

To understand the concept of FileOutputStream by writing array of bytes into a file.

Explaination -

Java FileOutputStream is an output stream used for writing data to a file. We can also write string into a file by using array of bytes.
*/

import java.io.FileOutputStream;  
public class F2 {  
public static void main(String args[]){    
try{    
FileOutputStream fout=new FileOutputStream("D:\\testout.txt");    
String s="Hello World!";    
byte b[]=s.getBytes();		//converting string into byte array    
fout.write(b);    
fout.close();    
System.out.println("success...");    
}catch(Exception e){System.out.println(e);}    
}    
}  

/* 
Output -
success...

*/

The content of a text file testout.txt is 

Hello World!


/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B

Problem Statement - 

Write a java program to read single character from a file.

Objective -  

To understand the concept of FileInputStream by reading single character from a file.

Explaination -

Java FileInputStream class obtains input bytes from a file. It is used for reading byte-oriented data (streams of raw bytes) such as image data, audio, video etc. We can also read character-stream data.
*/

import java.io.FileInputStream;  
public class F3 {  
public static void main(String args[]){    
try{    
FileInputStream fin=new FileInputStream("D:\\testout.txt");    
int i=fin.read();  
System.out.print((char)i);    
	    fin.close();    
}catch(Exception e){System.out.println(e);}    
}    
}  

/* 
Output -

H

*/

The previous content of a text file testout.txt was 

Hello World!


/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B

Problem Statement - 

Write a java program to read all characters from a file.

Objective -  

To understand the concept of FileInputStream by reading all characters from a file.

Explaination -

Java FileInputStream class obtains input bytes from a file. It is used for reading byte-oriented data (streams of raw bytes) such as image data, audio, video etc. We can also read character-stream data.
*/

import java.io.FileInputStream;  
public class F4 {  
public static void main(String args[]){    
try{    
FileInputStream fin=new FileInputStream("D:\\testout.txt");    
int i=0;    
while((i=fin.read())!=-1){    
System.out.print((char)i);    
}    
fin.close();    
}catch(Exception e){System.out.println(e);}    
}    
}  

/* 
Output -

Hello World!

*/
The previous content of a text file testout.txt was 

Hello World!

/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to write data into a file using BufferedOutputStream.

Objective -  

To understand the concept of BufferedOutputStream by writing data into a file.

Explaination -

Java BufferedOutputStream class is used for buffering an output stream. It internally uses buffer to store data. It adds more efficiency than to write data directly into a stream. So, it makes the performance fast.
*/

import java.io.*;  
public class F5 {    
public static void main(String args[])throws Exception{    
FileOutputStream fout=new FileOutputStream("D:\\testout1.txt");    
BufferedOutputStream bout=new BufferedOutputStream(fout);    
String s="Welcome to Dehradun!";    
byte b[]=s.getBytes();    
bout.write(b);    
bout.flush();    
bout.close();    
fout.close();    
System.out.println("Success");    
}    
}  

/* 
Output -
Success

*/

The content of a text file testout1.txt is

Welcome to Dehradun!
/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to read data of a file using BufferedInputStream.

Objective -  

To understand the concept of BufferedInputStream by reading data from a file.

Explaination -

Java BufferedInputStream class is used to read information from stream. It internally uses buffer mechanism to make the performance fast.When a BufferedInputStream is created, an internal buffer array is created.

*/

import java.io.*;  
public class F6{    
public static void main(String args[]){    
try{    
FileInputStream fin=new FileInputStream("D:\\testout1.txt");    
BufferedInputStream bin=new BufferedInputStream(fin);    
int i;    
while((i=bin.read())!=-1){    
System.out.print((char)i);    
}    
bin.close();    
fin.close();    
}catch(Exception e){System.out.println(e);}    
}    
}  

/* 
Output -
Welcome to Dehradun!

*/
The content of a text file testout1.txt was
Welcome to Dehradun!
/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to write data into a file using FileWriter.

Objective -  

To understand the concept of FileWriter by writing data into a file.

Explaination -

Java FileWriter class is used to write character-oriented data to a file. It is character-oriented class which is used for file handling in java. It provides method to write string directly. 
*/

import java.io.FileWriter;  
public class F7 {  
public static void main(String args[]){    
try{    
FileWriter fw=new FileWriter("D:\\testout.txt");    
fw.write("Python");    
fw.close();    
}catch(Exception e){System.out.println(e);}    
System.out.println("Success...");    
}    
}  

/* 
Output -

Success...
*/

The content of a text file testout.txt is
Python




/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to read data from a file using FileReader.

Objective -  

To understand the concept of FileReader by reading data from a file.

Explaination -

Java FileReader class is used to read data from the file. It returns data in byte format like FileInputStream class. 
*/

import java.io.FileReader;  
public class F8 {  
public static void main(String args[])throws Exception{    
FileReader fr=new FileReader("D:\\testout.txt");    
int i;    
while((i=fr.read())!=-1)    
System.out.print((char)i);    
fr.close();    
}    
}    

/* 
Output -

Python
*/

The content of a text file testout.txt was
Python





/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to copy data from one file to another file

Objective -  

To understand the concept of FileReader and FileWriter.

Explaination -

The Java Scanner class is used to take input from user here. FileReader and FileWriter to read and write the content of file from one file to another.
*/

import java.io.*;  
import java.util.*;  
class Copyfile {  
public static void main(String arg[]) throws Exception {  
Scanner sc = new Scanner(System.in);  
System.out.print("Enter source file name :");  
String sfile = sc.next();  
System.out.print("Enter destination file name :");  
String dfile = sc.next();  
FileReader fin = new FileReader(sfile);  
FileWriter fout = new FileWriter(dfile, true);  
int c;  
while ((c = fin.read()) != -1) {  
fout.write(c);  
}  
System.out.println("Copy finish...");  
fin.close();  
fout.close();  
}  
}  






/* 
Output -

Enter source file name : file1.txt
Enter destination file name : file2.txt
Copy finish...
*/

file1 content is :
Content of file 1

file2 content after executing code is :
Content of file 1



























/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java socket program (create server and client). 

Objective -  

To understand the concept of socket programming.

Explaination -

Java Socket programming is used for communication between the applications running on different JRE.
Java Socket programming can be connection-oriented or connection-less.
*/



// Create Server 

import java.io.*;  
import java.net.*;  
public class MyServer {  
	public static void main(String[] args){  
		try{  
			ServerSocket ss=new ServerSocket(6666);  
			Socket s=ss.accept();//establishes connection   
			DataInputStream dis=new DataInputStream(s.getInputStream());  
			String  str=(String)dis.readUTF();  
			System.out.println("message= "+str);  
			ss.close();  
		      }
		catch(Exception e)
			{System.out.println(e);}  
		}  
}  







//Create Client

import java.io.*;  
import java.net.*;  
public class MyClient {  
	public static void main(String[] args) {  
	try{      
		Socket s=new Socket("localhost",6666);  
		DataOutputStream dout=new DataOutputStream(s.getOutputStream());  
		dout.writeUTF("Hello Server");  
		dout.flush();  
		dout.close();  
		s.close();  
	}
		catch(Exception e){System.out.println(e);}  
	}  
}  

/* 
Output -

message= Hello Server

*/
















/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 
Write a java program to create GUI using applet

Objective -  
To understand the concept of Appplet

Explaination -

Applet is a special type of program that is embedded in the webpage to generate the dynamic content. It runs inside the browser and works at client side.

*/

import java.applet.Applet;  
import java.awt.Graphics;  
	public class First extends Applet{  
		public void paint(Graphics g){  
		g.drawString("welcome",150,150);  
		}  
	}  
}    

<html>
<body>
<applet code="First.class" width="300" height="300">
</applet>
</body>
</html>












/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 
Write a java program to insert an image using applet

Objective -  
To understand the concept of Appplet.

Explaination -

Applet is a special type of program that is embedded in the webpage to generate the dynamic content. It runs inside the browser and works at client side.

*/
import java.awt.*;  
import java.applet.*;  

public class DisplayImage extends Applet {  

Image picture;  

public void init() {  
picture = getImage(getDocumentBase(),"sonoo.jpg");  
}  

public void paint(Graphics g) {  
g.drawImage(picture, 30,30, this);  
}  

}  

<html>
<body>
<applet code="DisplayImage.class" width="300" height="300">
</applet>
</body>
</html>





/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 
Write a java program to create GUI using Frame in AWT.

Objective -  
To understand the concept of AWT by creating basic GUI.

Explaination -

Java AWT (Abstract Window Toolkit) is an API to develop Graphical User Interface (GUI) or windows-based applications in Java. AWT components are platform-dependent and heavy weight
*/
import java.awt.*;    
public class Awtbasic extends Frame {    
	Awtbasic() { 	
		Button b = new Button("Click Me!!");  
		b.setBounds(30,100,80,30);  
		add(b);  
		setSize(300,300);  
		setTitle("This is our basic AWT example");   
		setLayout(null);   
		setVisible(true);  
	}    
	public static void main(String args[]) {   
		Awtbasic f = new Awtbasic();}  
}    
Output -













/*
NAME 	 -	ANISHA RAWAT
ROLLNO	 -	2023030
COURSE	 -	BSC IT B

Problem Statement - 

Write a java program to create basic calculator using AWT.

Objective -  

To understand the concept of  event handling, labels,buttons,etc in AWT.

Explaination -

Changing the state of an object is known as an event. For example, click on button, dragging mouse etc. The java.awt.event package provides many event classes and Listener interfaces for event handling. 
*/

import java.awt.*;
import java.awt.event.*;

public class ex1 extends Frame implements ActionListener
{
	
	TextField t1,t2,t3;
	Button b1,b2,b3,b4;
	ex1()
	{
		Label s=new Label("CALCULATOR");
		s.setBounds(150,50,150,20);
		Label n1=new Label("Enter first number");
		n1.setBounds(50,100,150,20);
		Label n2=new Label("Enter second number");
		n2.setBounds(50,150,150,20);
		Label ans=new Label("Result");
		ans.setBounds(50,200,150,20);
		t1=new TextField();
		t1.setBounds(200,100,150,20);
		t2=new TextField();
		t2.setBounds(200,150,150,20);
		t3=new TextField();
		t3.setBounds(200,200,150,20);
		t3.setEditable(false);
		b1=new Button("+");
		b1.setBounds(200,250,50,50);
		b2=new Button("-");
		b2.setBounds(300,250,50,50);
		b3=new Button("÷");
		b3.setBounds(200,310,50,50);
		b4=new Button("X");
		b4.setBounds(300,310,50,50);
		b1.addActionListener(this);
		b2.addActionListener(this);
		b3.addActionListener(this);
		b4.addActionListener(this);
		add(s);
		add(n1);
		add(n2);
		add(ans);
		add(t1);
		add(t2);
		add(t3);
		add(b1);
		add(b2);
		add(b3);
		add(b4);
		setSize(400,600);
		setLayout(null);
		setVisible(true);
	}

public void actionPerformed(ActionEvent e)
{
		String s1=t1.getText();
		String s2=t2.getText();
		int a=Integer.parseInt(s1);
		int b=Integer.parseInt(s2);
		int c=0;
		if(e.getSource()==b1)
		{
			c=a+b;
		}

		else if(e.getSource()==b2)
		{
			if(a>b)
			{
				c=a-b;
			}
			else
			{
				c=b-a;
			}
		}
		else if(e.getSource()==b3)
		{
			if(a>b)
			{
				c=a/b;
			}
			else
			{
				c=b/a;
			}
		}
		else if(e.getSource()==b4)
		{
			c=a*b;
		}
		String result=String.valueOf(c);
		t3.setText(result);
}

public static void main(String args[])
{
	
	new ex1();
}
}














/* 
Output -







































*/



/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B

Problem Statement - 

Write a java program to create GUI in Swing.

Objective -  

To understand the concept of AWT by creating basic GUI.

Explaination -

Java Swing tutorial is a part of Java Foundation Classes (JFC) that is used to create window-based applications. It is built on the top of AWT (Abstract Windowing Toolkit) API and entirely written in java.

Unlike AWT, Java Swing provides platform-independent and lightweight components.

*/

import javax.swing.*;  
public class FirstSwing {  
	public static void main(String[] args) {  
		JFrame f=new JFrame();//creating instance of JFrame  
		JButton b=new JButton("Click");
		b.setBounds(130,100,100, 40); 
		f.add(b);
		f.setSize(400,500); 
		f.setLayout(null);
		f.setVisible(true);
	}  


}  







/* 
Output -






























*/












/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to create table using JDBC.

Objective -  

To understand the concept of JDBC by creating table using MySql Database.

Explaination -

JDBC stands for Java Database Connectivity. JDBC is a Java API to connect and execute the query with the database. It is a part of JavaSE. JDBC API uses JDBC drivers to connect with the database. 

*/

import java.sql.*;

public class Mysql_create {
static final String DB_URL = "jdbc:mysql://localhost/bsc";
static final String USER = "root";
static final String PASS = "password";

public static void main(String[] args) {
try
	{
	  Connection conn = DriverManager.getConnection(DB_URL, USER, PASS);
Statement stmt = conn.createStatement();		
String sql = "CREATE TABLE REGISTRATION " +
"(id INTEGER not NULL, " +
" first VARCHAR(255), " + 
" last VARCHAR(255), " + 
" age INTEGER, " + 
" PRIMARY KEY ( id ))"; 

stmt.executeUpdate(sql);
System.out.println("Created table...");   	
} catch (SQLException e) {
e.printStackTrace();
} 
}
}

/*
Output-

Created table...
*/





































/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 
Write a java program to insert data into table using JDBC.

Objective -  
To understand the concept of JDBC by inserting data into table using MySql Database.

Explaination -

JDBC stands for Java Database Connectivity. JDBC is a Java API to connect and execute the query with the database. It is a part of JavaSE. JDBC API uses JDBC drivers to connect with the database. 
*/
import java.sql.*;
public class Mysql_create {
static final String DB_URL = "jdbc:mysql://localhost/bsc";
static final String USER = "root";
static final String PASS = "password";

public static void main(String[] args) {
try{
	 Connection conn = DriverManager.getConnection(DB_URL, USER, PASS);
Statement stmt = conn.createStatement();		
String sql = "INSERT INTO Registration VALUES (100, 'Ram', 'Kumar', 18)";
stmt.executeUpdate(sql);
sql = "INSERT INTO Registration VALUES (101, 'Ankit', 'Negi', 25)";
stmt.executeUpdate(sql);
sql = "INSERT INTO Registration VALUES (102, 'Akshay',’Saini’ 30)";
stmt.executeUpdate(sql);
System.out.println("Inserted records into the table...");  	
} catch (SQLException e) {
e.printStackTrace();
} 
}
}
/*
Output-
Inserted records into the table...
*/

/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to update data of a table using JDBC.

Objective -  

To understand the concept of JDBC by updating data of a  table using MySql Database.

Explaination -

JDBC stands for Java Database Connectivity. JDBC is a Java API to connect and execute the query with the database. It is a part of JavaSE. JDBC API uses JDBC drivers to connect with the database. 
*/
import java.sql.*;

public class Mysql_create {
static final String DB_URL = "jdbc:mysql://localhost/bsc";
static final String USER = "root";
static final String PASS = "password";

public static void main(String[] args) {
try
	{
	 Connection conn = DriverManager.getConnection(DB_URL, USER, PASS);
Statement stmt = conn.createStatement();		
String sql = “UPDATE REGISTRATION ” +
			“SET age= 19 WHERE id = 102”;
stmt.executeUpdate(sql);
System.out.println("Updated table...");
	} catch (SQLException e) {
e.printStackTrace();
} 
}
}
/* 
Output- 
Updated table...
*/
/*
NAME 	 -	SHUBHAM GOSAI
ROLLNO	 -	2023102
COURSE	 -	BSC IT B


Problem Statement - 

Write a java program to fetch data from a table using JDBC.

Objective -  

To understand the concept of JDBC by fetching data from a  table using MySql Database.

Explaination -

JDBC stands for Java Database Connectivity. JDBC is a Java API to connect and execute the query with the database. It is a part of JavaSE. JDBC API uses JDBC drivers to connect with the database. 
*/
import java.sql.*;

public class Mysql_create {
static final String DB_URL = "jdbc:mysql://localhost/bsc";
static final String USER = "root";
static final String PASS = "password";

public static void main(String[] args) {
try
	{
	 Connection conn = DriverManager.getConnection(DB_URL, USER, PASS);
Statement stmt = conn.createStatement();
	 ResultSet rs= stmt.executeQuery(“SELECT * FROM REGISRATION);		 while(rs.next())
	{
		System.out.print("ID: " + rs.getInt("id"));
	System.out.print(", Age: " + rs.getInt("age"));
	 System.out.print(", First: " + rs.getString("first"));
	 System.out.println(", Last: " + rs.getString("last"));
	} catch (SQLException e) {
e.printStackTrace();
} 
}
}

/* 
Output- 

ID: 100, Age: 18, First: Ram, Last: Kumar
ID: 101, Age: 25, First: Ankit, Last: Negi
ID: 102, Age: 30, First: Akshay Last: Saini

*/
