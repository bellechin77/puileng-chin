import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;

public class SeleniumTest {
    public static void main(String[] args) {
        
        // Set path to the ChromeDriver (change the path according to your setup)
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");

        // Initialize WebDriver with Chrome
        ChromeOptions options = new ChromeOptions();
        options.addArguments("--headless");  // Run in headless mode (optional, useful for CI/CD)
        WebDriver driver = new ChromeDriver(options);

        try {
            // Step 1: Navigate to the login page
            driver.get("https://example.com/login");  // Replace with your actual URL

            // Step 2: Find the username field and enter a username
            WebElement usernameField = driver.findElement(By.id("username"));
            usernameField.sendKeys("myUsername");

            // Step 3: Find the password field and enter a password
            WebElement passwordField = driver.findElement(By.id("password"));
            passwordField.sendKeys("myPassword123");

            // Step 4: Find the login button and click it
            WebElement loginButton = driver.findElement(By.id("loginBtn"));
            loginButton.click();

            // Step 5: Verify login by checking if the logout button is displayed (or any other element that appears after login)
            WebElement logoutButton = driver.findElement(By.id("logoutBtn"));
            if (logoutButton.isDisplayed()) {
                System.out.println("Login successful! Logout button found.");
            } else {
                System.out.println("Login failed.");
            }

        } catch (Exception e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            // Step 6: Close the browser
            driver.quit();
        }
    }
}
