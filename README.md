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
    
 三、UserDetails接口
 
 实现身份认证
 
 四、认证和授权
 
 1、认证：authentication
 
 确认用户可以访问当前系统
 
 2、授权：authorization
 
 确定用户在当前系统中是否能够执行某个操作，即用户所拥有的功能权限
 
 五、sql语句的自动执行
 
 在目录src/main/resources目录下，import.sql文件会自动被执行
 
 六、安全配置类
 
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {
	
	/**
     * 自定义配置
     */
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http.authorizeRequests()
            .antMatchers("/css/**", "/js/**", "/fonts/**", "/index").permitAll(); // 都可以访问
    }
}
 
 
 
 
 
 
