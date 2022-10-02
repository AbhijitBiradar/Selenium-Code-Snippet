# Selenium Code Snippet / Selenium Cheatsheet

# WebDriver Initialization


1. **Chrome Driver Initialization**

 ```java 
 
System.setProperty("webdriver.chrome.driver","path to chromedriver.exe");
Webdriver driver = new ChromeDriver();

```

2. **Firefox Driver Initialization**

 ```java
 
System.setProperty("webdriver.gecko.driver", "path to geckodriver.exe");
Webdriver driver=new FirefoxDriver();

```

3. **Internet Explorer Driver Initialization**

 ```java
 
System.setProperty("webdriver.ie.driver","path to iedriver.exe");
WebDriver driver=new InternetExplorerDriver();

```

4. **Edge Driver Initialization**

```java
System.setProperty("webdriver.edge.driver", "path to edgedriver.exe");
WebDriver driver = new EdgeDriver();

```

5. **Safari Driver Initialization**

```java
System.setProperty("webdriver.safari.driver","path to safaridriver.exe")
WebDriver driver = new SafariDriver();

```

# Element Locators


1. **Find element By ID**

```java
driver.findElement(By.id("Id Value"));

```

2. **Find element By Name**

```java
driver.findElement(By.name("Name Value"));

```

3. **Find element By Class Name**

```java
driver.findElement(By.className("Class Name Value"));

```

4. **Find element By Link text**

```java
driver.findElement(By.linkText("Link text Value"));

```

5. **Find element By Partial Link text**

```java
driver.findElement(By.partialLinkText("Partial Text Constant Value"));

```

6. **Find element By Tag name**

```java
driver.findElement(By.tagName("Tag Name Value"));

```

7. **Find element By CSS Selector**

```java
driver.findElement(By.cssSelector("CSS Value"));

```

8. **Find element By XPath**

```java
driver.findElement(By.xpath("Xpath Value"));

```

1. **getText()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
String label = element.getText();

```

# Operation on TextBox

1. **sendKeys()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.sendKeys("abhijit");

```

2. **clear()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.clear();

```

3. **getText()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
String actualText = element.getText();

```

4. **getAttribute()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
String attributeValue = element.getAttribute("value"); 

```


# Operation on Button

1. **click()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.click();

```

1. **submit()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.submit();

```

# Operation on Radio Button

1. **click()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.click();

```

1. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

```

# Operation on Checkbox

1. **click()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.click();

```

1. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

```

# Operation on Link

1. **click()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.click();

```

2. **getText()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
String linkText = element.getText();

```

# Operation on Table (Static and Dynamic Table)

1. **Static Table**

```java

