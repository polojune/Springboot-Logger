#AOP와 BindResult를 이용한 로그 파일 만드는 법

![blog](https://postfiles.pstatic.net/MjAyMDA4MTdfOTQg/MDAxNTk3NjQyNzU1MjY1.wegGpyy9N6Z2jnUqWWC8yz2nezoUqfhIUpC4NSQVDxcg.7Q2Pdnza4II3ggt5MeI0SIxM-eVKdgUq62QsHSnvO58g.PNG.getinthere/Screenshot_38.png?type=w773)

```xml 
[2020-08-17 14:37:59:644241][http-nio-8080-exec-2] INFO  c.c.l.config.aop.warn.BindingAdvice - 인포찍혀?
[2020-08-17 14:37:59:644241][http-nio-8080-exec-2] DEBUG c.c.l.config.aop.warn.BindingAdvice - 디버그 찍혀?
[2020-08-17 14:37:59:644241][http-nio-8080-exec-2] ERROR c.c.l.config.aop.warn.BindingAdvice - 에러찍혀?
[2020-08-17 14:37:59:644241][http-nio-8080-exec-2] WARN  c.c.l.config.aop.warn.BindingAdvice - 
com.cos.logtest.controller.IndexController:user() 이메일이 공백일 수없습니다.


```
## 로그 레벨

- 로그는 해당 level 위로는 다 기록된다. 예를 들어 info level이면 info, warn, error
- debug -> info -> warn -> error

## 참고 주소

- http://logback.qos.ch/manual/
- https://blog.naver.com/getinthere/221799123006


## 의존성

```xml
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-aop</artifactId>
</dependency>

<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-validation</artifactId>
</dependency>
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
</dependency>
```