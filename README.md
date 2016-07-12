# myTry
<html>
  <head>
    <title>My JSP '2.jsp' starting page</title>
  </head>
  
  <body>
	 <jsp:useBean id="person" class="com.guigu.chen.person" scope="page"></jsp:useBean>
	
	<!-- jsp:setProperty 标签在工作的时候 会自动把字符串转换成八种基本数据类型 -->
	<!-- 但是对于复杂的数据类型是无法自动转换的 -->
	<jsp:setProperty name="person" property="name" value="hzgg" />
	<jsp:setProperty name="person" property="age"  value="40"/>
	
	<!-- 方式二 通过param参数赋值   -->
	<!-- http://localhost:8080/JavaJsp/javabean/2.jsp?name=abcde -->
	<jsp:setProperty name="person"  property="name" param="name" />
	
	<!-- 方式三 对javabean所有的属性通过参数赋值 -->
	<!-- http://localhost:8080/JavaJsp/javabean/2.jsp?name=abcde&age=45&password=opip -->
	<jsp:setProperty name="person" property="*" />
	
	
	<%
		System.out.println(person.getName());
		System.out.println(person.getPassword());
		System.out.println(person.getAge());
		
	
	 %>
	 <jsp:getProperty property="age" name="person"/>
	 
	
  </body>
</html>
