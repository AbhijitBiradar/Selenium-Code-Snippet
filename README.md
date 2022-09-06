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
