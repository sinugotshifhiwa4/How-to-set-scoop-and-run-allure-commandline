# How-to-install-scoop-and-run-allure-commandline


To install Allure Report on Windows using Scoop, follow these steps:

1. **Ensure Scoop is Installed**:
   - If you haven't installed Scoop yet, you can do so by running the following commands in a non-admin PowerShell terminal:
     ```powershell
     Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
     Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
     ```

2. **Verify Java Installation**:
   - Make sure you have Java version 8 or above installed.
   - Set the `JAVA_HOME` environment variable to the Java installation directory.

3. **Install Allure**:
   - Open a PowerShell terminal and run:
     ```powershell
     scoop install allure
     ```

4. **Check Allure Version**:
   - Verify the installation by running:
     ```powershell
     allure --version
     ```

This will install the latest version of Allure Report via Scoop²³.

-----------------------------------------------------------------


Guide to create a Maven project with TestNG and Allure integration:

1. **Create a Maven Project**:
   - Open your IDE (e.g., IntelliJ IDEA, Eclipse) and create a new Maven project.

2. **Add Dependencies**:
   - Add the following dependencies to your `pom.xml` file:
     ```xml
     <dependencies>
         <!-- TestNG dependency -->
         <dependency>
             <groupId>org.testng</groupId>
             <artifactId>testng</artifactId>
             <version>7.4.0</version>
             <scope>test</scope>
         </dependency>
         <!-- Allure TestNG dependency -->
         <dependency>
             <groupId>io.qameta.allure</groupId>
             <artifactId>allure-testng</artifactId>
             <version>2.13.9</version>
         </dependency>
     </dependencies>
     ```

3. **Create a Test Class**:
   - Create a test class in your project. For example:
     ```java
     import org.testng.annotations.Test;
     import static org.testng.Assert.assertTrue;

     public class SampleTest {
         @Test
         public void sampleTest() {
             assertTrue(true);
         }
     }
     ```

4. **Create `testng.xml`**:
   - Create a `testng.xml` file in your project root directory:
     ```xml
     <!DOCTYPE suite SYSTEM "http://testng.org/testng-1.0.dtd" >
     <suite name="Suite">
         <test name="Test">
             <classes>
                 <class name="com.example.SampleTest"/>
             </classes>
         </test>
     </suite>
     ```

5. **Run the Test**:
   - Run the test using the `testng.xml` file. This will generate the `allure-results` folder with JSON files.

6. **Serve Allure Report**:
   - Open a command prompt and navigate to the directory containing the `allure-results` folder.
   - Run the following command:
     ```sh
     allure serve path\to\allure-results
     ```
   - This will start a local server and open the Allure report in your default web browser.
