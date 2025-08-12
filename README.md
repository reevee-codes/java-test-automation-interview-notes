# Test Automation Interview Notes (mid/senior level, Java)
- ---------------------------------
<h3>UI automation</h3>
- Difference between Selenium and Selenide

- **Difference between Find Elements and find element**<br>
  <p>FindElement() method: to access single element on the web page, returns the object of the first matching element of locator, throws NoSuchElementException</p> 
  <p>FindElements() method: identify the list of web elements, returns empty list if can't find</p>
- **Difference between implicity and explicity wait**<br>
  `implicit wait` waits for all of the elements<br>
  `explicit wait` waits for a specific condition for specific element
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
- The parallel attribute can be extended for multiple values, as below:<br>
Methods: Helps run methods in separate threads
Tests: Help to run all methods belonging to the same tag in the same thread<br>
Classes: Helps to run all methods belonging to a class in a single thread<br>
Instances: Helps run all methods in the same instance in the same thread<br>
Creating thread: a) create a subclass of Thread and override the run() method<br> 
- b) to pass an object that implements Runnable interface to the Thread constructor
- **Exceptions in selenium**<br>
- ElementNotSelectableException, ElementNotVisibleException, NoSuchFrameException, NoSuchWindowException
- **What is stale exceptions**<br>
when an element that was previously located on the page, is no longer available
- **How to do drag and drop in selenium**<br>To perform the drag and drop, the Actions class provides the method, action. dragAndDrop(Source, Destination);<br> This method takes two input parameters, the first parameter is for the source location, and the second is for the destination location.
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
- **difference between soft and hard assert**<br>
  Soft assert allows the test to continue even if an assertion fails, while hard assert stops the test immediately
- **TestNG vs Cucumber**<br>
  TestNG is a testing framework for Java while Cucumber is a BDD tool for behavior-driven development.

TestNG is used for unit, functional, and integration testing<br>
Cucumber is used for acceptance testing and supports BDD<br>
TestNG uses annotations to define test methods and groups<br>
Cucumber uses Gherkin syntax to define scenarios and steps<br>
TestNG generates HTML reports while Cucumber generates reports in various formats<br>
TestNG supports parallel testing while Cucumber does not<br>
TestNG is widely used in the Java community while Cucumber is popular in the Agile community<br>
- **OOP concepts**
- inheritance, encapsulation, polymorphism, and abstraction
- **interface vs abstract class**
Abstract class is a class with partial implementation while interface is a contract with no implementation.
Abstract class can have both abstract and non-abstract methods while interface can only have abstract methods.
  (java 9 - interfaces can have private methods, java 8 - static and default methods)
A class can implement multiple interfaces but can only inherit from one abstract class.
Abstract class can have constructors while interface cannot but Abstract class also cant be instantiated.
Abstract class can have access modifiers while interface methods are public by default.
- **page object model**<br>
- **page object factory**<br> - to support Page Object Design patterns
- **Facade Design Pattern**<br>
- fluent wait
- **Fluent Page Object Model:**<br>
- **Singleton Design Pattern**<br>
-----------------------
<h3>ISTQB related</h3>

- **What is STLC (Software Testing Life Cycle)**<br>
  Process that follows a series of steps or phases, and each phase has specific objectives and deliverables.
  Consists of:

1. **requirement analysis** - analyze the requirements from testing perspective
2. **test planning** - test manager/test lead determines the effort and cost estimates entire project, resourse planning, tool selection, training requirements
3. **test case development** - preparing test cases, scripts, test data, requirements traceability matrix
4. **test environment setup** - for example devops can prepare TEST/UAT environment
5. **test execution** - executing the tests
6. **test closure** - prepare test closure report/test metrics, evaluate cycle competion based on test coverage/quality/time

- **difference between Test plan, test case, test scenario**<br>
- test plan is document describing the scope, approach, resources and schedule of intended test activities
- test cases are specific instructions that can be used to test a particular function
- test scenarios are high-level descriptions of how a specific feature of an application should work

- **7 rules of testing**
1. Testing shows presence of defects, not abscence of defects<br>
   (Testing can show that defects are present, but cannot prove that there are no defects)<br>
2. Exhaustive testing is impossible <br>
   (Testing everything (all combinations) is not possible)
3. Early testing saves time and money<br>
   (Early testing is sometimes referred to as shift left. Testing early in the software development lifecycle helps reduce or eliminate costly changes)
4. Defects cluster together<br>
   (small number of modules usually contains most of the defects discovered)
5. Beware of the pesticide paradox<br>
   (If the same tests are repeated over and over again, eventually these tests no longer find any new defects)
6. Testing is context dependent<br>
   (Testing is done differently in different contexts)
