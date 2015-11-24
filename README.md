# Calculator web service README file

## What is this?
A simple calculator web service, written in Java and using the Spring framework.

## Requirements
- Java SDK 1.8
- Maven 3.3.3
- Eclipse Mars.1 
- Maven plugin for Eclipse.
- JavaCC plugin for Eclipse.


The project is managed using Maven, so this dependencies will be automatically downladed (among others):

- Spring framework v1.3
- SQLite3 v3.8.11.2



## How to build
### From shell:
Do 

`mvn package`

in the project folder, where the pom.xml file is located. A calculator.war file should be created in /target folder.

## Launching the web application
You can deploy the .war to your tomcat server, or just run the embedded tomcat server by doing

`java -jar calculator.war`

Now the calculator should be running in 

`http:/localhost:8080/calculator`

## Usage example

To request to the calculator to solve some mathematical expression, let's say "2+2", this string has to be passed to the 'input`value like:

`http:/localhost:8080/calculator?input=2%2B2`

and then, the calculator answer in this case would be:

`{"data":[{"math_expression":"2+2","result":"4.0"}],"service_status":{"code":0,"message":"OK"}}`

Note that the every expression we want to solve using the calculator will need to be properly encoded to pass it in a URL.
