# cursedwindowsupgrades
A comprehensive list on how to unlock a bunch of unintended Windows upgrade paths, bypassing artificial blocks. \
While those update paths do work, **DO NOT USE THEM IF YOU HAVE IMPORTANT DATA ON YOUR MACHINE!** \
Also, note that if your hardware cannot run the Windows version you are upgrading to, **IT WILL NOT WORK**.
With that said, we can now begin:


## Windows XP x64 to Windows Vista x64
Credits: [Heathercat123](https://heathercat123.github.io)

### Requirements
- [The x64 version of Application Verifier 4.0](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/ApplicationVerifier.amd64.msi)
- An x64 Windows Vista CD or ISO
- A machine running Windows XP x64 Edition

### Upgrade process
1. Open *Application Verifier 4.0 (x64)
1. Click on *File*, press *Add Application*
1. Navigate to the *sources* folder from your Windows Vista disc, click on *setup.exe*, then hit *Open*
1. Uncheck *Basics*, expand *Compatibility*, then check *HighVersionLie*
1. Right click *HighVersionLie*, then hit *Properties*
1. Set *Major version* to 5, *Minor version* to 1, *Build number* to 2600 and *Service pack major* to 3
1. Press *OK*, then press *Save*
1. From the *sources* folder on your Windows Vista disc open *setup.exe*
1. On the *Get important updates for installation* page, hit *Do not get the latest updates for installation*
1. On the product key page, hit *Next*, then *No*
1. On the license terms page, check *I accept the license terms*, then hit *Next*
1. You will now see the option to upgrade. Click it.
1. If you see the *Compatibility Report* page, hit *Next*
Windows will now upgrade flawlessly!



## Windows NT 3.51 to XP
Credits: [Windows 386 on BetaArchive](https://www.betaarchive.com/forum/viewtopic.php?t=26847)

### Requirements
- An English Windows NT 3.51 install
- A Windows XP Professional SP3 English disc or ISO
- [nLite](https://nliteos.com/)
- [A program capable of extracting 7z and ISO files](https://7-zip.org/) (not included in this repository due to it not being abandonware)
- [WINNT351toXP.7z](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/WINNT351toXP.7z)

### Upgrade process
1. Extract your Windows XP ISO or copy its content to a folder if it's a disc
1. Extract WINNT351toXP and copy its content to the root of the extracted Windows XP installer
1. Open nLite
1. Hit next on the *Welcome to nLite!* page
1. On the *Locating the Windows installation* page, click on *Browse* and select the extracted Windows XP installer and then hit next
1. On the *Presets* page, hit next
1. On the *Task Selection* page, click on *Bootable ISO*, then click next
1. On the *Bootable ISO* page, click on *Make ISO*
1. When it's done, hit next
1. Now, hit finish
1. Insert the ISO into your Windows NT 3.51 virtual machine, or burn it to a CD then insert it if it's a physical machine
1. In Windows NT 3.51, navigate to *D:\\i386\\* and launch *WINNT35.exe*
1. Finally, you can upgrade!
Everything should now just work.



## Windows ME to 2000
Credits: [Skye](https://www.youtube.com/watch?v=V-X8DYejJm0)

### Requirements
- A Windows 2000 disc or ISO
- A machine running Windows ME, virtual or not

### Upgrade process
1. Put the disc or ISO into your Windows ME machine
It's a common misconception to think that Windows ME cannot be upgraded to Windows 2000, probably due to the fact the ME released after Windows 2000. However, this is an official and intended upgrade path.



## Windows XP to Windows Server 2003
Credits: Pinky, [Skye](https://skyeweeb.weebly.com/)

### Requirements
- [The 32 bit version of Application Verifier 4.0](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/ApplicationVerifier.x86.msi)
- [TweakNT](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/TweakNT.zip)
- A 32 bit Windows Server 2003 disc or ISO
- A machine running 32 bit Windows XP

### Upgrade process
1. Open *Registry Editor* (regedit)
1. Go to *HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\WPAEvents* and set OOBETimer to *FF FF FF FF FF FF FF FF FF FF FF FF*
1. Right click the *WPAevents* key and click on *Permissions...*
1. Click on *SYSTEM* and check both checkboxes under *Deny*
1. Now, press on *Apply* and hit *Yes*. You can now close the *Registry Editor*.
1. Open a *Command Prompt* (cmd)
1. Execute `cd %windir%\system32\oobe` and then `msoobe /a`
1. If an *Activate Windows* window pops up which says that this copy of Windows must be activated, you are good to go! If it does not, then go back to step 1
1. Now that you've confirmed that Windows is NOT activated, you can close the window
1. Set the theme to *Windows Classic* to avoid graphical glitches
1. Open TweakNT
1. Check *Convert to:*, select *Server*, and then select the SKU of Windows Server which is on your CD or ISO
1. Hit *Apply*, click *Yes* and then press *Ok*
1. In case of a SYSTEM_LICENSE_VIOLATION BSOD, you must reinstall Windows
1. Your bootscreen should now say *Microsoft Windows Server Family*, but this is still Windows XP
1. Copy the contents of your Windows Server 2003 disc to a folder on your hard drive
1. Navigate to that folder, go to i386 and then rename *WINNT32.exe* to whatever your heart desires, as long as the file extensions stays *.exe*
1. Launch Application Verifier, click on *File*, then *Add Application*
1. Find your renamed *WINNT32.exe*, then press *Open*
1. Uncheck *Basics*, expand *Compatibility*, then check *HighVersionLie*
1. Right click *HighVersionLie*, then hit *Properties*
1. Set *Major version* to 5, *Minor version* to 2 and *Build number* to 3718
1. Press *OK*, then press *Save*
1. Open your renamed *WINNT32.exe*
1. You can now upgrade! Do it!
1. If you get any driver errors during the upgrade, just hit *No*



## Windows Server 2003 to Windows XP
Credits: Pinky

### Requirements
- [The 32 bit version of Application Verifier 4.0](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/ApplicationVerifier.x86.msi)
- [The XP Conversion Pack](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/xpconv.exe)
- A 32 bit Windows XP disc or ISO
- A machine running 32 bit Windows Server 2003

### Upgrade process

If you are on a Corporate/VL version:
1. Open *Registry Editor* (regedit)
1. Go to *HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\WPAEvents* and set OOBETimer to *FF FF FF FF FF FF FF FF FF FF FF FF*
1. Right click the *WPAevents* key and click on *Permissions...*
1. Click on *SYSTEM* and check both checkboxes under *Deny*
1. Now, press on *Apply* and hit *Yes*. You can now close the *Registry Editor*.
1. Open a *Command Prompt* (cmd)
1. Execute `cd %windir%\system32\oobe` and then `msoobe /a`
1. If an *Activate Windows* window pops up which says that this copy of Windows must be activated, you are good to go! If it does not, then go back to step 1
1. Now that you've confirmed that Windows is NOT activated, you can close the window

If you are on a Retail copy or you are finished with the steps above:
1. Launch the XP Conversion Pack
1. On the Welcome page, hit *Next >*
1. On the *Donation* page, hit *Next >*
1. On the *Working mode optimization* page, select *Workstation*, then hit *Next >*
1. On the *Windows Server 2003/Windows XP conversion* page, check *I want to apply Windows Server 2003/Windows XP conversion*, then hit *Next >*
1. On the *Server security configuration* page, hit *Next >*
1. On the *Features configuration* page, hit *Next >*
1. On the *Hidden Services configuration* page, hit *Next >*
1. On the *XP Missing Features configuration* page, hit *Next >*
1. On the *Setting up tasks* page, hit *Next >*
1. On the *The optimization is ready to start* page, hit *Optimize*
1. When it asks you to restart, hit *Restart* and wait for the timer to go to 0
1. Once you log in, wait for the new timer to go to 0
1. After that restart, copy the contents of your Windows XP disc to a folder on your hard drive
1. Navigate to that folder, go to i386 and then rename *WINNT32.exe* to whatever your heart desires, as long as the file extensions stays *.exe*
1. Launch Application Verifier, click on *File*, then *Add Application*
1. Find your renamed *WINNT32.exe*, then press *Open*
1. Uncheck *Basics*, expand *Compatibility*, then check *HighVersionLie*
1. Right click *HighVersionLie*, then hit *Properties*
1. Set *Major version* to 5, *Minor version* to 1 and *Build number* to 2526
1. Press *OK*, then press *Save*
1. Open your renamed *WINNT32.exe*
1. You can now upgrade! Just do it!
1. On the *Who will use this computer?* page of the OOBE, hit *Skip* if you want to keep your account.
1. If you hear an error sound during the *welcome* screeen, press CTRL, ALT and DELETE simultaneously and press *OK* on every error box you see
Expect a pretty broken install of Windows XP after this.



## Longhorn to Windows XP
Credits: Pinky, [Skye](https://skyeweeb.weebly.com/)

### Requirements
- [The 32 bit version of Application Verifier 4.0](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/ApplicationVerifier.x86.msi)
- A 32 bit Windows XP disc or ISO
- A machine running 32 bit Longhorn build 4053 or older

### Upgrade process
1. Copy the contents of your Windows XP disc to a folder on your hard drive
1. Navigate to that folder, go to i386 and then rename *WINNT32.exe* to whatever your heart desires, as long as the file extensions stays *.exe*
1. Launch Application Verifier, click on *File*, then *Add Application*
1. Find your renamed *WINNT32.exe*, then press *Open*
1. Uncheck *Basics*, expand *Compatibility*, then check *HighVersionLie*
1. Right click *HighVersionLie*, then hit *Properties*
1. Set *Major version* to 5, *Minor version* to 1 and *Build number* to 2526
1. Press *OK*, then press *Save*
1. Open your renamed *WINNT32.exe*
1. On the *Welcome to Windows setup* page, hit *Next >*
1. On the *License Agreement* page, check *I accept this agreement*, then hit *Next >*
1. On the *Get Updated Setup Files* page, check *No*, then hit *Next >*
1. When it's about to restart, you may see a dialog warning you what other users are still using your computer. Just click *Yes*
1. After the second restart, you will see many copy errors. Hit *Cancel*, then hit *Yes* on each and every one of them
1. The OOBE may lack music, but it will still function as usual
1. When you arrive at the desktop, right click on it, press *Properties*, then set the theme to whatever you want, but please avoid the broken *Consumer* theme!
1. You can delete the *File a Longhorn Bug* icon if you want to



## Windows XP to Windows 7
Credits: [Skye](https://skyeweeb.weebly.com/) \
Notice: The current method of upgrading breaks networking and audio and doesn't automatically transfer your programs and data

### Requirements
- A Windows 7 disc or ISO
- A Windows Vista disc or ISO
- A machine running Windows XP

### Upgrade process
1. Create a folder on your hard disc, then create another folder in it called *sources*
1. Navigate to the sources folder from your Windows 7 disc
1. Copy *install.wim* and every *install_Windows 7 [edition].cfg* file to the *sources* folder which you created earlier
1. Copy everything from your Windows Vista disc to your folder, except the *sources* subfolder
1. Copy everything except *install.wim* and every *install_Windows Vista [edition].cfg* from your disc's *sources* folder to the one which you created earlier
1. Run *setup.exe* from the root of your folder
1. Hit *Install now*
1. On the *Get important updates for installation* page, hit *Do not get the latest updates for installation*
1. On the product key page, hit *Next*, then *No*
1. If you are on Windows XP Professional, select *Windows 7 ULTIMATE* or *Windows 7 PROFESSIONAL*. If you are on Windows XP Starter Edition, select *Windows 7 STARTER*. Else, select *Windows 7 HOMEBASIC* or Windows 7 *HOMEPREMIUM*
1. Check *I have selected the version of Windows that I purchased* and hit *Next*
1. On the license terms page, check *I accept the license terms*, then hit *Next*
1. You will now see the option to upgrade. Click it.
1. If you see the *Compatibility Report* page, hit *Next*
1. After the second restart, you will see *Windows could not start the installation process.*
1. Press Shift and F10 simultaneously, type *regedit*, then press Enter
1. Navigate to *HKEY_LOCAL_MACHINE\SYSTEM\setup*
1. Double click on *CmdLine*, set it to *cmd.exe*, then hit *OK*
1. Double click on *OOBEInProgress*, set it to *0*, then hit *OK*
1. Double click on *SetupPhase*, set it to *0*, then hit *OK*
1. Double click on *SetupType*, set it to *0*, then hit *OK*
1. Double click on *SystemSetupInProgress*, set it to *0*, then hit *OK*
1. Double click on *Upgrade*, set it to *0*, then hit *OK*
1. Close *Registry Editor*
1. In *cmd*, execute `shutdown -r -t 0`
1. After you arrive at the desktop, you'll have to manually reinstall drivers
1. Every file you had on Windows XP is located inside *C:\\$WINDOWS.~Q\\DATA*
1. Moving every folder from *C:\\$WINDOWS.~Q\\DATA* to *C:\\* to bring your programs back



## Windows Vista to Windows 8
Credits: [Skye](https://skyeweeb.weebly.com/) \
Notice: The current method of upgrading doesn't automatically transfer your programs

### Requirements
- Application Verifier [x86](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/ApplicationVerifier.x86.msi) or [x64](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/ApplicationVerifier.amd64.msi), depending on your Windows install's architecture
- A Windows 8 disc or ISO. Windows 8.1 or above will not work.
- A machine running Windows Vista

### Upgrade process
1. Open Application Verifier. Make sure to use the x64 version if you are on an x64 Windows install!
1. Click on *File*, press *Add Application*
1. Navigate to the *sources* folder from your Windows 8 disc, click on *installprep.exe*, then hit *Open*
1. Uncheck *Basics*, expand *Compatibility*, then check *HighVersionLie*
1. Right click *HighVersionLie*, then hit *Properties*
1. Set *Major version* to 6, *Minor version* to 1, *Build number* to 7601, *Service pack major* to 1 and *Service pack minor* to 1
1. Press *OK*, then press *Save*
1. From the *sources* folder on your Windows 8 disc, open *installprep.exe*
1. When the installer launches, select *No, thanks* on the *Get important updates* page
1. On the *Product key* page, make sure you enter a Windows 8 Pro key if you are running Windows Vista Business, Enterprise, or Ultimate
1. The rest of setup will go as usual
1. In the OOBE, on the *Sign in to your PC* page, hit *Skip*



## Windows 7 to Windows 11
Credits: [NTDev](https://ntdev.blog/), [Skye](https://skyeweeb.weebly.com/)

### Requirements
- [GImageX](https://github.com/heathercat123/cursedwindowsupgrades/raw/refs/heads/master/gimagex.zip)
- A Windows 11 disc or ISO
- A Windows 10 1507 or 1511 (RTM or November Update) x64 disc or ISO
- A machine running Windows 7 x64

### Upgrade process
1. Create a folder on your hard disc, then create another folder in it called *sources*
1. Copy the contents except the *sources* folder of your Windows 10 disc to this new folder
1. Copy everything except *install.wim* from your disc's *sources* folder to to the *sources* folder which you created earlier
1. From your Windows 11 disc's *sources* folder, copy *install.wim* to your hard drive. Do not copy it to your *sources* folder!
1. Create another folder on your hard drive in which the WIM will be extracted to later
1. Open GImageX
1. Go to the *Info* tab, click on *Browse...*, select your *install.wim* then click on *Get Info*. Note the number next to the SKU which you want to install.
1. Go to the *Mount* tab
1. Next to *Mount Point*, press *Browse...* then select your empty folder
1. Next to *Source* click on *Browse...* then select your *install.wim*
1. Set *Image* to the number you noted from the *Info* tab
1. Check *Read and Write*, then hit *Mount*
1. Go to your folder and navigate to *Windows\servicing\Editions\*
1. Open *UpgradeMatrix.xml* in *Notepad*
1. Scroll to the SKU you want then paste these lines:
```
		<SourceEdition ID="HomeBasic" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="true" cleanInstall="true"/>
		<SourceEdition ID="HomeBasicN" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="false" cleanInstall="true"/>
		<SourceEdition ID="HomePremium" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="true" cleanInstall="true"/>
		<SourceEdition ID="HomePremiumN" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="false" cleanInstall="true"/>
		<SourceEdition ID="Professional" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="true" cleanInstall="true"/>
		<SourceEdition ID="ProfessionalN" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="false" cleanInstall="true"/>
		<SourceEdition ID="Starter" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="true" cleanInstall="true"/>
		<SourceEdition ID="StarterN" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="false" cleanInstall="true"/>
		<SourceEdition ID="Ultimate" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="true" cleanInstall="true"/>
		<SourceEdition ID="UltimateN" processorArchitecture="amd64" versionRange="win7" dataOnly="true" dataSetting="false" fullUpgrade="false" cleanInstall="true"/>
```
1. Hit *File*, then *Save As...*
1. Navigate to somewhere else, press *Text Documents (\*.txt)*, change it to *All Files*, add *.xml* at the end of the file name then click *Save*
1. Right click the original *UpgradeMatrix.xml*, click on *Properties*, *Security*, then *Advanced*
1. Go to the *Owner* tab, hit *Edit* and *Other users or groups...*
1. Type your username, then press *OK*
1. Click *OK* on every dialog until you're back at the properties dialog
1. Hit *Edit*
1. Press *Administrators*, check *Full control*, then press *Ok* and press it again
1. Replace *UpdateMatrix.xml* with your version by copying it to the *Editions* folder
1. Go back to GImageX, click the item in the *Unmount* box, check *Commit Changes*, then hit *Unmount*
1. Close GImageX and move your *install.wim* to the *sources* folder on your hard drive
1. Launch *SetupPrep.exe*
1. When the installer launches, select *No, thanks* on the *Get important updates* page
1. The rest of setup will go as usual
1. In the OOBE, disable *Advertising ID*
The *Go back* option in the settings does not work and your drivers don't transfer, but the rest works flawlessly



## Windows 8 or 8.1 to Windows 11
Credits: [Skye](https://skyeweeb.weebly.com/)

### Requirements
- A Windows 11 disc or ISO
- A Windows 10 1507 or 1511 (RTM or November Update) x64 disc or ISO
- A machine running Windows 8/8.1 x64

### Upgrade process
1. Just upgrade as if you were going from 10 to 11
1. In the OOBE, all of the privacy settings are turned on. You can turn them off.
The *Go back* option in the settings does not work, your drivers don't transfer and the Windows 8 UWP apps may not work, but the rest works flawlessly



## Windows 11 to Windows 10
Credits: [LagLife](https://www.youtube.com/@laglife)

### Requirements
- [IDA Free](https://out7.hex-rays.com/files/idafree84_windows.exe) (not included in this repository due to it not being abandonware)
- [System Informer](https://www.systeminformer.com/downloads.php) (not included in this repository due to not being abandonware)
- A Windows 10 2004 or higher x64 disc or ISO
- A machine running Windows 11

### Upgrade/Downgrade process
1. Create a folder on your hard drive, then copy everything from the Windows 10 disc to it
1. Open IDA as an Administrator and, from your new folder, open *sources\\setupcompat.dll*
1. Allow IDA to search to symbols
1. Hit ALT and T simultaneously and search for the function *ConX::Setup::Common:CWindowsVersionIsLaterThan*, then select *Find all occurances*
1. Click on the one with no *Instruction*, scroll all the way to the bottom, then pick the label with *mov eax, 1*
1. Click on *Edit*, *Patch Program*, then *Change byte*
1. Change `B8 01` to `B8 00` and hit *OK*
1. Save
1. Go to *Edit*, *Patch program* and click *Apply patches to input file...*, then click *OK*
1. Launch *setup.exe* from your folder you created earlier
1. On the *Get important updates* page, select *No, thanks*
1. Let it downgrade!
1. After the first time setup, you will receive a black screen. Hit CTRL, ALT and DELETE simultaneously and select *Task Manager*
1. Press ALT and TAB simultaneously, then individually hit ALT, O then A. You should now see the *Task Manager*
1. Go to *Details*, find *explorer.exe*, press it then hit *End task*
1. Go to *File* ->  *Run new task*, type *explorer.exe*, then press *OK*
1. Navigate to *C:\ProgramData\Microsoft\Windows*
1. Right click on *AppxRepository*, click on *Properties*, *Security*, then *Advanced*
1. Next to *Owner*, hit *Change*, type your username, press *OK*, check *Replace owner on subcontainers and objects*, then hit *Ok*
1. Click on *Advanced* again, press *Change permissions*, *Add*, then *Select a principal*
1. Type your username, then press *OK*
1. Check *Full control*, then press *OK*, then press it again, and again
1. Open *System Informer*
1. In the *Services* tab, search for *AppXSvc*, right click on it, then hit *Stop*
1. Search for *StateRepository* and stop it too
1. Close *System Informer*
1. Right click on the Start button and click on *Windows Powershell (Admin)*
1. Execute these commands:
```
del "C:\ProgramData\Microsoft\Windows\AppRepository\StateRepository*"
add-appxpackage -register "C:\Windows\SystemApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Windows\ImmersiveControlPanel\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
```
Running the last command thrice is necessary.
1. Restart your computer
1. If you see a black screen: end *explorer.exe* in *Task Manager* like we did earlier
1. Right click the taskbar and open its settings, then find *Turn system icons on or off*.
1. Turn *Clock*, *Volume*, *Network*, *Action Center* and *Power* if it's available
1. If you are on 21H2 or older, disable Windows Update



## Windows 10 20H2+ to Windows 10 2004
Credits: [LagLife](https://www.youtube.com/@laglife) \
Note: The process to downgrade Windows 10 1909 to 1903 may be similar. However, it is untested.

### Requirements
- [IDA Free](https://out7.hex-rays.com/files/idafree84_windows.exe) (not included in this repository due to it not being abandonware)
- A Windows 10 2004 disc or ISO
- A machine running Windows 10 20H2 or higher

### Downgrade process
1. Create a folder on your hard drive, then copy everything from the 2004 disc to it
1. Open IDA as an Administrator and, from your new folder, open *sources\\setupcompat.dll*
1. Allow IDA to search to symbols
1. Hit ALT and T simultaneously and search for the function *ConX::Setup::Common:CWindowsVersionIsLaterThan*, then select *Find all occurances*
1. Click on the one with no *Instruction*, scroll all the way to the bottom, then pick the label with *mov eax, 1*
1. Click on *Edit*, *Patch Program*, then *Change byte*
1. Change `B8 01` to `B8 00` and hit *OK*
1. Save
1. Go to *Edit*, *Patch program* and click *Apply patches to input file...*, then click *OK*
1. Launch *setup.exe* from your folder you created earlier
1. On the *Get important updates* page, select *No, thanks*
1. Let it downgrade!
1. After you've arrived at the desktop, disable Windows Update
The downgrade should now just work!



## Windows 10 2004+ to Windows 10 1903 or 1909
Credits: [LagLife](https://www.youtube.com/@laglife) \
Notice: **THIS WILL DELETE ALL OF YOUR UWP APPS**

### Requirements
- [IDA Free](https://out7.hex-rays.com/files/idafree84_windows.exe) (not included in this repository due to it not being abandonware)
- [A program capable of extracting WIM files](https://7-zip.org/) (not included in this repository either due to not being abandonware)
- A Windows 10 1903 or 1909 disc/ISO
- A machine running Windows 10 20H2 or higher

### Downgrade process
1. Create a folder on your hard drive, then copy everything from the 1903/1909 disc to it
1. Open IDA as an Administrator and, from your new folder, open *sources\\setupcompat.dll*
1. Allow IDA to search to symbols
1. Hit ALT and T simultaneously and search for the function *ConX::Setup::Common:CWindowsVersionIsLaterThan*, then select *Find all occurances*
1. Click on the one with no *Instruction*, scroll all the way to the bottom, then pick the label with *mov eax, 1*
1. Click on *Edit*, *Patch Program*, then *Change byte*
1. Change `B8 01` to `B8 00` and hit *OK*
1. Save
1. Go to *Edit*, *Patch program* and click *Apply patches to input file...*, then click *OK*
1. Launch *setup.exe* from your folder you created earlier
1. Wait until you get to the desktop
1. Navigate to *C:\ProgramData\Microsoft\Windows*
1. Right click on *AppxRepository*, click on *Properties*, *Security*, then *Advanced*
1. Next to *Owner*, hit *Change*, type your username, press *OK*, check *Replace owner on subcontainers and objects*, then hit *Ok*
1. Click on *Advanced* again, press *Change permissions*, *Add*, then *Select a principal*
1. Type your username, then press *OK*
1. Check *Full control*, then press *OK*, then press it again, and again
1. Open *System Informer*
1. In the *Services* tab, search for *AppXSvc*, right click on it, then hit *Stop*
1. Search for *StateRepository* and stop it too
1. Close *System Informer*
1. Right click on the Start button and click on *Windows Powershell (Admin)*
1. Execute `rd /s /q "C:\Program Files\WindowsApps"`. This will delete all of your UWP apps
1. Launch a new *File Explorer* windows, navigate the *sources* folder in your Windows 10 1903/1909 disc and open *install.esd* in 7-Zip, then navigate to *\1\Program Files*
1. Copy *WindowsApps* from 7-Zip to your desktop
1. If you see a *This destination has files with the same names* box, click on *Replace the files in the destination*
1. Move the folder to *C:\Program Files*
1. Go back to Powershell and execute these commands:
```
del "C:\ProgramData\Microsoft\Windows\AppRepository\StateRepository*"
add-appxpackage -register "C:\Windows\SystemApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Windows\ImmersiveControlPanel\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
```
Running the last command thrice is necessary.
1. Restart your computer
1. Disable Windows Update
Your Windows downgrade is now ready for use!



## Windows 10 1903 or 1909 to Windows 10 1809
Credits: [LagLife](https://www.youtube.com/@laglife) \
Note: This may also work with Windows 10 2004+ as a base, including Windows 11. However, it is untested. \
Notice: **THIS WILL DELETE ALL OF YOUR UWP APPS**

### Requirements
- [IDA Free](https://out7.hex-rays.com/files/idafree84_windows.exe) (not included in this repository due to it not being abandonware)
- [A program capable of extracting WIM files](https://7-zip.org/) (not included in this repository either due to not being abandonware)
- A Windows 10 1809 disc/ISO
- A machine running Windows 10 1903 or 1909

### Downgrade process
1. Sign out of your Microsoft account if you are signed into any
1. Create a folder on your hard drive, then copy everything from the 1809 or 1803 disc to it
1. Open IDA as an Administrator and, from your new folder, open *sources\\setupcompat.dll*
1. Allow IDA to search to symbols
1. Hit ALT and T simultaneously and search for the function *ConX::Setup::Common:CWindowsVersionIsLaterThan*, then select *Find all occurances*
1. Click on the one with no *Instruction*, scroll all the way to the bottom, then pick the label with *mov eax, 1*
1. Click on *Edit*, *Patch Program*, then *Change byte*
1. Change `B8 01` to `B8 00` and hit *OK*
1. Save
1. Go to *Edit*, *Patch program* and click *Apply patches to input file...*, then click *OK*
1. Disable your internet connection
1. Launch *setup.exe* from your folder you created earlier
1. Let it install until the first restart
1. Boot into the Windows 10 installer from a disc or an USB key. If you were copying ISOs between machines before, you'll need to actually burn it to a DVD or flash it to a USB key to boot from it.
1. When it loads, press Shift and F10 simultaneously, type *regedit*, then press Enter
1. Click on *HKEY_LOCAL_MACHINE*, go to *File* -> *Load Hive...* and select *C:\WINDOWS\System32\config\SAM*
1. When it asks for a key name, you can use whatever you want. I recommand using *sam2*
1. Expand this new key and go to the *SAM* subkey inside of it
1. Double click on *C* and replace the *09* at the beginning by *08*
1. Click on *sam2*, then go to *File* -> *Unload hive...*
1. Close the *Registry Editor*
1. In *cmd*, execute `wpeutil reboot`
1. Wait until Windows gets to the desktop
1. Navigate to *C:\ProgramData\Microsoft\Windows*
1. Right click on *AppxRepository*, click on *Properties*, *Security*, then *Advanced*
1. Next to *Owner*, hit *Change*, type your username, press *OK*, check *Replace owner on subcontainers and objects*, then hit *Ok*
1. Click on *Advanced* again, press *Change permissions*, *Add*, then *Select a principal*
1. Type your username, then press *OK*
1. Check *Full control*, then press *OK*, then press it again, and again
1. Open *System Informer*
1. In the *Services* tab, search for *AppXSvc*, right click on it, then hit *Stop*
1. Search for *StateRepository* and stop it too
1. Close *System Informer*
1. Right click on the Start button and click on *Windows Powershell (Admin)*
1. Execute `rd /s /q "C:\Program Files\WindowsApps"`. This will delete all of your UWP apps
1. Launch a new *File Explorer* windows, navigate the *sources* folder in your Windows 10 1809 disc and open *install.esd* in 7-Zip, then navigate to *\1\Program Files*
1. Copy *WindowsApps* from 7-Zip to your desktop
1. If you see a *This destination has files with the same names* box, click on *Replace the files in the destination*
1. Move the folder to *C:\Program Files*
1. Go back to Powershell and execute these commands:
```
del "C:\ProgramData\Microsoft\Windows\AppRepository\StateRepository*"
rd /s /q "C:\ProgramData\Microsoft\Windows\AppRepository\Packages"
add-appxpackage -register "C:\Windows\SystemApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Windows\ImmersiveControlPanel\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
```
If you get an error about *ActivationStore.dat* or *ActivationStore.dat.LOG1*, just ignore it. Running the last command thrice is necessary.
1. Restart your computer
1. Disable Windows Update
1. If you see applications which have weird name in the Start menu or it doesn't work, right click them, go to *More* -> *App settings*, then hit *Reset*
Everything should work, except what requires a newer version of Windows 10, of course!




## Windows 10 1809 to Windows 10 1803, 1709, 1703 or 1607
Credits: [LagLife](https://www.youtube.com/@laglife), [Charles](https://www.youtube.com/@charles25565) \
Note: Only 1607 was tested, but 1703-1803 should be similar enough \
Notice: **THIS WILL DELETE ALL OF YOUR UWP APPS AND RESET YOUR LEGACY EDGE's USER DATA**

### Requirements
- [IDA Free](https://out7.hex-rays.com/files/idafree84_windows.exe) (not included in this repository due to it not being abandonware)
- A Windows 10 1607, 1703, 1709, 1803 disc/ISO. We'll call it the *old Windows 10 disc*
- A machine running Windows 10 1809

### Downgrade process
1. If you had anything stored on OneDrive which you will want to access after the downgrade, download it as OneDrive will break
1. Create a folder on your hard drive, then copy everything from the old Windows 10 disc to it
1. Open IDA as an Administrator and, from your new folder, open *sources\setupcompat.dll*
1. Allow IDA to search to symbols
1. Hit ALT and T simultaneously and search for the function *ConX::Setup::Common:CWindowsVersionIsLaterThan*, then select *Find all occurances*
1. Click on the one with no *Instruction*, scroll to the box right above the bottom one, then pick the label with *mov eax, 1*
1. Click on *Edit*, *Patch Program*, then *Change byte*
1. Change `B8 01` to `B8 00` and hit *OK*
1. Go to *Edit*, *Patch program* and click *Apply patches to input file...*, then click *OK*
1. Disable your internet connection
1. Launch *setup.exe* from your folder you created earlier
1. Let it install
1. When you arrive at the desktop, you may see a few errors. Just disregard those.
1. Open a *Registry Editor* (regedit)
1. Navigate to *HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion* and delete as much as you can inside of the *Notifications* and *PushNotifications* subkeys
1. Open *System Informer*
1. In the *Services* tab, search for *AppXSvc*, right click on it, then hit *Stop*
1. Search for *StateRepository* and stop it too
1. Close *System Informer*
1. Right click on the Start button and click on *Command Prompt (Admin)*
1. Execute `rd /s /q "C:\Program Files\WindowsApps"`. This will delete all of your UWP apps
1. Launch a new *File Explorer* windows, navigate the *sources* folder in your old Windows 10 disc and open *install.esd* in 7-Zip, then navigate to *\1\Program Files*
1. Copy *WindowsApps* from 7-Zip to your desktop
1. If you see a *This destination has files with the same names* box, click on *Replace the files in the destination*
1. Move the folder to *C:\Program Files*
1. Click on the address bar and type *%localappdata%\Packages* and delete the folder whose name starts with *Microsoft.MicrosoftEdge*
1. Navigate to *C:\Program Files\WindowsPowershell\Modules\PSReadLine* and delete the *2.0.0* subfolder
1. Go back to the *Command Prompt* and execute `powershell`
1. Now that you are in Powershell, execute these commands:
```
del "C:\ProgramData\Microsoft\Windows\AppRepository\StateRepository*"
add-appxpackage -register "C:\Windows\SystemApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Windows\ImmersiveControlPanel\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
add-appxpackage -register "C:\Program Files\WindowsApps\*\AppxManifest.xml" -disabledevelopmentmode
```
Running the last command thrice is necessary.
1. Restart Windows
1. You may get a *Recovery* BSOD
1. Boot into the Windows installer from a DVD/USB
1. Press SHIFT and F10 simultaneously
1. Execute `regedit`
1. Click on *HKEY_LOCAL_MACHINE*, go to *File* -> *Load Hive...* and select *C:\WINDOWS\System32\config\SYSTEM*
1. When it asks for a key name, you can use whatever you want. I recommand using *sys*
1. Expand this new key and go into *\ControlSet001\Services* inside of it
1. Delete these keys: *WdBoot*, *WdFilter* and *WdNisDrv*
1. Click on *sys*, then go to *File* -> *Unload hive...*
1. Close the *Registry Editor*
1. In *cmd*, execute `wpeutil reboot`
1. Wait until Windows gets to the desktop
1. If you want to stop getting errors whenever you get to the desktop, you may disable *OneDrive* in the *Task Manager*'s *Startup* tab
Your Windows 10 install should be good to go!