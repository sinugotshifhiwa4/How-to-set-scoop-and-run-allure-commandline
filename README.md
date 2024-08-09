# How-to-install-scoop-and-run-allure-commandline

1. **Set the Execution Policy**:
   ```powershell
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

2. **Install Scoop**:
   ```powershell
   Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
   ```

Once you've run these commands, Scoop should be installed and ready to use.



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
