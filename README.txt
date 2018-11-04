# AutomationTest2
Write a suite of three automated browser tests for demo banking app at: http://demo.guru99.com/v4/

1. What I have done:
  a. Setup & Configure environment
    - Setup Java
    - Setup Eclipse
    - Setup WebDriverClient
    - Configure Eclipse with WebDriver
  b. Project scripting on Chrome/IE/Firefox browser:
    - Login successfully to http://demo.guru99.com/v4/
    - Create new customer successfully with valid info
    - Create new account based on created customer above successfully
    - Create new deposit based on created account above successfully
  
2. Test pre-requisites:
    - Download driver for each browser to set property
    - Set property before scripting for each browser:
      a. Chrome:
        System.setProperty("webdriver.chrome.driver", "Path to Chrome driver folder" + "\\chromedriver.exe");
        WebDriver driver = new ChromeDriver();
      b. IE:
        System.setProperty("webdriver.ie.driver", "Path to IE driver folder" + "\\IEDriverServer.exe");
		    InternetExplorerDriver driver = new InternetExplorerDriver();
      c. Firefox:
        System.setProperty("webdriver.gecko.driver", "Path to Gecko driver folder" + "\\geckodriver.exe");
        WebDriver driver = new FirefoxDriver();

3. Issues:
    - Configure to run on IE browser fail due to unmatched version between WebDriver & IEDriverServer. But after detected, I fix and configure successfully so that the script runs successfully.
    - Have no idea how to implement the page object pattern: http://www.seleniumhq.org/docs/06_test_design_considerations.jsp#page-object-designpattern 