for(int numberOfRows=1; numberOfRows<=5; numberOfRows++){
	for(int numberOfCol=1; numberOfCol <=3; numberOfCol++){
		System.out.println(driver.findElement(By.xpath(“//div[@id='main']/table[1]/tbody/tr[“+numberOfRows+”]/th[“+numberOfCol+”]”)));
	}
}

```

2. **Dynamic Table**

```java

WebElement htmltable=driver.findElement(By.xpath("//*[@id='main']/table[1]/tbody"));
List<WebElement> rows=htmltable.findElements(By.tagName("tr"));
 
for(int rnum=0;rnum<rows.size();rnum++){
	List<WebElement> columns=rows.get(rnum).findElements(By.tagName("th"));
	System.out.println("Number of columns:"+columns.size());
	 
	for(int cnum=0;cnum<columns.size();cnum++){
		System.out.println(columns.get(cnum).getText());
	}
}

```


# Operation on Extent Report


```java
 
public class DemoTest {
 
    ExtentHtmlReporter htmlReporter;
 
    ExtentReports extent;
    //helps to generate the logs in the test report.
    ExtentTest test;
 
    @BeforeTest
    public void startReport() {
        // initialize the HtmlReporter
        htmlReporter = new ExtentHtmlReporter(System.getProperty("user.dir") +"/test-output/testReport.html");
 
        //initialize ExtentReports and attach the HtmlReporter
        extent = new ExtentReports();
        extent.attachReporter(htmlReporter);
 
 
        //configuration items to change the look and feel
        //add content, manage tests etc
        htmlReporter.config().setChartVisibilityOnOpen(true);
        htmlReporter.config().setDocumentTitle("Simple Automation Report");
        htmlReporter.config().setReportName("Test Report");
        htmlReporter.config().setTestViewChartLocation(ChartLocation.TOP);
        htmlReporter.config().setTheme(Theme.STANDARD);
        htmlReporter.config().setTimeStampFormat("EEEE, MMMM dd, yyyy, hh:mm a '('zzz')'");
    }
 
    @Test
    public void test_1() {
        test = extent.createTest("Test Case 1", "The test case 1 has passed");
        Assert.assertTrue(true);
    }
 
 
    @Test
    public void test_2() {
        test = extent.createTest("Test Case 2", "The test case 2 has failed");
        Assert.assertTrue(false);
    }
 
    @Test
    public void test_3() {
        test = extent.createTest("Test Case 3", "The test case 3 has been skipped");
        throw new SkipException("The test has been skipped");
    }
 
    @AfterMethod
    public void getResult(ITestResult result) {
        if(result.getStatus() == ITestResult.FAILURE) {
            test.log(Status.FAIL,result.getThrowable());
        }
        else if(result.getStatus() == ITestResult.SUCCESS) {
            test.log(Status.PASS, result.getTestName());
        }
        else {
            test.log(Status.SKIP, result.getTestName());
        }
    }
 
    @AfterTest
    public void tearDown() {
        //to write or update test information to reporter
        extent.flush();
    }
}

```


# Operation on Jenkins configuration

```java

public class LoginPage {
	
	WebDriver driver;
	
	@BeforeTest
	public void setUp() {
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\Shalini\\Downloads\\chrom86_driver\\chromedriver.exe");
		driver = new ChromeDriver();
	}
	
	public void login() {
		String login_url = "https://opensource-demo.orangehrmlive.com/";
		driver.get(login_url);
		
		driver.manage().window().maximize();
		driver.manage().timeouts().pageLoadTimeout(10, TimeUnit.SECONDS);
		driver.findElement(By.id("txtUsername")).sendKeys("Admin");
		driver.findElement(By.id("txtPassword")).sendKeys("admin123");
		System.out.println(driver.getTitle());
	}
	
	@Test
	public void dashboard() {
		
		driver.findElement(By.id("menu_dashboard_index")).click();
		String textPresent = driver.findElement(By.xpath("//*[@id=\"content\"]/div/div[1]/h1")).getText();
		
		String textToBePresent = "DashBoard";
		assertEquals(textPresent, textToBePresent);
	}
	
	
	@AfterTest
	public void tearDown() {
			driver.quit();
	}

}


```


# Operation on Dropdown

1. **Select Dropdown option by Index**
	```java
	
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	dropdown.selectByIndex(Index);
	
	```
	
2. **Select Dropdown option by visible Text**	
	```java
	
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	dropdown.selectByVisibleText("text");
	
	```

3. **Select Dropdown option by value**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	dropdown.SelectByValue("value");
 
	```

4. **Deselect all selected options of dropdown**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	dropdown.deselectAll();
 
	```	
	
5. **Deselect Dropdown option by Index**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	dropdown.deselectByIndex(Index);
 
	```	

6. **Deselect Dropdown option by visible Text**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	dropdown.deselectByVisibleText("text");
 
	```	

7. **Deselect Dropdown option by value**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	dropdown.deselectByValue("value");
 
	```	

8. **List of all options in the dropdown**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	List<WebElement> options = dropdown.getOptions();
 
	```	
	
9. **Get selected option in the dropdown**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	String option = dropdown.getFirstSelectedOption();
 
	```	
	
	
10. **Vefify Dropdown allows selection of multiple items.**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	boolean isMultiple = dropdown.isMultiple();
 
	```	

# Operation on Browser

1. **Get Page Title**
	```java
	
	String pageTitle = driver.getTitle();
	
	```
	
2. **Get Current URL**	
	```java
	
	String currentURL = driver.getCurrentUrl();
	
	```
	
3. 	**Get Page Source**	
	```java
	
	String currentPageSource = driver.getPageSource();
	
	```

	
# Navigation Operation

1. **Navigate to page**
	```java
	
	driver.get("https://www.facebook.com/");
	
	```	
	
2. 	**Maxmize browser window**

	```java
	
	driver.manage().window().maximize();
	
	```	
	
3. 	**Fullscreen browser window**


	```java
	
	driver.navigate().to("https://www.google.com/");
	
	```	
	
4. 	**Navigate Back**

	```java
	
	driver.navigate().back();
	
	```

5. 	**Navigate Forward**

	```java
	
	driver.navigate().forward();
	
	```
	
6. 	**Refresh webpage**	

	```java
	
	driver.navigate().refresh();
	
	```
	
7. 	**Close Current browser**

	```java
	
	driver.close();
	
	```
	
8. 	**Close all browsers**

	```java
	
	driver.quit();
	
	```	

# Alert Operation

1. **Switch to Alert**
	```java
	
	Alert alert = driver.switchTo().alert();
	
	```	
	
2. **Accept Alert**

	```java
	
	Alert alert = driver.switchTo().alert();
	alert.accept();
	
	```	
	
3. **Dismiss Alert**

	```java
	
	Alert alert = driver.switchTo().alert();
	alert.dismiss();
	
	```	
	
4. **Get Alert text **

	```java
	
	Alert alert = driver.switchTo().alert();
	String text=alert.getText();
	
	```		
	
4. **Enter text into alert **

	```java
	
	Alert alert = driver.switchTo().alert();
	alert.sendKeys(“text");
	
	```		

# Cookie Operation

1. **Add Cookie**
	```java
	
	 driver.manage().addCookie(new Cookie("key", "value"));;
	
	```	
	
2. **Get Named Cookie**

	```java	
	
	Cookie cookie1 = driver.manage().getCookieNamed("foo");
	
	```	
	
3. **Get All Cookies**

	```java
	
	Set<Cookie> cookies = driver.manage().getCookies();
    System.out.println(cookies);
	
	```	
	
4. **Delete Cookie**

	```java
	
	// delete a cookie with name 'test1'
	driver.manage().deleteCookieNamed("test1");

	/*
	 Selenium Java bindings also provides a way to delete
	 cookie by passing cookie object of current browsing context
	 */
	driver.manage().deleteCookie(cookie1);
	
	```		
	
4. **Delete All Cookies**

	```java
	
	driver.manage().deleteAllCookies();
	
	```		


# Frame Operation

1. **Switch to frame using a WebElement**
	```java
	
	 //Store the web element
	WebElement iframe = driver.findElement(By.cssSelector("#modal>iframe"));

	//Switch to the frame
	driver.switchTo().frame(iframe);
	
	```	
	
2. **Switch to frame using a name or ID**

	```java	
	
	//Using the ID
	driver.switchTo().frame("buttonframe");

	//Or using the name instead
	driver.switchTo().frame("myframe");
	
	```	
	
3. **Switch to frame using an index**

	```java
	
	// Switches to the second frame
	driver.switchTo().frame(1);
	
	```	
	
4. **Leaving a frame**

	```java
	
	// Return to the top level
	driver.switchTo().defaultContent();
	
	```		
	

# Screenshot Operation

1. **Capture screenshot**
	```java
	
	//Take the screenshot
	File screenshot = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
	
	//Copy the file to a location and use try catch block to handle exception
	try {
		FileUtils.copyFile(screenshot, new File("C:\\projectScreenshots\\homePageScreenshot.png"));
	} catch (IOException e) {
		System.out.println(e.getMessage());
	}
	
	```	
	
# Action Class Keyboard & Mouse Operation	

1. **Sendkeys**
	```java
	
	//create an object for the Actions class and pass the driver argument 
	Actions action = new Actions(driver);
	
	//pass the product name that has to be searched in the website
	action.sendKeys(element, "iphone").build().perform();
	//pass the Enter value through sendKeys
	action.sendKeys(Keys.ENTER).build().perform();
	
	```	
	
2. **Mouse click**
	```java
	
	//create an object for the Actions class and pass the driver argument 
	Actions action = new Actions(driver);

	//specify the locator of the search box in which the product has to be typed
	WebElement elementToType = driver.findElement(By.id("twotabsearchtextbox"));
	
	//pass the value of the product
	action.sendKeys(elementToType, "iphone").build().perform();
	
	//specify the locator of the search button
	WebElement elementToClick = driver.findElement(By.className("nav-input"));

	//perform a mouse click on the search button
	action.click(elementToClick).build().perform();
	
	```	

3. **ContextClick**
	```java
	
	Actions action = new Actions(driver);	
	action.contextClick().build().perform();
	
	```		
	
4. **doubleClick**
	```java
	
	Actions action = new Actions(driver);	
	action.doubleClick(element).build().perform();
	
	```		

5. **moveToElement**
	```java
	
	Actions action = new Actions(driver);
	//mouse hover the Resources element
	action.moveToElement(element).build().perform();
	
	```		
	
6. **dragAndDrop**
	```java
	
	Actions action = new Actions(driver);		
	WebElement source = driver.findElement(By.xpath("//*[@id=\"drag1\"]"));
	WebElement destination = driver.findElement(By.xpath("//*[@id=\"div2\"]"));
	
	action.clickAndHold(source).moveToElement(destination).release().build().perform();	
	
	```		
	
7. **KeyUp & KeyDown**
	```java
	
	Actions action = new Actions(driver);		
	//holds the SHIFT key and converts the text to uppercase
	action.keyDown(element,Keys.SHIFT).sendKeys("lambdatest").build().perform();
	
	```			
	
8. **Scroll Up & Down the page**
	```java
	
	Actions act = new Actions(driver);
	// Scroll Down using Actions class
	act.keyDown(Keys.CONTROL).sendKeys(Keys.END).perform();

	try {
		Thread.sleep(1000);
	} catch (InterruptedException e) {
		e.printStackTrace();
	}
	  // Scroll Up using Actions class
	act.keyDown(Keys.CONTROL).sendKeys(Keys.HOME).perform();
	
	```		
9. **Copy & Paste**
	```java
	
	Actions action = new Actions(driver);

	action.keyDown( Keys.CONTROL ).sendKeys( "a" ).keyUp( Keys.CONTROL ).build().perform();
	action.keyDown( Keys.CONTROL ).sendKeys( "c" ).keyUp( Keys.CONTROL ).build().perform();
 
	WebElement firstName = driver.findElement(By.id("firstName"));
	userName.click();
	action.keyDown( Keys.CONTROL ).sendKeys( "v" ).keyUp( Keys.CONTROL ).build().perform();
	
	```			
	
10. **Refresh the page**
	```java
	
	Actions action = new Actions(driver);		
	action.keyDown(Keys.CONTROL).sendKeys(Keys.F5).build().perform();
	
	```		
	
11. **ClickAndHold**
	```java	
	
     Actions actions = new Actions(driver);  
	 WebElement titleC = driver.findElement(By.xpath("//li[text()= 'C']")); 
     actions.moveToElement(titleC); 
     actions.clickAndHold().perform(); 
	
	```	
	
	
# JavaScript Operation	

1. **To Click on a Button**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("document.getElementById('enter element id').click();");

//or

js.executeScript("arguments[0].click();", okButton);

```

2. **To Type Text in a Text Box without using sendKeys() method**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("document.getElementById(id').value='someValue';");
js.executeScript("document.getElementById('Email').value='SeleniumTesting.com';");

```

3. **To Handle Checkbox by passing the value as true or false**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("document.getElementById('enter element id').checked=false;");

```

4. **To generate Alert Pop window in Selenium Webdriver**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("alert('Welcome To Selenium Testing');");

```

5. **To refresh browser window using Javascript**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("history.go(0)");

```

6. **To get the innertext of the entire webpage in Selenium**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
String innerText = js.executeScript(" return document.documentElement.innerText;").toString();
System.out.println(innerText);

```

7. **To get the Title of our webpage**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
String titleText =  js.executeScript("return document.title;").toString();
System.out.println(titleText);

```

8. **To get the domain name**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
String domainName=  js.executeScript("return document.domain;").toString();
System.out.println(domainName);

```

9. **To get the URL of a webpage**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
String url=  js.executeScript("return document.URL;").toString();
System.out.println(url);

```

9. **To get the Height and Width of a web page**

 ```java 
 
JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript(“return window.innerHeight;”).toString();
js.executeScript(“return window.innerWidth;”).toString();

```

10. **To find a hidden element in selenium using JavaScriptExecutor**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("arguments[0].click();", element);

```

11. **To navigate to a different page using Javascript**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("window.location = 'https://www.lambdatest.com");

```

12. **To perform Scroll on an application using Selenium - To scroll the page vertically for 500px**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript(“window.scrollBy(0,500)”);

```

13. **To perform Scroll on an application using Selenium - To scroll the page vertically till the end**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript(“window.scrollBy(0,document.body.scrollHeight)”);

```

14. **Adding an element in DOM**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript("var btn=document.createElement('newButton');" + "document.body.appendChild(btn);");

```


15. **To get innertext of the entire webpage in Selenium**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;  
String sText =  js.executeScript("return document.documentElement.innerText;").toString();
System.out.println(sText);

```

16. **To click on a SubMenu which is only visible on mouse hover on Menu**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;   
js.executeScript("$('ul.menus.menu-secondary.sf-js-enabled.sub-menu li').hover()");

```


17. **To navigate to a different page using Javascript**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;   
js.executeScript("window.location = 'https://www.softwaretestingmaterial.com");

```

18. **To Type Text in a Text Box**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver; 
js.executeScript("document.getElementById('some id').value='someValue';");
js.executeScript("document.getElementById('Email').value='SoftwareTestingMaterial.com';");

```


# Window Handle Operation	

1. **getWindowHandle()**

 ```java 
 
String mainWindowHandle = driver.getWindowHandle();

```

2. **getWindowHandle()**

 ```java 
 
Set<String> allWindowHandles = driver.getWindowHandles();

```


3. **getWindowHandle()**

 ```java 
 
String mainWindowHandle = driver.getWindowHandle();
Set<String> allWindowHandles = driver.getWindowHandles();
Iterator<String> iterator = allWindowHandles.iterator();

```

4. **switch to child window**

 ```java 
 
String mainWindowHandle = driver.getWindowHandle();
Set<String> allWindowHandles = driver.getWindowHandles();
Iterator<String> iterator = allWindowHandles.iterator();

// Here we will check if child window has other child windows and will fetch the heading of the child window
while (iterator.hasNext()) {
	String ChildWindow = iterator.next();
		if (!mainWindowHandle.equalsIgnoreCase(ChildWindow)) {
		driver.switchTo().window(ChildWindow);
		WebElement text = driver.findElement(By.id("sampleHeading"));
		System.out.println("Heading of child window is " + text.getText());
	}
}

```

5. **Switch to main window**

 ```java 
 
String mainWindowHandle = driver.getWindowHandle();
driver.switchTo().window(mainwindow);

```



# Selenium Timeouts

1. **Implicitly Wait**

 ```java 
 
System.setProperty("webdriver.chrome.driver", "Path of Chrome Driver");
WebDriver driver = new ChromeDriver();
driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);

```


2. **setScriptTimeout()**

 ```java 
 
System.setProperty("webdriver.chrome.driver", "Path of Chrome Driver");
WebDriver driver = new ChromeDriver();
driver.manage().timeouts().setScriptTimeout(10, TimeUnit.SECONDS);

```

3. **pageLoadTimeout in Selenium**

 ```java 
 
System.setProperty("webdriver.chrome.driver", "Path of Chrome Driver");
WebDriver driver = new ChromeDriver();
driver.manage().timeouts().pageLoadTimeout(30, TimeUnit.SECONDS);

```

4. **Explicit Wait in Selenium**

 ```java 
 
System.setProperty("webdriver.chrome.driver", "Path of Chrome Driver");
WebDriver driver = new ChromeDriver();

WebDriverWait wait = new WebDriverWait(driver,30);
wait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//div[contains(text(),'COMPOSE')]")));

```


4. **Fluent Wait in Selenium**

 ```java 
 
System.setProperty("webdriver.chrome.driver", "Path of Chrome Driver");
WebDriver driver = new ChromeDriver();

Wait wait = new FluentWait(WebDriver reference)
.withTimeout(timeout, SECONDS)
.pollingEvery(timeout, SECONDS)
.ignoring(Exception.class);

WebElement foo=wait.until(new Function<WebDriver, WebElement>() {
	public WebElement applyy(WebDriver driver) {
	return driver.findElement(By.id("foo"));
	}
});

```


# AutoIt

Auto IT Script : AutoItTest.exe

; Wait 10 seconds for the Upload window to appear

  Local$hWnd=WinWait("[CLASS:#32770]","",10)

; Set input focus to the edit control of Upload window using the handle returned by WinWait

  ControlFocus($hWnd,"","Edit1")

; Wait for 2 seconds.

  Sleep(2000)

; Set the File name text on the Edit field

ControlSetText($hWnd, "", "Edit1", "SomeFile.txt")

  Sleep(2000)

; Click on the Open button 

  ControlClick($hWnd, "","Button1");
  
  
  
  Main Program
  
   ```java 
  	private static WebDriver driver = null;

  	public static void main(String[] args) throws IOException, InterruptedException {

  	driver = new FirefoxDriver();

	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

	driver.get("https://toolsqa.com/automation-practice-form");

	driver.findElement(By.id("photo")).click();

	Runtime.getRuntime().exec("D:\AutoIt\AutoItTest.exe");

	Thread.sleep(5000);

	driver.close();	
}

```

# Selenium GRID (Parallel Execution)

 ```java 

DesiredCapabilities dr=null;
if(browserType.equals("firefox")){
	dr=DesiredCapabilities.firefox();
	dr.setBrowserName("firefox");
	dr.setPlatform(Platform.WINDOWS);

}else{
	dr=DesiredCapabilities.internetExplorer();
	dr.setBrowserName("iexplore");
	dr.setPlatform(Platform.WINDOWS);
}
	 
RemoteWebDriver driver=new RemoteWebDriver(new    URL("http://localhost:4444/wd/hub"), dr);
driver.navigate().to("http://gmail.com");
driver.findElement(By.xpath("//input[@id='Email']")) .sendKeys("username");
driver.findElement(By.xpath("//input[@id='Passwd']")) .sendKeys("password");
driver.close();

```

# Advanced Browser Configuration


# Desired Capabilities

 ```java 

public String username = "Your_LambdaTest_Username";
public String accesskey = "Your_LambdaTest_Access_Key";
public static RemoteWebDriver driver = null;
public String gridURL = "@hub.lambdatest.com/wd/hub";
boolean status = false;

DesiredCapabilities capabilities = new DesiredCapabilities();
capabilities.setCapability("browserName", browser);
capabilities.setCapability("version", version);
capabilities.setCapability("platform", "win10"); // If this cap isn't specified, it will just get the any available one
capabilities.setCapability("build", "LambdaTestSampleApp");
capabilities.setCapability("name", "LambdaTestJavaSample");
capabilities.setCapability("network", true); // To enable network logs
capabilities.setCapability("visual", true); // To enable step by step screenshot
capabilities.setCapability("video", true); // To enable video recording
capabilities.setCapability("console", true); // To capture console logs

 capabilities.setCapability("selenium_version","4.0.0-alpha-2");
 capabilities.setCapability("timezone","UTC+05:30");
 capabilities.setCapability("geoLocation","IN");
 capabilities.setCapability("chrome.driver","78.0");


try {
	driver = new RemoteWebDriver(new URL("https://" + username + ":" + accesskey + gridURL), capabilities);
} catch (MalformedURLException e) {
	System.out.println("Invalid grid URL");
} catch (Exception e) {
	System.out.println(e.getMessage());
}
               
}

```

