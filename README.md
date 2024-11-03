# aws-lambda-example

Deploy Spring Boot Serverless CRUD API to AWS Lambda 🔥 | API Gateway | ‪@Javatechie‬

https://www.youtube.com/watch?v=J0aEfUUervE

create lamba function
function name: courier-service
runtime: java21
code: uplaod zip file
edit runtime settings
src/main/java/org/example/StreamLambdaHandler.java
see the code public class StreamLambdaHandler implements RequestStreamHandler {
org.example.StreamLambdaHandler::handleRequest

test
event name: course-api
template-optional
Api Gateway AWS Proxy - path - change path - /courses - httpmethod: GET
src/main/java/org/example/controller/CourseController.java - @RequestMapping("/courses")
click on test

API Gateway
rest api - new api - name: course-service
create resource - resource name: {proxy+)
create method - method type: ANY - integration type: lambda proxy
deploy api - stage dev

postman
new - http - post - apigatewaydeploydevurl/courses - raw -
{
    "id": 101,
    "name": "spring boot",
    "price": 200
}   
{
    "id": 102,
    "name": "DevOps",
    "price": 300
}   

GET - apigatewaydeploydevurl/courses/101
