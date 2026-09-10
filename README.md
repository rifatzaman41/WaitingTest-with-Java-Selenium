# WaitingTest-with-Java-Selenium

#Fluent Wait

package com.fb;

import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.FluentWait;

public class Fluent {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
ChromeDriver driver=new ChromeDriver();
FluentWait<ChromeDriver>wait=new FluentWait<>(driver);

wait.withTimeout(Duration.ofSeconds(180));

wait.pollingEvery(Duration.ofSeconds(60));

wait.until(ExpectedConditions.visibilityOfElementLocated(By.linkText("Forget your password")));
	driver.findElement(By.linkText("Forget your password")).click();
	}

 #Implicit Wait & Explicit Wait

package com.fb;

import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;

public class wait {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
ChromeDriver driver=new ChromeDriver();
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(2));
driver.get("https://login.salesforce.com/?locate=in");
driver.findElement(By.id("username")).sendKeys("adminrian");
driver.findElement(By.id("password")).sendKeys("admin123");

WebDriverWait wait=new WebDriverWait(driver,Duration.ofSeconds(20));
	wait.until(ExpectedConditions.visibilityOfElementLocated(By.linkText("Forget your password")));
	driver.findElement(By.linkText("Forget your password")).click();
	}
}






  

  

  

}
