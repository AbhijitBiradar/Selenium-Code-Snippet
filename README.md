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

5. **isDisplayed()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean displayed = element.isDisplayed(); 

```


6. **isEnabled()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean enabled= element.isEnabled(); 

```

7. **getCssValue()**

```java
WebElement element=driver.findElement(By.xpath("Xpath Value"));
int fontSize = element.getCssValue("font-size")

```


# Operation on Button

1. **click()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.click();

```

2. **submit()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.submit();

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

5. **isDisplayed()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean displayed = element.isDisplayed(); 

```


6. **isEnabled()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean enabled= element.isEnabled(); 

```

2. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

```

7. **getCssValue()**

```java
WebElement element=driver.findElement(By.xpath("Xpath Value"));
int fontSize = element.getCssValue("font-size")

```

# Operation on Radio Button

1. **click()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.click();

```

2. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

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

5. **isDisplayed()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean displayed = element.isDisplayed(); 

```


6. **isEnabled()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean enabled= element.isEnabled(); 

```

2. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

```

7. **getCssValue()**

```java
WebElement element=driver.findElement(By.xpath("Xpath Value"));
int fontSize = element.getCssValue("font-size")

```

# Operation on Checkbox

1. **click()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
element.click();

```

2. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

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

5. **isDisplayed()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean displayed = element.isDisplayed(); 

```


6. **isEnabled()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean enabled= element.isEnabled(); 

```

2. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

```

7. **getCssValue()**

```java
WebElement element=driver.findElement(By.xpath("Xpath Value"));
int fontSize = element.getCssValue("font-size")

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

5. **isDisplayed()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean displayed = element.isDisplayed(); 

```


6. **isEnabled()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean enabled= element.isEnabled(); 

```

2. **isSelected()**

```java
WebElement element = driver.findElement(By.xpath("Xpath Value"));
boolean status = element.isSelected();

```

7. **getCssValue()**

```java
WebElement element=driver.findElement(By.xpath("Xpath Value"));
int fontSize = element.getCssValue("font-size")

```

# Operation on Table (Static and Dynamic Table)

1. **Static Table**

```java

for(int row=1; row<=5; row++){
	for(int column=1; column <=3; column++){
		WebElement element =driver.findElement(By.xpath("//div[@id='main']/table[1]/tbody/tr[" + row + "]/th[" + column + "]"));
		System.out.println(element.getText());
	}
}

```

2. **Dynamic Table**

```java


WebElement table=driver.findElement(By.xpath("//*[@id='main']/table[1]/tbody"));
List <WebElement> rows=table.findElement(By.tagName("tr"));

