# LambdaTest--Certifications
LambdaTest Cloud Selenium Grid in parallel and mention the final Test ID while submitting.
hello


TEST SCENARIO 1:----


In this scenario, we first set the system property for the Chrome driver and create a new instance of the driver. We then navigate to the webpage and wait for all elements to be available using an explicit wait with a maximum timeout of 10 seconds.

Next, we use a SoftAssert to assert the page title against the expected value of "LambdaTest". Since we are expecting the assertion to fail, we do not use a regular Assert statement, but rather a soft assertion.

Finally, we call assertAll() on the SoftAssert instance to assert all the soft assertions and fail the test if any of them fail. We then close the browser.

Note that in this example, we use By.tagName("body") as the locator to wait for all elements to be available. Depending on your webpage, you may need to use a different locator or combination of locators.  




TEST SCENARIO 2:-----


Open the web page containing the checkbox demo.
Find and click on the "Checkbox Demo" link under the "Input Forms" section of the web page.
Locate the "Single Checkbox Demo" section and click on the checkbox to select it.
Verify that the checkbox is now in a "selected" state by checking that it has a checkmark inside it or by checking its "checked" attribute value in the HTML code.
Click on the checkbox again to deselect it.
Verify that the checkbox is now in an "unselected" state by checking that it does not have a checkmark inside it or by checking its "checked" attribute value in the HTML code.



TEST SCENARIO 3:-----


@BeforeMethod with @Parameters annotation is used to launch the browser and navigate to the URL specified in the Test Suite XML.
@AfterMethod annotation is used to close the browser after each test scenario.
@Test annotation is used to define the Test Scenario 3.
In the testJavaScriptAlert() method, we first locate the "Javascript Alerts" link and click on it to navigate to the appropriate section. We then locate the "Click Me" button and click on it to trigger the alert box. We use the Alert class to switch to the alert box and get its message using the getText() method. We then validate that the message is "I am an alert box!" and click the "OK" button using the accept() method. Finally, we use the assert() method to validate that the alert message is correct.



OVERALL EXPLANATION:----


1.The setUp() method is annotated with @BeforeTest and takes two parameters - browserName and url - which are passed from the Test Suite XML file.
2.The tearDown() method is annotated with @AfterTest.
3.The testScenario1(), testScenario2(), and testScenario3() methods are annotated with @Test and have different priorities.
4.In testScenario1(), an explicit wait is performed using ExpectedConditions.presenceOfAllElementsLocatedBy(), and then a SoftAssert is used to validate the page title against the expected title. Since the expected title is "LambdaTest" and the actual title is different, the assertion will fail and the test will proceed to the next statement.
5.In testScenario2(), the "Checkbox Demo" link is clicked, and the single checkbox is located using its XPath. Its initial selected state is checked using isSelected(), and an assertion is made to verify that it is not selected. Then the checkbox is clicked, and another assertion is made to verify that it is now selected.
6.In testScenario3(), the page is refreshed to go back to the initial URL, and then the "Javascript Alerts" link is clicked.





