package gk.sample;
import io.github.bonigarcia.wdm.WebDriverManager;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.firefox.FirefoxOptions;
import org.testng.Assert;
import org.testng.annotations.Test;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.AfterTest;


public class gotowomensPageTest {

    public WebDriver driver;

    @BeforeTest
    public void setBaseURL() {
        FirefoxOptions capabilities = new FirefoxOptions();
        WebDriverManager.firefoxdriver().setup();
        driver = new FirefoxDriver(capabilities);
        driver.get("http://automationpractice.com/index.php");
    }



    @Test
    public void Gotowebsiteandclickwomenstab() throws InterruptedException {
        String title = driver.getTitle();
        //check if the page title is correct
        Assert.assertEquals(title, "My Store");
        //click on the women tab
        driver.findElement(By.linkText("Women")).click();
        Thread.sleep(1000);
        //wait for the page to load
        driver.findElement(By.xpath("/html/body/div/div[2]/div/div[3]/div[1]/div[1]/h2")).isDisplayed();
        System.out.println("Test passed - succesffully reached the womens page");
    }

    @AfterTest
    public void endSession() {
        driver.quit();
    }


}