for(int row=0; row< rows.size(); row++){
	List <WebElement> columns = rows.get(row).findElements(By.tagName("th"));
	for(int column =0; column < columns.size(); column++){
		System.out.println(column.get(column).getText());
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

11. **Get all selected options**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	List<WebElement> selectedOptions = select.getAllSelectedOptions();
 
	```	
	

12. **Select all options from dropdown**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select dropdown = new Select(element);
	if (dropdown.isMultiple()) 
		List<WebElement> options = dropdown.getOptions(); 
		for (WebElement option : options) {   
			option.selectByVisibleText(option.getText());
		}
	} else {
			System.out.println("Dropdown don't support multiselect option");
	}
 
	```	

# Operation on ListBox

1. **Select ListBox option by Index**
	```java
	
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	listBox.selectByIndex(Index);
	
	```
	
2. **Select ListBox option by visible Text**	
	```java
	
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	listBox.selectByVisibleText("text");
	
	```

3. **Select ListBox option by value**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	listBox.SelectByValue("value");
 
	```

4. **Deselect all selected options of ListBox**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	listBox.deselectAll();
 
	```	
	
5. **Deselect ListBox option by Index**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	listBox.deselectByIndex(Index);
 
	```	

6. **Deselect ListBox option by visible Text**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	listBox.deselectByVisibleText("text");
 
	```	

7. **Deselect ListBox option by value**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	listBox.deselectByValue("value");
 
	```	

8. **List of all options in the ListBox**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	List<WebElement> options = listBox.getOptions();
 
	```	
	
9. **Get selected option in the ListBox**
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	String option = listBox.getFirstSelectedOption();
 
	```	
	
	
10. **Vefify ListBox allows selection of multiple items.**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	boolean isMultiple = listBox.isMultiple();
 
	```	
	
11. **Get all selected options**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	List<WebElement> selectedOptions = select.getAllSelectedOptions();
 
	```	
	

12. **Select all options from listBox**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	Select listBox = new Select(element);
	if (listBox.isMultiple()) 
		List<WebElement> options = listBox.getOptions(); 
		for (WebElement option : options) {   
			option.selectByVisibleText(option.getText());
		}
	} else {
			System.out.println("listBox don't support multiselect option");
	}
 
	```		

# Operation on Image

1. **click()**	
	```java
 
	WebElement element =driver.findElement(By.cssSelector("a[title=\"Go to Facebook home\"]"));
	element.click();	
 
	```
	
2. **getAttribute()**	
	```java
 
	WebElement element =driver.findElement(By.Id("Country"));
	String attriute=element.getAttribute("src");
 
	```	
	

# New Window

1. **Switch To New Window**	
	```java
 
	WebDriver newWindow = driver.switchTo().newWindow(WindowType.WINDOW);
	newWindow.get("https://blog.testproject.io/");
	System.out.println(driver.getTitle());
 
	```

# New Tab

1. **Switch To New Tab**	
	```java
 
	WebDriver newTab = driver.switchTo().newWindow(WindowType.TAB);
	newTab.get("https://testproject.io/platform/");
	System.out.println(driver.getTitle());
 
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
	
4. **Get Alert text**

	```java
	
	Alert alert = driver.switchTo().alert();
	String text=alert.getText();
	
	```		
	
4. **Enter text into alert**

	```java
	
	Alert alert = driver.switchTo().alert();
	alert.sendKeys(???text");
	
	```		

# Cookie Operation

1. **Add Cookie**
	```java
	
	 driver.manage().addCookie(new Cookie("key", "value"));;
	
	```	
	
2. **Get Named Cookie**

	```java	
	Cookie cookie1 = new Cookie("test", "selenium");
	Cookie cookie2 = new Cookie("subject", "Java");
	
	Cookie cookie1 = driver.manage().getCookieNamed("test");
	
	```	
	
3. **Get All Cookies**

	```java
	
	Set<Cookie> cookies = driver.manage().getCookies();
    	System.out.println(cookies);
	
	```	
	
4. **Delete Cookie**

	```java
	
	// Method 1
	Cookie cookie1 = new Cookie("test", "selenium");
	Cookie cookie2 = new Cookie("subject", "Java");
	
	driver.manage().deleteCookieNamed("test");

	// Method 2
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
	
	File sourceFile = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);	
	File destinationFile=new File("C:\\projectScreenshots\\homePageScreenshot.png");
	
	try {		
		FileUtils.copyFile(sourceFile, destinationFile);
	} catch (IOException e) {
		System.out.println(e.getMessage());
	}
	
	```	
	
# Action Class Keyboard & Mouse Operation	

1. **Sendkeys**
	```java	
	WebElement element = driver.findElement(By.className("nav-input"));
	
	Actions action = new Actions(driver);	
	action.sendKeys(element, "iphone")
		.build()
		.perform();	
	action.sendKeys(Keys.ENTER)
		.build()
		.perform();
	
	```	
	
2. **Mouse click**
	```java	 
	
	WebElement element = driver.findElement(By.className("nav-input"));
	
	Actions action = new Actions(driver);	
	action.click(element)
		.build()
		.perform();
	
	```	

3. **ContextClick or Right Click**
	```java
	WebElement element = driver.findElement(By.className("nav-input"));
	
	Actions action = new Actions(driver);	
	action.contextClick(element)
		.build()
		.perform();
	
	```		
	
4. **doubleClick**
	```java
	
	WebElement element = driver.findElement(By.className("nav-input"));
	
	Actions action = new Actions(driver);	
	action.doubleClick(element)
		.build()
		.perform();
	
	```		

5. **moveToElement**
	```java
	
	WebElement element = driver.findElement(By.className("nav-input"));
	Actions action = new Actions(driver);	
	action.moveToElement(element)
		.build()
		.perform();
	
	```		
	
6. **dragAndDrop**
	```java
			
	WebElement source = driver.findElement(By.xpath("//*[@id=\"drag1\"]"));
	WebElement destination = driver.findElement(By.xpath("//*[@id=\"div2\"]"));
	
	Actions action = new Actions(driver);	
	
	// Method 1
	action.clickAndHold(source)
		.moveToElement(destination)
		.release()
		.build()
		.perform();	
		
	// Method 2		
	action.dragAndDrop(element1, element2)
		.build()
		.perform();
	```		
	
7. **KeyUp & KeyDown**
	```java
	WebElement element1 = driver.findElement(By.xpath("//*[@id=\"drag1\"]"));
	WebElement element2 = driver.findElement(By.xpath("//*[@id=\"div2\"]"));
	
	Actions action = new Actions(driver);	
	action.keyDown(element1,Keys.SHIFT)
		.sendKeys("abhijit")
		.build()
		.perform();
		
	action.keyUp(element2,Keys.SHIFT)
		.sendKeys("biradar")
		.build()
		.perform();
	
	```			
	
8. **Scroll Up & Down the page**
	```java
	
	Actions action = new Actions(driver);	
	
	//scroll down a page
	action.sendKeys(Keys.PAGE_DOWN)
		.build()
		.perform();
		
	//scroll up a page
	action.sendKeys(Keys.PAGE_UP)
		.build()
		.perform();
	
	```		
9. **Copy & Paste**
	```java
	
	Actions action = new Actions(driver);

	action.keyDown(Keys.CONTROL)
		.sendKeys("a")
		.keyUp(Keys.CONTROL)
		.build()
		.perform();
		
	action.keyDown(Keys.CONTROL)
		.sendKeys("c")
		.keyUp(Keys.CONTROL)
		.build()
		.perform();
 
	WebElement firstName = driver.findElement(By.id("firstName"));
	userName.click();
	
	action.keyDown(Keys.CONTROL)
		.sendKeys("v")
		.keyUp(Keys.CONTROL)
		.build()
		.perform();
	
	```			
	
10. **Refresh the page**
	```java
	
	Actions action = new Actions(driver);		
	action.keyDown(Keys.CONTROL)
		.sendKeys(Keys.F5)
		.build()
		.perform();
	
	```		
	
11. **ClickAndHold**
	```java	
	
     WebElement titleC = driver.findElement(By.xpath("//li[text()= 'C']")); 
     
     Actions action = new Actions(driver);
     actions.moveToElement(titleC)
     	.clickAndHold()
	.perform(); 
	
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
js.executeScript(???return window.innerHeight;???).toString();
js.executeScript(???return window.innerWidth;???).toString();

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
js.executeScript(???window.scrollBy(0,500)???);

```

13. **To perform Scroll on an application using Selenium - To scroll the page vertically till the end**

 ```java 

JavascriptExecutor js = (JavascriptExecutor) driver;  
js.executeScript(???window.scrollBy(0,document.body.scrollHeight)???);

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

# Window Handle Operation	

1. **getWindowHandle()**

 ```java 
 
String mainWindowHandle = driver.getWindowHandle();

```

2. **getWindowHandles()**

 ```java 
 
Set<String> allWindowHandles = driver.getWindowHandles();

```


3. **switch to child window**

 ```java 
 
String mainWindowHandle = driver.getWindowHandle();
Set<String> allWindowHandles = driver.getWindowHandles();
Iterator <String> iterator = allWindowHandles.iterator();

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
Set<String> allWindowHandles = driver.getWindowHandles();
Iterator <String> iterator = allWindowHandles.iterator();

while (iterator.hasNext()) {
	String ChildWindow = iterator.next();
	if (!mainWindowHandle.equalsIgnoreCase(ChildWindow)) {
		driver.switchTo().window(ChildWindow);
		WebElement text = driver.findElement(By.id("sampleHeading"));
		System.out.println("Heading of child window is " + text.getText());
	}
}
driver.switchTo().window(mainWindowHandle);

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
 
// Waiting 30 seconds for an element to be present on the page, checking
// for its presence once every 5 seconds.
Wait<WebDriver> wait = new FluentWait<WebDriver>(driver)
	.withTimeout(Duration.ofSeconds(30))
  	.pollingEvery(Duration.ofSeconds(5))
  	.ignoring(NoSuchElementException.class);

WebElement foo = wait.until(new Function<WebDriver, WebElement>() {
	public WebElement apply(WebDriver driver) {
    		return driver.findElement(By.id("foo"));
  	}
});

```


# AutoIt

 ```java 
 
//Auto IT Script : AutoItTest.exe

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
  
  
  
  // Main Program  
 
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

# WebDriverEventListener Interface

1. **WebDriverEventListener methods**

```java 

@Override
    public void afterAlertAccept(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("After Alert Accept "+arg0.toString() );
    }
 
    @Override
    public void afterAlertDismiss(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("After Alert Dismiss "+ arg0);
         
    }
 
    @Override
    public void afterChangeValueOf(WebElement arg0, WebDriver arg1,
            CharSequence[] arg2) {
        // TODO Auto-generated method stub
        System.out.println("After value change of" +arg0);
         
    }
 
    @Override
    public void afterClickOn(WebElement arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("After clicked"+arg0);
    }
 
    @Override
    public void afterFindBy(By arg0, WebElement arg1, WebDriver arg2) {
        // TODO Auto-generated method stub
        System.out.println("After Find By"+arg1);
         
    }
    @Override
    public void afterNavigateBack(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("After Navigate Back");
    }
 
    @Override
    public void afterNavigateForward(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("After Navigate Forward");
    }
 
    @Override
    public void afterNavigateRefresh(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("On Navigating Refresh");
    }
 
    @Override
    public void afterNavigateTo(String arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("On Navigating To"+arg0);
         
    }
 
    @Override
    public void afterScript(String arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("After Script");
    }
 
    @Override
    public void beforeAlertAccept(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("Before Alert Accept");
    }
 
    @Override
    public void beforeAlertDismiss(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("Before Alert Dismiss");
    }
 
    
    @Override
    public void beforeChangeValueOf(WebElement arg0, WebDriver arg1,
            CharSequence[] arg2) {
        // TODO Auto-generated method stub
        System.out.println("Before Change Value of"+arg0);
    }
 
    @Override
    public void beforeClickOn(WebElement arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("Before Click on"+arg0);
    }
 
    @Override
    public void beforeFindBy(By arg0, WebElement arg1, WebDriver arg2) {
        // TODO Auto-generated method stub
        System.out.println("Before Find By"+arg0);
    }
 
    @Override
    public void beforeNavigateBack(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("Before Navigate Back");
    }
 
    @Override
    public void beforeNavigateForward(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("Before Navigate Forward");
    }
 
    @Override
    public void beforeNavigateRefresh(WebDriver arg0) {
        // TODO Auto-generated method stub
        System.out.println("Before Navigate Refresh");
    }
 
    @Override
    public void beforeNavigateTo(String arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("Before Navigate To"+arg0);
    }
 
    
    @Override
    public void beforeScript(String arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("Before Script");
    }
 
    @Override
    public void onException(Throwable arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("On Exception"+arg0);
    }


```


## AbstractWebDriverEventListener

1. **AbstractWebDriverEventListener Methods**

```java 
    public void afterChangeValueOf(WebElement arg0, WebDriver arg1,
            CharSequence[] arg2) {
        // TODO Auto-generated method stub
        System.out.println("After value change of" +arg0);
         
    }
 
    public void afterClickOn(WebElement arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("After clicked"+arg0);
    }
 
    public void afterFindBy(By arg0, WebElement arg1, WebDriver arg2) {
        // TODO Auto-generated method stub
        System.out.println("After Find By"+arg1);
         
    }
 

    public void beforeChangeValueOf(WebElement arg0, WebDriver arg1,
            CharSequence[] arg2) {
        // TODO Auto-generated method stub
        System.out.println("Before Change Value of"+arg0);
    }
 
    public void beforeClickOn(WebElement arg0, WebDriver arg1) {
        // TODO Auto-generated method stub
        System.out.println("Before Click on"+arg0);
    }
 
    public void beforeFindBy(By arg0, WebElement arg1, WebDriver arg2) {
        // TODO Auto-generated method stub
        System.out.println("Before Find By"+arg0);
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

# Solution of Stale Element Reference Exception

**Solution 1: Refreshing the web page**

```java 
driver.navigate().refersh();
driver.findElement(By.xpath("xpath here")).click();

```

**Solution 2: Using Try Catch Block**

```java 
// Using for loop, it tries for 3 times.
// If the element is located for the first time then it breaks from the for loop nad comeout of the loop
for(int i=0; i<=2;i++){
  try{
     driver.findElement(By.xpath("xpath here")).click();
     break;
  }
  catch(Exception e){
     Sysout(e.getMessage());
  }
}

```

**Solution 3: Using ExpectedConditions.refreshed**

```java 
wait.until(ExpectedConditions.presenceOfElementLocated(By.id("table")));
wait.until(ExpectedConditions.refreshed(ExpectedConditions.stalenessOf("table")));

```


# An Example for Ajax HANDLING

```java 
public class Ajaxdemo {
	
	private String URL = "http://demo.guru99.com/test/ajax.html";
	
	WebDriver driver;
	WebDriverWait wait;
	
	@BeforeClass
	public void setUp() {
		System.setProperty("webdriver.chrome.driver",".\\chromedriver.exe");
		//create chrome instance
		driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.navigate().to(URL);
	}
	
	@Test
	public void test_AjaxExample() {

		By container = By.cssSelector(".container");
		wait = new WebDriverWait(driver, 5);
		wait.until(ExpectedConditions.presenceOfElementLocated(container));
		
		//Get the text before performing an ajax call
		WebElement noTextElement = driver.findElement(By.className("radiobutton"));
		String textBefore = noTextElement.getText().trim();
		
		//Click on the radio button
		driver.findElement(By.id("yes")).click();
	
		//Click on Check Button
		driver.findElement(By.id("buttoncheck")).click();
		
		/*Get the text after ajax call*/
		WebElement TextElement = driver.findElement(By.className("radiobutton"));
		wait.until(ExpectedConditions.visibilityOf(TextElement));
		String textAfter = TextElement.getText().trim();
		
		/*Verify both texts before ajax call and after ajax call text.*/
		Assert.assertNotEquals(textBefore, textAfter);
		System.out.println("Ajax Call Performed");
		
		String expectedText = "Radio button is checked and it's value is Yes";
		
		/*Verify expected text with text updated after ajax call*/
		Assert.assertEquals(textAfter, expectedText);
		driver.close();
	}
	
}

```


# Flash Testing

```java 

public class Flash {				
    public static void main(String[] args) throws InterruptedException {								
  	// Open firefox browser		
	FirefoxDriver driver = new FirefoxDriver();			
  	// Maximize browser		
	driver.manage().window().maximize();		
  	// Under Flash jar file there is separate FlashObjectWebDriver class		
	FlashObjectWebDriver flashApp = new FlashObjectWebDriver(driver, "myFlashMovie");		
  	// Pass the URL of video		
	driver.get("http://demo.guru99.com/test/flash-testing.html");			
	Thread.sleep(5000);		
  	flashApp.callFlashObject("Play");			
  	Thread.sleep(5000);		
	flashApp.callFlashObject("StopPlay");			
	Thread.sleep(5000);		
	flashApp.callFlashObject("SetVariable","/:message","Flash testing using selenium Webdriver");
    System.out.println(flashApp.callFlashObject("GetVariable","/:message"));						
  }		
}

```

# Handle SSL Certificate in Browser

1. **Handle SSL Certificate in Firefox browser**

```java 
ProfilesIni prof = new ProfilesIni()				
FirefoxProfile ffProfile= prof.getProfile ("myProfile")
ffProfile.setAcceptUntrustedCertificates(true) 
ffProfile.setAssumeUntrustedCertificateIssuer(false)
WebDriver driver = new FirefoxDriver (ffProfile)	

```


2. **SSL Certificate Error Handling in Chrome**

```java 
DesiredCapabilities handlSSLErr = DesiredCapabilities.chrome ()       
handlSSLErr.setCapability (CapabilityType.ACCEPT_SSL_CERTS, true)
WebDriver driver = new ChromeDriver (handlSSLErr);

```

3. **SSL Certificate Error Handling in IE**

```java 
// first method
driver.navigate ().to ("javascript:document.getElementById('overridelink').click()");

// second method
DesiredCapabilities capabilities = new DesiredCapabilities();
capabilities.setCapability(CapabilityType.ACCEPT_SSL_CERTS, true);
System.setProperty("webdriver.ie.driver","IEDriverServer.exe");
WebDriver driver = new InternetExplorerDriver(capabilities);

```

# Create Custom Profile for Browser

1. **Create a Firefox Profiles**

```java
public class FirefoxProfile2{
	public static void main(String[] args) {
		// Create object for FirefoxProfile
		FirefoxProfilemyprofile=newFirefoxProfile (newFile("\c:users\AppData\MozillaFirefoxProfile_name.default "));  
		// Initialize Firefox driver    
		WebDriver driver = new FirefoxDriver(myprofile);
		//Maximize browser window       
		driver.manage().window().maximize();
		//Go to URL      
		driver.get("http://www.google.com");
		//Set  timeout      
		driver.manage().timeouts().implicitlyWait(5, TimeUnit.SECONDS);
		//close firefox browser  
		driver.close();
	}
}

```

2. **Create a Chrome Profiles**

```java
System.setProperty ("webdriver.chrome.driver","C:\\chromedriver.exe");
ChromeOptions options = new ChromeOptions();
options.addArguments("user-data-dir=C:/Users/user_name/AppData/Local/Google/Chrome/User Data");
options.addArguments("--start-maximized");
driver = new ChromeDriver(options);
driver.get("http://www.google.com");

```

3. **Create a Edge Profiles**

```java
System.setProperty("webdriver.edge.driver", "your\\path\\to\\edge\\webdriver\\msedgedriver.exe"); 
EdgeOptions edgeOptions = new EdgeOptions();

// Here you set the path of the profile ending with User Data not the profile folder
edgeOptions.addArguments("user-data-dir=C:\\Users\\username\\AppData\\Local\\Microsoft\\Edge\\User Data");

// Here you specify the actual profile folder
edgeOptions.addArguments("profile-directory=Profile 2");

edgeOptions.addArguments("--start-maximized");
WebDriver driver = new EdgeDriver(edgeOptions); 
driver.get("https://www.google.com");

```

# Handle Proxy
1. **Handle Proxy through AutoIT**

```java 
ProxyAuthentication.exe

Send("guru99{ENTER}")
Send("guru99{ENTER}")


public class AutoITDemo {
    public static void main(String[] args) throws IOException {
        System.setProperty("webdriver.chrome.driver", "D:\\ chromedriver.exe");;
        WebDriver driver = new ChromeDriver();
        driver.get("http://demo.guru99.com/test/basic_auth.php");
        //Passing the AutoIt Script to Selenium	
        Runtime.getRuntime().exec("D:\\Data_Personal\\ProxyAuthentication.exe");
    }
}

```

2. **Handle Proxy Using Alerts**

```java 
public class AlertsDemo {
    public static void main(String args[]) throws IOException {
        System.setProperty("webdriver.chrome.driver", "D:\\Data_Personal\\Software\\chromedriver_win32\\chromedriver.exe");;
        WebDriver driver = new ChromeDriver();
        driver.get("http://demo.guru99.com/test/basic_auth.php");
        // Handling Username alert
        driver.switchTo().alert().sendKeys("guru99");
        driver.switchTo().alert().accept();
        // Handling Password alert
        driver.switchTo().alert().sendKeys("guru99");
        driver.switchTo().alert().accept();
    }
}

```

# Broken Links

```java 
public class BrokenLinks {
    public static void main(String[] args) {
        System.setProperty("webdriver.chrome.driver","./src/resources/chromedriver");
        WebDriver driver = new ChromeDriver();
        driver.manage().window().maximize();
        driver.get("https://demoqa.com/broken");

        //Storing the links in a list and traversing through the links
        List<WebElement> links = driver.findElements(By.tagName("a"));

        // This line will print the number of links and the count of links.
        System.out.println("No of links are "+ links.size());  
      
        //checking the links fetched.
        for(int i=0;i<links.size();i++)
        {
            WebElement E1= links.get(i);
            String url= E1.getAttribute("href");
            verifyLinks(url);
        }
        
        driver.quit();
    }
    
    
    public static void verifyLinks(String linkUrl)
    {
        try
        {
            URL url = new URL(linkUrl);

            //Now we will be creating url connection and getting the response code
            HttpURLConnection httpURLConnect=(HttpURLConnection)url.openConnection();
            httpURLConnect.setConnectTimeout(5000);
            httpURLConnect.connect();
            if(httpURLConnect.getResponseCode()>=400)
            {
            	System.out.println(linkUrl+" - "+httpURLConnect.getResponseMessage()+"is a broken link");
            }    
       
            //Fetching and Printing the response code obtained
            else{
                System.out.println(linkUrl+" - "+httpURLConnect.getResponseMessage());
            }
        }catch (Exception e) {
      }
   }
}

```
