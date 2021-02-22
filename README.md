# selenium-java SevenSender Task1
Automation of KOMOOT.COM using Page Object/Page Factory 

## Prerequisites 
   Check JAVA and MAVEN system **cmd command**
   ```
   java -version  
   mvn -version
   ```
### Follow steps if JAVA and MAVEN is not installed   
  - JAVA https://www.oracle.com/java/technologies/javase-downloads.html
  - Apache Maven https://maven.apache.org/download.cgi
   
  - How to download and install JAVA https://www.guru99.com/install-java.html
    also need to set Environment Variables 
  - For JAVA https://mkyong.com/java/how-to-set-java_home-on-windows-10/
  - For MAVEN https://mkyong.com/maven/how-to-install-maven-in-windows/
  - Configuration should be look like this (https://i.ibb.co/z8PB6ZW/selenium.jpg)
    
### Browser Version 
- Chrome Version 88.0.4324.150 (Official Build) (64-bit)
- Firefox 85.0.2 (64-bit)

### IF Browser Version Error 
- Check https://www.selenium.dev/downloads/ and download supported webdriver for respective browser 
  and replace into *SRC/MAIN/RESOURCES*

-------------------------------------------------------------------------------------------------------------------------------------------------

### Test Case Decription
#### TC001_simpleLoginTest
- Launching Browser (opening browser, maximizing window, navigate to URL)
- Click on **ACCEPT ALL**
- Enter **EMAIL**
- Click on **continueWithEmail**
- ENter **Encrypted Paswword** 
- Click on **LOGIN**
- Compare *Expected and Actual User* then print **ACTUAL USER** *(get text from page)*
- Close Browser

#### TC002_pageTitleTest
- Launching Browser (opening browser, maximizing window, navigate to URL)
- Click on **ACCEPT ALL**
- **CTR** and click **Discover, Route planner, Features** *opening window in new tab*
- Get title of page and print on CONSOLE
- Close Browser

-----------------------------------------------------------------------------------------------------------------------------------------------------

## How to run Test Cases using JENKIN
- Download JENKIN war file from https://www.jenkins.io/download/
- Go to jenkins.war file location and run through *CMD* **java -jar jenkins.war -httpPort=8080
- Verify JENKINS IS FULLY UP AND RUNNING MESSAGE https://i.ibb.co/bWHMgwW/jenkins-running.jpg
- Open browser and navigate to **http://localhost:8080/** for first use create account and login
- Configure local JDK and MAVEN path. Go to *manage jenkins* -> *global tool configuration* -> click on *JDK installations...* and insert local JDK path https://i.ibb.co/PwSHGy0/java.jpg then navigate to *Maven installations* and insert maven path https://i.ibb.co/JCRwN5m/maven.jpg then *save* changes
- Click on *New Item* Enter item name and select *Freestyle project*
- Click on *configure* https://i.ibb.co/nm7dvnd/configure.jpg under general click on *Advanced...* use custom workspace (as we are trigging mvn on local as menctioned in task3) write command **${JENKINS_HOME}/nameOfProject** and under Build select maven version, **test** command Goals filed. https://i.ibb.co/2Sf18mx/jenkins1.png
- Past your project into local jenkins repository **C:\Users\XYZ\.jenkins**
- Return to Dashboard slect project and click on **Build Now**
- **TASK3 SCHEDULE TEST RUN for NOON everyday** Under build trigger section *Build Triggers* -> *Build periodically* Documentation = https://tinyurl.com/rrf4mbbb Proof = https://i.ibb.co/vjzKtmK/success.jpg https://i.ibb.co/kHYG984/success2.jpg Build is automatically triggred at 5.35 PM (JENKINS SHOULD BE UP AND RUNNING)
	```
	35 17 * * * 
	```


💪 Mastering automation testing to improve software quality

🚀 Unleashing the potential of using Selenium WebDriver for automation