7. Absence-of-errors is a fallacy<br>
   ( it is a fallacy (i.e., a mistaken belief) to expect that just finding and fixing a large number of defects will ensure the success of a system. For example, thoroughly testing all specified requirements and fixing all defects found could still produce a system that is difficult to use, that does not fulfill the users’ needs and expectations, or that is inferior compared to other competing systems.)
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
- **regression/smoke tests/sanity tests**<br>
- Smoke testing verifies the entire system e2e (acceptance testing) <br>
- Sanity Testing verifies only a particular component (regression testing) <br>
regression -  test the software/ application when a defect is fixed to ensure that the original defect is completely removed  <br>
- **: Error vs. Fault vs. Bug vs. Defect vs. Failure**<br>
1. error: The problem in code leads to errors<br>
2. fault: result of an error<br>
3. defect: fail to perform its required function<br>
4. failure: defect if encountered during execution =  failure<br>
- **Pairwise testing**<br>
- **Test techniques**<br>
- Equivalence testing -  used to reduce the number of test cases by identifying different sets of data
that are not the same and only executing one test from each set of data
- Boundary value analysis - behavior of the system at the boundaries of allowed data
- State transition testing - validate allowed and disallowed states and transitions
from one state to another by various input data
- Pairwise (all-pairs) testing - used for lowering number of test cases without getting too much danger, algorithm can be used in order to select test cases<br>
- **What is Adhoc Testing?**<br>
- A testing phase where the tester tries to ‘break’ the system by randomly trying the system’s functionality.<br>
Can include negative testing as well. See also Monkey Testing.
- **What is Bottom Up Testing?**<br>
- An approach to integration testing where the lowest level components are tested first then used to facilitate the testing of higher-level components.
  The process is repeated until the component at the top of the hierarchy is tested.
- **Pyramid of testing (from bottom to up)**<br>
- Unit
- Component
- Integration
- E2E
- **Static vs Dynamic testing**<br>
- Static Testing involves testing the software without running it<br>
- Dynamic Testing involves executing the program<br>
- ---------------------------------
<h3>SQL</h3>
- **Select all the different values from the Country column in the Customers table**<br>
-select distinct Country FROM Customers;
- **Select all records where the City column has the value "Berlin".**<br>
- SELECT * FROM Customers where city ='Berlin';<br>
  SELECT * FROM Customers WHERE NOT City = 'Berlin';
