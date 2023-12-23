## How To Enable Group Policy Editor (gpedit.msc) In Windows 11  

The Group Policy Editor, also known as gpedit.msc, serves as a crucial administrative instrument for adjusting configurations on a Windows system.

Essentially, Gpedit offers a user-friendly approach to overseeing Windows settings via the Windows Registry. Modifications implemented in gpedit.msc promptly manifest in the Windows Registry.

Typically utilized by advanced users, the Gpedit.msc tool is regrettably not automatically integrated into Windows 10 Home. This tutorial outlines the steps to activate gpedit.msc in the Windows 10 Home edition.  

> Gpedit.msc is usually located in C:\Windows\System32 on all versions of Windows.  

### Cannot find ‘gpedit.msc’ error  

If you run gpedit.msc on Windows 10 Home, you will get the following error:

> Windows cannot find "gpedit.msc". Make sure you typed the name correctly, and then try again. 

### Run the following commands one after the other:

> FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")  
> FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")

These commands will install gpedit.msc console on your computer.

Taken from this [website](https://www.itechtics.com/enable-gpedit-windows-10-home/).