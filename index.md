**SOFTWARE INSTALLATION AND CONFIGURATION GUIDE**

**Installing Visual Studio Code Using Windows Command Prompt (CMD)**

**Document Version:** 1.0  
**Document Type:** Command-Line Installation Guide  
**Audience:** Beginners, IT Support Professionals and Software Developers  
**Operating System:** Windows 10 / Windows 11

**Document Revision History**

| **Version** | **Date**         | **Description**          |
| ----------- | ---------------- | ------------------------ |
| 1.0         | 24 November 2026 | Initial document created |

**1\. Purpose**

This guide describes how to install Visual Studio Code on a Windows computer using Windows Command Prompt. It covers the basic requirements, installation commands, verification procedures and solutions to common installation problems.

It explains how to check the system requirements, verify the availability of Windows Package Manager (WinGet), execute the installation command and confirm that the application has been installed successfully.

This guide is intended for users who prefer command-line installation over the traditional graphical installation method.

**2\. Overview**

Visual Studio Code is a lightweight source-code editor developed by Microsoft. It supports multiple programming languages and provides features such as syntax highlighting, debugging, extensions and integrated terminal access.

Windows Package Manager (WinGet) is a command-line tool that allows users to discover, install, upgrade and manage applications on Windows.

Using WinGet, users can install Visual Studio Code directly through Command Prompt without manually downloading the installation file.

**3\. Prerequisites**

Before starting the installation, ensure that the following requirements are met:

- A computer running a supported version of Windows 10 or Windows 11.
- An active internet connection.
- Windows Package Manager (WinGet) installed and accessible.
- Sufficient disk space for the application.
- Appropriate user permissions to install software.

**Note:** WinGet is generally provided through Microsoft's App Installer package. If it is unavailable, update or install App Installer through the Microsoft Store.

**4\. Checking Windows Package Manager Availability**

Before installing Visual Studio Code, verify whether WinGet is available on your computer.

Follow these steps:

1. Press Windows + R on your keyboard.
2. Type "cmd" in the Run dialog box.
3. Press Enter to open Command Prompt.
4. Enter the following command:

winget --version

5. Press Enter.

**Expected Output:**

The command should display the installed WinGet version, for example:

v1.x.x

The exact version may vary depending on the installed release.

If a version number appears, WinGet is ready to use.

If Windows displays an error stating that 'winget' is not recognised, install or update the App Installer package and reopen Command Prompt.

**5\. Searching for Visual Studio Code**

Before installing the application, users can verify that the correct package is available in the WinGet repository.

Enter the following command:

winget search --id Microsoft.VisualStudioCode --exact

Press Enter to execute the command.

WinGet will search for the specified application package.

**Expected Result:**

The search results should display Visual Studio Code with the package ID:

Microsoft.VisualStudioCode

**Note:** The package ID helps identify the correct application and reduces the possibility of selecting an unrelated software package.

**6\. Installing Visual Studio Code Using CMD**

Once the package has been identified, follow the installation procedure below.

**Step 1: Open Command Prompt**

Open the Windows Start menu, search for Command Prompt and launch it.

**Step 2: Execute the Installation Command**

Enter the following command:

winget install --id Microsoft.VisualStudioCode --exact --source winget

Press Enter to begin the installation.

**Step 3: Review the Installation Prompts**

Depending on the WinGet configuration, Windows may display source agreements or other confirmation prompts.

Review the displayed information and accept the required agreements to continue.

**Step 4: Wait for Installation**

WinGet will download the Visual Studio Code installation package and execute the installer.

Allow the process to finish without closing the Command Prompt window.

**Step 5: Check the Installation Status**

After installation, WinGet should display a successful installation message.

For example:

Successfully installed

The exact confirmation message may vary depending on the WinGet version.

**7\. Verifying the Installation**

After installation, verify that Visual Studio Code is working correctly.

**Step 1: Check the Application Version**

Close and reopen Command Prompt to ensure that the updated system PATH is available.

Enter:

code --version

Press Enter.

**Expected Result:**

The command should display the installed Visual Studio Code version and additional build information.

**Note:** If the command is still not recognised after reopening Command Prompt, check whether the VS Code installation directory has been added to the system PATH.

**Step 2: Launch Visual Studio Code**

To open the application through Command Prompt, execute:

code

The Visual Studio Code application should launch.

**Step 3: Open a Project Folder**

Users can also open an existing project folder directly from Command Prompt.

For example:

cd C:\\Users\\Public\\Documents

code .

The first command navigates to the specified directory, while the second opens that folder in Visual Studio Code.

**8\. Installing an Extension Using CMD (Optional)**

Visual Studio Code supports extensions that provide additional functionality.

For example, users working with Python can install the official Python extension published by Microsoft.

Execute the following command:

code --install-extension ms-python.python

Press Enter to install the extension.

After installation, the extension will be available in Visual Studio Code.

**Important:** Installing the Python extension does not install the Python interpreter. Python must be installed separately if users want to execute Python programs.

**9\. Troubleshooting Common Installation Issues**

The following table describes common problems that may occur during installation and their recommended solutions.

| **Issue**                    | **Possible Cause**                                              | **Recommended Solution**                                         |
| ---------------------------- | --------------------------------------------------------------- | ---------------------------------------------------------------- |
| 'winget' is not recognised   | WinGet is unavailable or not properly configured.               | Install or update Microsoft's App Installer package.             |
| Package not found            | Incorrect package ID or unavailable package source.             | Verify the package ID and check the WinGet source.               |
| Installation fails           | Network interruption or insufficient permissions.               | Check the internet connection and review the installation error. |
| 'code' is not recognised     | Command Prompt has not refreshed the PATH environment variable. | Close and reopen Command Prompt.                                 |
| Extension installation fails | Network connectivity or extension marketplace issue.            | Check the internet connection and retry the command.             |
| Application does not launch  | Installation may be incomplete or corrupted.                    | Review the installation status and reinstall if necessary.       |

**Additional Support:**

If the installation continues to fail, execute the following command to check the available WinGet sources:

winget source list

Review the output and confirm that the required package source is available.

**10\. Important Installation Considerations**

Before using WinGet for software installation, consider the following points:

- Always verify the application package ID before executing an installation command.
- Use official and trusted software sources.
- Maintain a stable internet connection throughout the installation.
- Avoid closing Command Prompt while the installation is running.
- Restart Command Prompt after installation if the code command is not recognised.
- Ensure that the installed application is compatible with the operating system.

**11\. Conclusion**

Installing Visual Studio Code through Windows Command Prompt provides a convenient alternative to traditional graphical installation.

By using Windows Package Manager, users can download and install the application through a single command. The additional verification and troubleshooting steps help confirm that the installation has been completed successfully.

Using WinGet simplifies the installation process and eliminates the need to download the installer manually. This approach is useful for developers and IT support professionals who prefer managing software through command-line tools.

**12\. References**

1. Microsoft. Visual Studio Code Documentation. <https://code.visualstudio.com/docs>
2. Microsoft. Visual Studio Code Download. <https://code.visualstudio.com/>
3. Microsoft. Windows Package Manager Documentation. <https://learn.microsoft.com/en-us/windows/package-manager/winget/>
