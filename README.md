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
