# SoapUIFramework
Excel Data Driven Framework for API Automation using SoapUi and groovy

PreRequisite:
1. Make sure to add jxl.jar to the soapuiinstallationfolder/lib and soapuiinstallationfolder/bin/ext
2. Soapui installation folder will be your C:\Program Files\SmartBear\SoapUI-5.5.0 unless you installed in other folders
3. Download the project xml and excel to your machine and make sure the soapui.xls also placed in the same folder where you placed the project xml file. 
4. Import the project in to your workspace.

Running the suite:

1. runme groovy script file under TestRunner testcase takes care of reading the values from excel and driving the tests based on the Yes/No keywords in the excel.
2. You can also run the TestRunner testcase from cmd. 

Adding more tests:

1. Create as many as tests you want in the same suite.
2. Make sure the tests created in soapui is same as in the excel sheet. 
3. If you add a new test case, make sure to add the below script in the tearDown script of the test case.
4. If you want to run same test case with multiple test data, use a different iteration in the excel sheet.

// Code to execute the GenerateCSVReport test step
testRunner.testCase.testSuite.project.testSuites["Library"].testCases["Reporting_Utility"].
testSteps["GenerateCSVReport"].run(testRunner, context);

Reports:
1. Reports will be generated to the folder where the project is placed in the local machine.
2. Reports are done based on the below article. 
https://dzone.com/articles/how-to-achieve-csv-reporting-in-soapui-open-source-1
3. Request and response bodies are also stored in a notepad file in the results folder along with the csv reports.

Please contact me if you need any details through mech.amuthansakthivel@gmail.com


