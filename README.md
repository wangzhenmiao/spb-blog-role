# spb-blog-role

一、角色管理实现步骤

角色管理是安全设置的重要方面，角色定义了用户可以执行的操作集合

1、建立权限（角色）实体

2、建立用户与权限（角色）的关系

3、创建用户时，关联角色

4、修改用户的角色

5、初始化权限（角色）、用户的数据

二、pom依赖

1、security依赖

    <dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-security</artifactId>
		</dependency>
    
2、thymeleaf与spring security的整合

    <dependency>
			<groupId>org.thymeleaf.extras</groupId>
			<artifactId>thymeleaf-extras-springsecurity4</artifactId>
		</dependency>
    
 三、
