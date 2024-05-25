# Win 10 Courage Rice

### Win 10 Courage Rice - How to achieve my personal Rice!

## Required Software:

- []() : **
- []() : **
- []() : **
- []() : **
- []() : **
- []() : **




### Windows Translucency:

### A few things to make various parts of your Windows OS Translucent

- [TranslucentTB](https://github.com/TranslucentTB/TranslucentTB) - A lightweight utility that makes the Windows **taskbar** translucent/transparent.
- [TranslucentSM](https://github.com/rounk-ctrl/TranslucentSM) - A lightweight utility that makes the Windows **Start Menu** translucent/transparent
- [DWMBlurGlass](https://github.com/Maplespe/DWMBlurGlass) - Add custom effect to global system **title bar**, support win10 and win11.
- [ExplorerBlurMica](https://github.com/Maplespe/ExplorerBlurMica) - Add background Blur effect or Acrylic (Mica for win11) effect to **explorer** for win10 and win11.
- [TranslucentFlyouts](https://github.com/ALTaleX531/TranslucentFlyouts) - Translucent effect for most of the win32 **flyouts**.
- [Translucent Flyouts Config GUI](https://github.com/Satanarious/TranslucentFlyoutsConfig) - A configuration GUI for Translucent Flyouts


### QTTabBar: Media/File Preview on hover not working for a certain file extension:

1. First we going to start of be opening "QTTabBar Options" and navigate to "Preview".
2. Click on the "Extensions, font and color" tab, and click on either Picture, Movie & Music or Text depending on which file extension you would like to add to QTTabBar.
3. Type the file extensino in the empty input box for example ".aiff" and then click the plus button.
4. Click "Apply" and then "Ok" and then restart your explorer and see if you get a Preview of your file. If not, continue with these steps.
5. Navigate to [Download K-Lite Codec Pack](https://codecguide.com/download_kl.htm) to download the neccecary Codec Pack.
6. Download either "Full" or "Mega".
7. Go through the setup wizard and install the Codec Pack.
8. After this is done the media preview should be working.


### First: **How to Install PowerShell 7 on Windows 10 & get auto-completions**

> To enable auto-completions in PowerShell based on the history of commands, you can use the PSReadLine module, which provides an enhanced command-line editing experience in PowerShell. PSReadLine has features like syntax coloring, multi-line editing, and most importantly, predictive IntelliSense based on command history.

1. Fire up PowerShell and copy/paste the following cmdlet into the window:
  ```powershell
    iex "& { $(irm https://aka.ms/install-powershell.ps1) } -UseMSI"
  ```
2. Press the Enter key, and PowerShell will run the command and begin the download.
3. Go Through the Installer
4. Next, you get to decide which optional features to enable on the install. You can enable or disable the following four options:
- **Add PowerShell to Path Environment Variable:** Adds PowerShell to the Windows Path environment variable and allows you to call PowerShell from any other shell or terminal.
- **Register Windows Event Logging Manifest:** Adds PowerShell to the Windows Event Logging Manifest and allows you to log events from within a PowerShell instance.
- **Enable PowerShell Remoting:** Enables the ability to run commands remotely.
- **Add 'Open here' Context Menus to Explorer:** Adds an option inside the right-click context menu that opens an instance of PowerShell in the folder you click.
5. Once the setup wizard completes, click "Finish" to exit.

Now for the **auto-completions in PowerShell:** Here's how to enable and configure this functionality:

1. **Install PSReadLine Module (if not already installed)**:
   Open a PowerShell session and run the following command to install the PSReadLine module from the PowerShell Gallery:
   ```powershell
   Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
   ```

2. You need to create the "Microsoft.Powershell_profile.ps1" at the location of your profile.

Run the following in Powershell to create your Powershell Profile:
```powershell
  new-item -type file -path $profile -force
```

Execute the following to get the location of your profile:
```powershell
  $profile
```

The following command opens the "Current User, Current Host" profile in Notepad:
```powershell
  notepad $PROFILE
```

Now leave your Powershell Profile open in notepad, we will be adding some lines.

3. **Import the PSReadLine Module**:
   Now you need to import the module into your PowerShell session. You can do this by adding the following line to your PowerShell profile script (which is typically located at `$PROFILE`):
   ```powershell
   Import-Module PSReadLine
   ```

4. **Enable Prediction Based on History**:
   PSReadLine version 2.1.0 and later includes a feature called "Predictive IntelliSense." To enable this feature, add the following lines to your profile script:
   ```powershell
   Set-PSReadLineOption -PredictionSource History
   ```

   This command tells PSReadLine to use your command history for predictions.

4. **Customize PSReadLine Options (Optional)**:
   You can further customize PSReadLine to enhance your experience. Here are some useful options:
   ```powershell
   # Set the prediction style (available options: InlineView, ListView)
   Set-PSReadLineOption -PredictionViewStyle ListView

   # Enable/Disable predictive IntelliSense
   Set-PSReadLineOption -PredictionSource HistoryAndPlugin

   # Set the history save mode (SaveAtExit, SaveIncrementally)
   Set-PSReadLineOption -HistorySaveStyle SaveIncrementally

   # Set the maximum number of history items
   Set-PSReadLineOption -MaximumHistoryCount 4096
   ```

5. **Reload Your Profile**:
   After updating your profile script, you need to reload it to apply the changes. You can do this by running:
   ```powershell
   . $PROFILE
   ```

6. **Use Predictive IntelliSense**:
   With these settings, PowerShell will now provide auto-completions based on your command history as you type. For example, if you previously ran a long `Get-Process` command, typing `Get-` and pressing the **right arrow key** or Tab should show the suggestion from your history.

By following these steps, you will enable and configure PowerShell to suggest auto-completions based on your command history, making your command-line experience more efficient and user-friendly.

***






