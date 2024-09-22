---
layout: default
title: Cvetelin Stoimenov QA Blog
---

## Welcome to My QA Projects

### What You'll Find Here

- **Diverse Projects:** Each project highlights different aspects of QA, including manual testing, automated testing, and CI/CD integration.
- **Hands-On Experience:** I’ve implemented various testing strategies using tools like Selenium, Postman, and JMeter, focusing on real-world applications and scenarios.
- **Documentation:** Each project is accompanied by detailed documentation, including setup instructions, testing methodologies, and challenges faced during development.

### My Commitment

I am passionate about ensuring software quality and user satisfaction. Through continuous learning and experimentation, I aim to contribute effectively to the tech industry. I welcome feedback and collaboration, so feel free to explore my projects and connect with me!


<h2 style="color: #2E86C1;">Building Scalable Automated UI Tests for Foody’s Core Functionalities</h2>
<p>Automating UI tests is crucial for ensuring the functionality and reliability of web applications. In this project, I focused on creating automated tests for <strong>Foody's core features</strong>, including creating, editing, and deleting food items, as well as searching through the menu. Using <strong>Selenium WebDriver</strong> for automation, I ensured these tests run across different browsers.</p>

<h3 style="color: #1ABC9C;">Step-by-Step Breakdown</h3>
<ol>
  <li><strong>Set up the testing environment:</strong> I started by configuring Selenium WebDriver with <strong>Google Chrome</strong> as the browser of choice. Installing the latest WebDriver, along with setting up <strong>Visual Studio</strong> for C#, allowed me to integrate the tests smoothly.</li>
  <li><strong>Create Test Scenarios:</strong> Based on the functional requirements, I outlined the following test scenarios:
    <ul>
      <li>Log in to the Foody app.</li>
      <li>Add a new food item.</li>
      <li>Edit the food item.</li>
      <li>Delete the food item.</li>
      <li>Search for a specific food item.</li>
    </ul>
  </li>
  <li><strong>Writing Selenium Tests:</strong> Each scenario was translated into a series of test cases. Below is an example of the test for adding a new food item.
  </li>
</ol>

<h3 style="color: #1ABC9C;">Example Selenium Test Script</h3>
<p>The test below demonstrates how Selenium interacts with the browser to automate the process of adding a new food item.</p>
<pre style="background-color: #F0F3F4; padding: 10px;"><code>public void AddFoodItemTest()
{
    IWebDriver driver = new ChromeDriver();
    driver.Navigate().GoToUrl("https://foody-app.com");

    // Log in
    var login = driver.FindElement(By.Id("login"));
    login.SendKeys("testuser");
    login.Submit();

    // Add a new food item
    var addButton = driver.FindElement(By.Id("addItem"));
    addButton.Click();
    
    var itemName = driver.FindElement(By.Id("itemName"));
    itemName.SendKeys("Pasta Carbonara");
    itemName.Submit();
    
    driver.Quit();
}
</code></pre>

<h3 style="color: #1ABC9C;">Challenges Faced and Solutions</h3>
<ul>
  <li><strong>Dynamic Element Loading:</strong> The add button took a while to load, so I incorporated <code>WebDriverWait</code> to ensure that the element is clickable before the test proceeds.</li>
  <li><strong>Cross-Browser Testing:</strong> Selenium made it easy to run tests on both Chrome and Firefox browsers. I configured my tests using the WebDriver factory to switch between browsers effortlessly.</li>
</ul>

<h3 style="color: #1ABC9C;">Test Process Overview</h3>
<table border="1" style="width: 100%; border-collapse: collapse; text-align: center;">
    <tr style="background-color: #D5F5E3;">
        <th>Test</th>
        <th>Description</th>
        <th>Status</th>
    </tr>
    <tr>
        <td>Login Test</td>
        <td>Ensure login functionality works correctly</td>
        <td style="color: green;">Passed</td>
    </tr>
    <tr>
        <td>CRUD Operations</td>
        <td>Create, edit, delete, and search food items</td>
        <td style="color: green;">Passed</td>
    </tr>
</table>

<h3 style="color: #1ABC9C;">Postman API Testing for Backend</h3>
<p>To complement the UI tests, I used <strong>Postman</strong> for testing the API endpoints responsible for CRUD operations. Below is the Postman JSON collection used to test the API:</p>
<pre style="background-color: #FCF3CF; padding: 10px;"><code>{
    "info": {
        "name": "Food Item API",
        "description": "Testing CRUD operations for food items"
    },
    "item": [
        {
            "name": "Create Item",
            "request": {
                "method": "POST",
                "url": "https://api.foody-app.com/items",
                "body": {
                    "mode": "raw",
                    "raw": "{\"name\":\"Pasta Carbonara\", \"category\":\"Italian\"}"
                }
            }
        }
    ]
}</code></pre>

<h3 style="color: #1ABC9C;">Conclusion</h3>
<p>This project showcased the importance of end-to-end testing, ensuring both the front-end UI and back-end API layers work harmoniously. I was able to build a reliable, scalable, and automated testing process using Selenium and Postman. These automated tests reduced regression testing time significantly and helped maintain code quality across releases.</p>

<h3 style="color: #1ABC9C;">Additional Resources</h3>
<ul>
    <li><a href="https://github.com/your-repo/selenium-tests">View Selenium Test Repository</a></li>
    <li><a href="https://www.selenium.dev/">Selenium Official Website</a></li>
</ul>
<img src="https://example.com/selenium-dashboard.png" alt="Selenium Test Results" style="border: 1px solid #D6DBDF; padding: 5px;" />



### Languages and Tools:

<p align="left">
   <a href="https://www.w3schools.com/cs/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="csharp" width="40" height="40" /> </a>
   <a href="https://dotnet.microsoft.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dot-net/dot-net-original-wordmark.svg" alt="dotnet" width="40" height="40" /> </a>
   <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40" /> </a>
   <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40" /> </a>
   <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40" /> </a>
   <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="mongodb" width="40" height="40" /> </a>
   <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40" /> </a>
   <a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer"> <img src="https://www.svgrepo.com/show/303229/microsoft-sql-server-logo.svg" alt="mssql" width="40" height="40" /> </a>
   <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40" /> </a>
   <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40" /> </a>
     <a href="https://www.selenium.dev" target="_blank" rel="noreferrer"> <img  alt="selenium" width="40" height="40"   src="https://raw.githubusercontent.com/devicons/devicon/master/icons/selenium/selenium-original.svg"> </a>
   <a href="https://www.jenkins.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/jenkins/jenkins-icon.svg" alt="jenkins" width="40" height="40" /> </a>
   <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40" /> </a>
   <a href="https://postman.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="postman" width="40" height="40" /> </a>
</p>
