# Tendable
(https://www.tendable.com/)
## How to run the test
Firstly Import Project from Git into Eclipse.Below are the steps mentioned:
1. Launch eclipse IDE -> Click File> Import
2. In the Import Window, click Projects from Git (with smart import) and click Next.
3. In the Select Repository Source Window, click Existing local repository or Clone URI.
4. Step through the wizard and click Finish for the wizard to analyze the content for the project folder to find projects for import. 
5. Then import them into the IDE. The imported project will be listed in the Project Explorer view.

After importing project, test script is ready to execute in the following way:
1. Right-click on the TestRunner script.
2. Select “Run As” option and click on the “TestNG Test”.

TestNG result is displayed into two windows:
- Console Window
- TestNG Result Window

TestNG also generates HTML reports for the test executions. 
These reports can be viewed in any of the browsers and it can also be viewed using Eclipse’s build –in browser support.

## Strategy to employ Tendable challenge
1. Firstly, I created a Maven Project.
2. Then, I added few dependencies in pom.xml for cucumber, TestNG, selenium.
3. In src/test/resources folder, I created a package for feature files.
4. As it is integrated with Cucumber so Tendable.feature has been created for all the Test scenarios in given when then format.
5. Same, In src/test/java folder, I created another stepdefinitions package in which Tendable and TestRunner java classes has been created.
6. Tendable.java file is created for mapping all the test steps into test code and TestRunner.java file is used to execute the script. 
7. In Tendable.java file, added @BeforeTest and @AfterTest methods
- In @BeforeTest method, creates a new instance of the Chrome driver to open the browser and it will be executed before the first test case. 
- In @AfterTest method, added close method to close the driver which will be executed after the last test case.
