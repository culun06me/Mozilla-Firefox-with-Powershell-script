# Mozilla-Firefox-with-Powershell-script

1. As an Administrator, start an elevated Powershell command-line.
2. Copy paste code from install command in the PowerShell window.

Here's a breakdown of what each line does:
1)	$SourceURL: Specifies the URL for the Firefox MSI installer.
2)	$Installer: Defines the path where the installer will be saved. It uses the system's temporary directory (typically "C:\Users<Username>\AppData\Local\Temp").
3)	Invoke-WebRequest: Downloads the Firefox MSI installer from the specified URL and saves it to the temporary directory.
4)	Start-Process: Initiates the installation process. It runs the installer silently with the "/s" switch, elevating the process to run with administrator privileges using the "-Verb RunAs" parameter, and waits for the installation to finish before proceeding.
5)	Remove-Item: Removes the downloaded MSI installer from the temporary directory to clean up after the installation.

   
Your script is a practical and automated way to install Firefox on a Windows system. Just ensure that you have the necessary permissions to run scripts and install software, and also note that the specific download URL you provided is for the MSI installer.
