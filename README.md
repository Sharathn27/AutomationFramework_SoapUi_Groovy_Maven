# Automation Framework for SoapUi Groovy Maven
This framework helps in automating SOAP and REST webservices using SoapUI. This framework is developed using SoapUI free version, Grrovy and Maven. This framework provides features (Test Data Management and Reporting) which are not available in SoapUI Free version.

## Steps to Install : -
•	Clone the project to your local machine.

•	Update properties file under config folder accordingly.

•	Update confiration in pom.xml as per your project needs.

•	Run 'mvn clean install' command to build code and run tests.


<img width="567" alt="screen shot 2018-05-03 at 9 55 34 pm" src="https://user-images.githubusercontent.com/14148321/39575127-caedfe3e-4f1c-11e8-9af3-c913df3ffc2f.png">

# Steps to perform in SoapUI project xml

## 1. Double click on SoapUI project and go to TestSuites tab and update setup and teardown scripts with below lines of code.

   Setup Script
   
       import com.ae.framework.*
       FrameworkUtils.projectSetUp(project)
       
   Teardown Script
   
       import com.ae.framework.*
       FrameworkUtils.projectTearDown(project)
       

## 2. Now Double click on TestSuite and update setup and teardown scripts with below lines of code.

Setup Script

       import com.ae.framework.*
       FrameworkUtils.testSuiteSetup(testSuite)
       
   Teardown Script
   
       import com.ae.framework.*
       FrameworkUtils.testSuiteTearDown(testSuite)
       
       
## 3. Now Double click on TestCase and update setup and teardown scripts with below lines of code.

Setup Script

       import com.ae.framework.*
       import groovy.json.JsonSlurper
       FrameworkUtils.testCaseSetup(testRunner)
       FrameworkUtils.updatePropertiesAndExecute(testRunner, testCase) 
       
   Teardown Script
   
       import com.ae.framework.*
       FrameworkUtils.testCaseTearDown(testRunner)
       
       
