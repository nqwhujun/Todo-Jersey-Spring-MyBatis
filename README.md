#Todo-RESTful-spring-jersey-tomcat-mybatis
===================
This repository is a restful service for task management, which allows user to create, update and delete
account and events and automatically sends email to notify user if there are events that need to be done in one hour.

This service is based on Spring, Jersey and Mybatis framework and it uses Quartz Scheduler to check whether there are events need to be done in an hour.
Besides, I use token for authentication


##1. How to run
###1. in IDE
1. Checkout this project into your IDE
2. Run `Starter.java` in test folder

###2. in Tomcat 7
1. Install Tomcat 7(should install tomcat-admin) & Maven
2. Deploy the service into Tomcat7 with Maven(need to configure tomcat and maven account)
3. Run `mvn tomcat7:deploy` or `mvn tomcat7:redeploy`


##2. How to use API
**HTTP methods**: GET,POST,PUT and DELETE.<br/>
**Data**: Consumes and produces data in json format.<br/>
**url**: for user: `$BASE_URL/user`, for events: `$BASE_URL/event`<br/>

### For example:
##### Sign Up
**url**: `$BASE_URL/user/signup`
**method**: `POST`
Consumes:
```json
{"email" : "xxx@xx", "userName" : "xxx", "password" : "xxx"}
```
Sample Response : 
```json
{
        "token":"3615e0273f7094da2a8f9130671f0b32",
        "status":"200",
        "msg":"Create User Successfully"
}
```







