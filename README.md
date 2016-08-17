# hello-world
//Create a new repository-example-practice
/*Este es un ejemplo con Selenium WebDriver*/

package TestCases;

import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.testng.annotations.Test;

public class FirstTest {

	@Test
	public void FirstTest() {
		WebDriver driver = new FirefoxDriver();
		  driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		driver.get("http://unvirtual.medellin.unal.edu.co/");

		driver.findElement(By.xpath(".//*[@id='yui_3_17_2_1_1471447945662_184']")).click();

		driver.findElement(By.id("username")).sendKeys("lacalvarezga");
		driver.findElement(By.id("password")).sendKeys("0");
		driver.findElement(By.id("loginbtn")).click();

	}
}


