# 第一题
实现某师生健康码管理系统的用户注册和登录功能，具体要求如下：
- 用户注册register.jsp。如果是教师，则可输入姓名、身份证号、工号、密码、学院、角色（系统管理员、校级管理员、院级管理员、普通教师）等信息，注册的信息写入教师表dbt_teacher中；如果是学生，则可输入姓名、身份证号、学号、密码、学院、专业、班级等信息，注册的信息存入学生表dbt_student。要求密码采用SHA256加密（可用JDK自带的java.security.MessageDigest实现）后存入数据库。要求教师的身份证号、工号和学生的身份证号、学生不能重复注册，否则跳转至failed.jsp提示“您输入的身份证号、工号或学号已被注册！”。
- 用户登录login.jsp。选择用户类型(教师或学生)，输入登录名、密码，教师的登录名为工号，学生的登录名为学号。如果教师用户登录成功后，跳转至teacher.jsp显示该教师的姓名、身份证号、工号、密码、学院、角色等信息；如果是学生用户登录成功后，跳转至student.jsp显示该学生的姓名、身份证号、学号、密码、学院、专业、班级等信息；如果登录失败，则跳转至error.jsp，显示“您的用户名或密码错误”，3秒后自动跳转至登录页面login.jsp。

# 第二题
写基于DAO的MVC设计模式实现的添加客户信息功能，包括BaseDao.java、CustomerDao.java、addCustomer.jsp、AddCustomerServlet.java,使之能正常运行。要求dao类在com.dao包下，servlet类在com.controller包下，javabeans类在com.model包下，数据库访问采用数据源实现，然后增加查询、列出所有客户信息、修改和删除等功能。
- 查询：输入客户姓名查询，支持模糊查询。
- 列出所有可出信息：按客户号、姓名、~~Email~~（没有实现）、余额和操作，其中操作包括修改和删除链接； 
- 修改：根据客户号修改该客户的信息； 
- 删除：根据客户号删除该客户的信息；
