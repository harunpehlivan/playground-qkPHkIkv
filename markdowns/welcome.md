# Introduction!

Are you looking for a way to convert your existing Win32/WPF/Classic desktop applications to Universal Windows platform? Do not want to change any code? then go through this article, it will help you to convert your desktop apps to UWA (Universal Windows Apps) using **Project Centennial**

## Need for Universal Windows platform Apps

*Are you facing below problems in Classic Windows desktop/WPF/Win32 apps?*
 
![Dll-Hell](https://www.codeproject.com/KB/dotnet/1105994/dll_hell_1.png) 

1. Error in installations (Incomplete installations, access issue, registry failure, framework problem)
2. DLL hell issue (occur when same DLL is referring by multiple program but DLL is replaced due to version information is not persist by application)
3. Uninstallation issue (Does not Uninstall completely, Application un-install but registry key was not removed)
4. Application utilizing high System resources (Processor, RAM leads to hang up machine)
5. One click installation not possible
6. Performance issue
7. Want to run application on Windows 10

To over come such issues, we should move to UWA (Universal windows Apps), There are multiple links exist on internet that explain, how to build Universal windows Apps but none will explain, How to convert our existing Classic Windows/WPF/Win32 Desktop Apps to UWA ? The answer is **Project Centennial**

## What is Project Centennial ?

![Dll-Hell](https://www.codeproject.com/KB/dotnet/1105994/UWPPic.png)

Simply, it is nothing but useful desktop application convertor that will help developers to convert their desktop application/Win32/WPF classic application to UWA, Just you need to give your installer file (MSI) or .EXE file as an input and it will work on file and give you a .AppX or .AppXbundle file, that can be easily install on windows 10 and further more you can deploy that file to windows store. 

Project Centennial also gives a package identity to converted AppX/AppXbundle file (Package identity will be useful when deploy it to windows store)

According to Microsoft

*"Desktop App Converter is a pre-release tool that enables developers to bring their existing desktop apps written for .NET 4.6.1 or Win32 to the Universal Windows Platform. The developers can run their desktop installers through the converter in an unattended (silent) mode and obtain an AppX package that can be installed via the Add-AppXPackage PowerShell cmdlet on their development machine."*

[Ref: [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=51691)] 

## List of Features
1. Apps created by Project Centennial can get full Windows 10 leverages, Apps get smoothly installed using sideloading features Read here: [Sideloading features of Windows 10](https://technet.microsoft.com/en-us/itpro/windows/deploy/sideload-apps-in-windows-10)
2. As your APP has package identity, you can easily call UWA (Universal Windows Apps) API in your existing code.
3. User will experience window store like installation process as One click installation is possible.
4. Install and uninstall gets Intelligible as all required files and registry entries stored on single point, (In windows desktop Applications, where some temp files and few registry entries gets left behind even after you un-install application)
5. Overall System speed will not affect as registry entries will not span across all registry and installation files will be at single location (In Classic/Win32 Desktop application registry entries and installation files span across system and will load on system boot each time, so it will cost to system performance), as well as Window 10 will handle UWA differently than classic application so it ends up in resource and performance improvement
6. After conversion your output package will gifted with Windows Apps features like Great user interface with  XAML , Live tiles and updates, services, background work and more.
7. Windows store licensing and update amenity will be 'bydefault' applicable to your converted app
8. Once it converted to AppX, we can run it on different windows platform like Desktop, Mobile, XboX, Surface, Holographic Devices, IOT etc

![WUP](https://www.codeproject.com/KB/dotnet/1105994/WUP.png)

## Pre-requisite
It needs at least Windows 10 to be on system to run Project Centennial, Hardware could be a x64 processor with good amount of Memory

## How to use Project Centennial

First you need to download DesktopAppConverter.zip and then base image .wim file, both files can be downloaded from [Here](First you need to download DesktopAppConverter.zip and then base image .wim file, both files can be downloaded from)

Unzip 'DesktopAppConverter.zip' file on local system

Use power shell window with admin rights to install Convertor on your machine, see below command to install Desktop convertor

```Javascript
PS C:\> .\DesktopAppConverter.ps1 -Setup -BaseImage .\BaseImage-1XXXX.wim -Verbose
```

Successful run of above command will lead to reboot.

After reboot, you are almost ready to use App convertor, PowerShell or command prompt can be use to run this tool, you need to provide different parameters to run it like Installer, Destination, PackageName, Publisher and Version to AppX file (which is the output of the convertor program)

Syntax will be as below

```javascript
DesktopAppConverter.ps1
-Installer <String> [-InstallerArguments <String>] [-InstallerValidExitCodes <Int32>]
-Destination <String>
-PackageName <String>
-Publisher <String>
-Version <Version>
```

## Things to discuss
![WIN10](https://www.codeproject.com/KB/dotnet/1105994/win10_1.png)
It is really amazing Convertor that will convert your Classic Windows/Win32 EXE to directly AppX without any code change, additionally we will get all Windows Store Apps like benefits in bonus. Now Lets see, in future how Develoepers will treat this opprtunity and convert their EXE/MSI to AppX.

Hope it will help you all to Convert your existing Win32/Windows Classic/WPF applications to New world AppX

Happy Conversion to you !


-Prasad



### Reference

Fore more details and Usage you can switch to below link

[Windows Dev Center](https://msdn.microsoft.com/en-us/windows/uwp/porting/desktop-to-uwp-run-desktop-app-converter)



Please refer to the [documentation](https://tech.io/doc) to learn more about adding programming exercises within your contribution.

# Template Resources

[`markdowns/welcome.md`](https://github.com/TechDotIO/techio-basic-template/blob/master/markdowns/welcome.md)  
What you are reading here is generated by this file. Tech.io uses the [Markdown syntax](https://tech.io/doc/reference-markdowns) to render text, media and to inject programming exercises.


[`techio.yml`](https://github.com/TechDotIO/techio-basic-template/blob/master/techio.yml)  
This *mandatory* file describes both the table of content and the programming project(s). The file path should not be changed.
