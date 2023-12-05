# java-test-automation-notes

<h3>Selenium/TestNG</h3>

- **Difference between Find Elements and find element**<br>
  <p>FindElement() method: to access single element on the web page, returns the object of the first matching element of locator, throws NoSuchElementException</p> 
  <p>FindElements() method: identify the list of web elements, returns empty list if can't find</p>
- **Difference between implicity and explicity wait**<br>
  `implicit wait` waits for an element to appear on the page<br>
  `explicit wait` waits for a specific condition
- **syntax for explicit wait**<br>
- `WebDriverWait wait = new WebDriverWait(driver, 5);
  wait.until(somethingThatShouldHappen);`
- **How to invoke browser**<br>
- Set a system property `webdriver.chrome.driver` to the path of your ChromeDriver.exe file and instantiate a ChromeDriver class: `System.setProperty(“webdriver.chrome.driver”,”chromedriver location”);`
  Maximize the window: `driver.manage().window().maximize();`  
  To open the URL: `driver.get(“URL link”)`
- **What is testNg Annotations**<br>
  TestNG is a Java-based framework, while JUnit is an open-source Unit Testing Framework for JAVA. Comparing TestNG Vs JUnit, TestNG annotations are easier to use and understand than JUnit. TestNG allows us to create parallel tests, whereas JUnit does not support running parallel tests (in 4, in 5 it supports).
- **How to read excel file in selenium**
  Apache POI is an open-source Java library often utilized to create and handle Microsoft Office-based files
- **How to do parallel Testing**
- The parallel attribute can be extended for multiple values, as below:

Methods: Helps run methods in separate threads
Tests: Help to run all methods belonging to the same tag in the same thread
Classes: Helps to run all methods belonging to a class in a single thread
Instances: Helps run all methods in the same instance in the same thread
Creating thread: a) create a subclass of Thread and override the run() method.b) to pass an object that implements Runnable (java.lang.Runnable to the Thread constructor.
- **Exceptions in selenium**<br>
- ElementNotSelectableException, ElementNotVisibleException, NoSuchFrameException, NoSuchWindowException
- **What is stale exceptions**<br>
when an element that was previously located on the page, is no longer available
- **How to do drag and drop in selenium**<br>To perform the drag and drop, the Actions class provides the method, action. dragAndDrop(Source, Destination);<br> This method takes two input parameters, the first parameter is for the source location, and the second is for the destination location.
- **Java program to find the largest two numbers in a given array**<br>
  `int max1 = Integer.MIN_VALUE;`<br>
  `int max2 = Integer.MIN_VALUE;`<br>
  for (int number : numbers) {
  if (number > max1) {
  max2 = max1;
  max1 = number;
  } else if (number > max2) {
  max2 = number;
  }
  }`
- **wiremock**<br>
WireMock is a tool for building mock APIs. Create stable development environments, isolate yourself from flakey 3rd parties and simulate APIs that don't exist yet.

- **Access modifiers in java**<br>
public: visible in class, subclass, package, global <br>
protected: visible in class, subclass, package (protected from global) <br>
default: visible in class, package <br>
private: visible in class <br>
- **checked and unchecked exception**
A checked exception is caught at compile time whereas a runtime or unchecked exception is, as it states, at runtime.<br>
Checked: IOException, SQLException, FileNotFoundException, ClassNotFoundException <br>
Unchecked: NPE, ArrayIndexOutOfBonds, ArithmeticException
- **how to handle alerts in selenium**<br>
  driver.switchTo().alert().accept();
- **how to handle frames:**<br>
driver.switchTo().frame(“ID of the frame“);

<h3>ISTQB related</h3>

- **What is STLC**<br>
  Process that follows a series of steps or phases, and each phase has specific objectives and deliverables.
  Consists of:

1. **requirement analysis** - analyze the requirements from testing perspectinve
2. **test planning** - test manager/test lead determines the effort and cost estimates entire project, resourse planning, tool selection, training requirements
3. **test case development** - preparing test cases, scripts, test data, requirements traceability matrix
4. **test environment setup** - for example devops can prepare TEST/UAT environment
5. **test execution** - executing the tests
6. **test closure** - prepare test closure report/test petrics, evaluate cycle competion based on test coverage/quality/time

- **difference between Test plan,test case,test scenario**<br>
- The main difference between test cases and test scenarios is that test cases are specific instructions that can be used to test a particular function or feature of an application,
- while test scenarios are high-level descriptions of how a specific function or feature of an application should work.
- **7 rules of testing**
1. Testing shows presence of defects, not abscence of defects
2. Exhaustive testing is impossible
3. Early testing saves time and money
4. Defects cluster together
5. Beware of the pesticide paradox
6. Testing is context dependent
7. Absence-of-errors is a fallacy
- **Boundary value testing**
  It checks for the input values near the boundary that have a higher chance of error.<br>
  Example: Consider a system that accepts ages from 18 to 56.

  Boundary Value Analysis(Age accepts 18 to 56)

  Valid Test cases: Valid test cases for the above can be any value entered greater than 17 and less than 57.<br>

  Enter the value- 18.<br>
  Enter the value- 19.<br>
  Enter the value- 37.<br>
  Enter the value- 55.<br>
  Enter the value- 56.<br>

Invalid Testcases: When any value less than 18 and greater than 56 is entered.
Enter the value- 17.<br>
Enter the value- 57.<br>
- **what is defect bug cycle**<br>
like jira statuses
- **regression/smoke tests/sanity tests**
regression -  test the software/ application when a defect is fixed to ensure that the original defect is completely removed  <br>
smoke tests - minimal set of tests run on each build <br> 
sanity tests -  very brief run-through of the functionality <br>
- **: Error vs. Fault vs. Bug vs. Defect vs. Failure**<br>
error: The problem in code leads to errors<br>
fault: A fault is introduced into the software as the result of an error<br>
defect: flaw in a component or system that can cause the component or system to fail to perform its required function, e.g., an incorrect statement or data definition<br>
failure: a defect, if encountered during execution, may cause a failure<br>


