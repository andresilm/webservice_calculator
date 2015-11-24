# Calculator web service README file

## What is this?
A simple calculator web service 

## Requirements
- Eclipse Mars.1 or newer with Maven 3 plugin
or
- Maven 3.x to build from command line

## How to build
### From shell:
Do 
`mvn package`
in the project folder, where the pom.xml file is located. A calculator.war file should be created in /target folder.

## How to run the calculator
You can deploy the .war to your tomcat server, or just run the embedded tomcat server by doing

`java -jar calculator.war`

