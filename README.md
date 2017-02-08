
1.	What is Basic steps writing selenium scripts starting from scratch?
Ans:   a. Download JDK and JRE
           b. Update the Environmental variable 
           c. Download the Eclipse 
           d. create a Maven project
           e. create the package 
           f. Download the maven dependencies - Selenium
          g. Update the POM.XML file and run Maven install
          h. Create the class 
          i. Write the test case of selenium. 
Example :  package facebook_login;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

public class TestFB {
 public static void main(String[] args) throws InterruptedException {
	  WebDriver driver=new FirefoxDriver();
	   driver.get("https://www.facebook.com");
	  driver.manage().window().maximize();
         driver.findElement(By.xpath(".//*[@id='email']")).sendKeys("xyz@ymail.com");
	  driver.findElement(By.xpath(".//*[@id='pass']")).sendKeys("123");
	  driver.findElement(By.xpath(".//*[@id='u_0_o']")).click();
	   driver.close();}
}
2.	Explain how to do following in Selenium?
a.	How do u handle dynamic elements without using XPath?
Ans : By using id, cssname, name  locators 
b.	What are the different types of driver implementation?
Ans : ChromeDriver,FirefoxDriver,InternetExplorerDriver,SafariDriver
c.	Timeouts in selenium support?
Ans : Implicit wait and Explicit Wait 
d.	How do you printout snapshot using Selenium Web Driver?
           Ans :  WebDriver driver=new FirefoxDriver();
	   driver.get("https://www.facebook.com");

e.	Different exception in selenium?
ElementNotVisibleException,ErroeException,InvalidElementStateException.
3.	Different Locator in Selenium and explain briefly?
Ans : Id , css, xpath, name,classname 
a.	Write the code for selector
Ans : driver.findElement(By.xpath(“.//*[@id=’ap_name]”)).sendKeys(“Abrar”);
b.	radio button
Ans : driver.findElement(By.xpath(“.//*[@id=’ap_button]”)).click();
c.	select box
Ans: driver.findElement(By.xpath(“.//*[@id=’ap_checkbox]”)).click();
d.	Selecting rows and printing table data
Ans : driver.findElements(By.xpath("//*[@id='post-body 6522850981930750493']/div[1]/table/tbody/tr[1]/td")).size();
e.	difference between findElement() findElements()
Ans: findElement() -> returns single Web element
        FindElements() -> returns List of Web elements
4.	Give Purpose of following Items?
a.	ActionDriver -> the driver which performs some action..eg. FirefoxDriver 
b.	Listener -> It defines a listeners of a test class.
c.	Maven-> To fetch the jar files 
d.	Jenkin-> It’s a continous integration tool which uses maven to build the jar file 
e.	Log4j-> It’s a reporting tool 
5.	Give the difference between them?
a.	Methods of driver: Quit(), Close()
Quit() -> It quits the web driver ; close() -> It close the current page 
b.	Junit and Test NG?
In Junit each test is independent of other test where as in TestNG  each test method is dependent on another .
In TestNG we don’t need to extend the class where as in JUnit we need to extend the class
c.	JXL and Apache POI?
JXL doesnot support conditional formatting where as Apache POI supports
JXL supports page set up  where as Apache POI doesnot 
d.	IDE and RC
IDE does not support parallel execution where as RC supports parallel execution 
RC supports almost all browser where as IDE supports few browsers
e.	WebDriver and GRID
WebDriver is fast and automates the browsers faster than GRID.
6.	Different Annotation of TestNG?
@Test, @BeforMethod, @AfterMethod, @Listener,@Dataprovider
7.	What are different jars you include and give the use of them.
Selenium jar, TestNG jar, JXL Jar, Log4J jar,JAXB jar
8.	What do you do following this in TestNG?
a.	Passing parameter -> @Parameters
b.	Groups the test -> @BeforeGroup , @AfterGroup 
c.	skipping the tests -> @Test(Ignore)
d.	Introducing dependency on tests -> @Test
e.	Prioritizing these test? ->@Test(Priority=0)……….@Test(Priority=1)
9.	explain Page object model components?
POM components are : 
1.Browser Creation  2. Identify the Elements 3. Set the data 4. Perform Action 5. Validation   6. Truncate the test 
10.	Explain data driven framework and keyword driven framework?
Data Driven Framework is the process of reading the data from the spread sheet in which we have the data in the stored in the form a spread sheet and the data is read using the JXL dependency.