- **alphabetically by city**<br>
SELECT * FROM Customers ORDER BY City;
- **reverse order**<br>
- SELECT * FROM Customers ORDER BY City DESC;
- **first by the column Country, then, by the column City.**<br>
- SELECT * FROM Customers order by country, city;
- - **where the PostalCode column is empty or not**
- SELECT * FROM Customers WHERE POstalCode is NULL / IS NOT NULL
- -**Update the City column of all records in the Customers table**
- UPDATE Customers SET City = 'Oslo';
- -**Set the value of the City columns to 'Oslo', but only the ones where the Country column has the value "Norway".**
- UPDATE Customers SET City = 'Oslo' WHERE Country = 'Norway';
- left join - everything on the left + anything on right that matches
- right join - everything on the right + anything on the left that matches
- outer join - all on the right and left (Outer Join will also keep information that is not related to the other table in the resulting table)
- inner join - only things that match on the left and right (inner join will keep only the information from both tables that's related to each other (in the resulting table))
- ---------------------------------
<h3>Bash</h3>
- **cd** : go to a different location 
- **ls** : list the contents of the current directory
- **mkdir** : create new folder
- **touch** : create file without any content
- **rm** : Remove a file or directory <br>
- **cp** : Copy a file or directory
- **mv** : Move or rename a file or directory
- **pwd : show current path** <br>
- ps (“process status,” helps you see what's happening inside your Linux computer)
- lista procesow, ilosc pamieci, otworzxyv jakis notatnikiem, jak sie polaczuc z linuxem
- ---------------------------------
<h3>HTTP Methods (http verbs)</h3>
GET - retrieves data <br>
HEAD - response like get but without response body<br>
POST -  submits an entity to the specified resource<br>
PUT -  replaces all current representations<br>
DELETE -  deletes the specified resource<br>
CONNECT -  establishes a tunnel to the server identified by the target resource<br>
OPTIONS - describes the communication options for the target resource<br>
TRACE - performs a message loop-back test along the path to the target resource<br>
PATCH - applies partial modifications to a resource<br>
POST vs PUT vs PATCH -  PUT is used for creating or replacing resources, POST is used for creating or appending data to resources, and PATCH is used for partially updating existing resources
- ---------------------------------
<h3>HTTP 1 vs HTTP 2 vs HTTP 3</h3>
HTTP1 - web browser makes several parallel requests for page contents: HTML, images, style, JS<br>
HTTP2 - web browser makes one TCP connection with requests for all page contents in streams (binary)<br>
HTTP3 - web browser makes one QUIC connection with requests for all page contents in QUIC streams (binary)<br>
- ---------------------------------
<h3>HTTP 2.0</h3>
HTTP/2 is binary instead of textual.
HTTP/2 is fully multiplexed.<br>
This means that HTTP/2 can send multiple requests for data in parallel over a single TCP connection. This is the most advanced feature of the HTTP/2 protocol
because it allows you to download web files via ASync mode from one server.
Most modern browsers limit TCP connections to one server.
- ---------------------------------
<h3>HTTP 3.0</h3>
Unlike previous versions which relied on theTCP, HTTP/3 uses QUIC, a transport protocol built on UDP.<br>
The same request methods, status codes, and message fields, but encodes them and maintains session state differently<br>
due to the protocol's adoption of QUIC, HTTP/3 has lower latency and loads more quickly in real-world usage when compared with previous versions: in some cases over 3× faster than with HTTP/1.1<br>
- ---------------------------------
<h3>HTTP Codes</h3>
Informational responses (100 – 199)<br>
Successful responses (200 – 299)<br>
Redirection messages (300 – 399)<br>
Client error responses (400 – 499)<br>
Server error responses (500 – 599)<br>

<b>Informational responses</b><br>
100 Continue (the client should continue the request)<br>

<b>Successful responses</b><br>
200 OK<br>
201 CREATED<br>
202 Accepted<br>
204 No content<br>

<b>Redirection messages</b><br>
301 Moved permanently

<b>Client error responses</b><br>
400 Bad request (client error - malformed request syntax)<br>
401 Unauthorized<br>
403 Forbidden (client does not have access rights to the content)<br>
404 Not Found (server cannot find the requested resource)<br>
418 Im a teapot (server refuses the attempt to brew coffee with a teapot)<br>

<b>Server error responses</b><br>
500 Internal server error (server has encountered a situation it does not know how to handle)<br>
501 Not Implemented (The request method is not supported by the server and cannot be handled. The only methods that servers are required to support (and therefore that must not return this code) are GET and HEAD.)<br>
502 Bad Gateway (the server, while working as a gateway to get a response needed to handle the request, got an invalid response)<br>
503 Service Unavailable (the server is not ready to handle the request)<br>
- ---------------------------------
<h3>FTP</h3>
The ftp command opens the user interface to the Internet's File Transfer Protocol.<br>
This user interface, called the command interpreter, enables you to log in to a remote system and perform a variety of operations with its file system.<br>
- opens 2 connections, one is used to send commands, other is for sending data. commands are “send,” “get,” “change directory,” and “transfer.”
- uses three different modes: block, stream, and compressed. can perform perform large file size transfers.
- allows you to send multiple files at once.
- ---------------------------------
<h3>SSH</h3>
a network protocol that allows two devices to communicate and share data remotely over an unsecured network, like the Internet. The primary difference between Secure Shell Protocol and other login protocols is that SSH provides an encrypted connection.
- ---------------------------------
<h3>SFTP</h3>
Extension of SSH.<br>
FTP stands for File Transfer Protocol, while SFTP refers to Secure Shell (SSH) File Transfer Protocol. This gives you file transfers that are secured via SSH, which provides full access to shell accounts. A shell account is
one that sits on a remote server.SFTP uses a tunneling method to transfer data. With the benefit of additional security, FTP, which is less secure, uses direct transfer.

- --------------------------------
<h3>ACID</h3>

- --------------------------------
<h3>MOCK VS STUB</h3>

<br><b>STUB</b><br> is a fake class that comes with preprogrammed return values. It’s injected into the class under test to give you absolute control over what’s being tested as input. A typical stub is a database connection that allows you to mimic any scenario without having a real database.<br>
Purpose: To provide pre-determined behavior. A stub provides canned responses, irrespective of what input it gets.<br>
`List stubbedList = Mockito.mock(List.class);`<br>
`Mockito.when(stubbedList.get(0)).thenReturn("first");`<br>
-------------------------------------------------
<br><b>MOCK</b><br>
A <b>mock</b> is a fake class that can be examined after the test is finished for its interactions with the class under test. For example, you can ask it whether a method was called or how many times it was called.
Purpose: To verify behavior. A mock is used to check if a certain method has been called with the right parameters.<br>
You can use a mock object to verify that you have called it in the way expected.<br>
`List mockedList = Mockito.mock(List.class);`
-------------------------------------------------
<br><b>SPY</b>
<br>partial mock. Spies call the real methods unless they’re stubbed. Real spies should be used carefully and occasionally, for example when dealing with legacy code.<br>
<b>PROBLEMS WITH USING:</b>You might be tempted to use a spy to mock getBook(String id) method so that it doesn’t hit the database for example, is seems fine, but here’s the catch: if someone later modifies the getBook(String id) method in the BookService class, your test would still pass even though the actual behavior of getBookTitle(String id) might have changed.
<br>`List list = new LinkedList();`<br>
`List spy = Mockito.spy(list);`
-------------------------------------------------
