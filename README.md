# Turn-old-Macbook-Pro-into-a-contemporary-notebook

This writing is done, because I forget the details, when doing a project and next time I have to re-invent all again.
And maybe it is of some kind of help to anyone who, like me wants that old Macbook Pro run those new applications. 
I started buying a Macbook Pro long time ago (2014) and used it untill short time ago (and now it is donated and keeps running as before). 
2-3 years ago I read about tools to make the newest MacOS run on old Macbooks and by now I did installations on about 5-6 different Macbooks, from 2012 to 2015. 
I get a bit better in it, and maybe one day I will be an expert ;-) 

# Introduction
This "HowTo" help will not be a chronilogical version of my findings (that would be a very long story, and hard to understand). So I cut it down in a couple of stages, what can be done with some "ease:

## Step 1: Get yourself a Macbook Pro
Almost any model can be used to run the latest MacOs versions. To use a Macbook as a standalone Windows machine, it needs an Intel processor. 
These can be found in Macbook Pro's up till about 2018. The younger the notebook the more expensive. So I would search for a notebook from 2013 or later (2012 or older is also possible, but not so fast etcetera). 
If you can choose: i7 is better then i5; more memory is better then less (best is 16 GB i7 but for "non-gaming" applications 4Gb i5 is nice). 
SSD-disks can be changed later. Some ideas on my 3 notebooks:
- 2013 i5 dual Core 8 gB as Windows10 (only) replacement for a "toooo slooooow" Acer from 2017.
- 2015 i5 8 gb, my experimental machine: MacOs Sequoia; Windows10, Linux Mint and some space left for fast and dirty OS installations. 
- 2015 i7 16 gB, my serious work machine, only MacOs Seqouia. (the less used of the 3 ;-) ) 
When buying:
- check the display. When there is bluryy, stripy, whatever stuff on the screen. That is hard to repair. Can only be done by screen replacement and these are rare to find and expensive to buy.
- It should boot, not needed that it boots to the SSD itself, but if there is a question mark on the screen, then you get it probably running. 
- check for waterdamage, gives stupid errors and almost not to repair (easily). 
- prices? Can differe very much per season, country, model. For my 3 machines the average was about € 150,- (including some small stuff like a rubber, screws, HDMI dummy plug)

## Step 2: Clean the machine
- Unpack what you bought, just some hot water + dishwashingsoap is good enought to wipe it off (do not make it wet!). Also use this soap to clean the display. Most of the time there is al lot of dirt, grease and what ever on it. 
- Lay it upside down and open it. You need some specific tools, just search on internet.
- Unscrew the 10 screens around the bottom. Take care to put the two at the ventilation opening (near the display) aside, these are smaller and must go back there.
- When opened, first unplug the battery.
- Then check what you got, and clean when needed. I sometimes use a vacuumcleaner on lowest power, with the big brush on it, and carefully go around. Do not vacuum clean the rubbers etc. they might just fly in.
  But most of the time, just a simple painting brush is enough to get some dirt out.
- The less you do in there, the better. It is easy to break something and hard to repair.
- Close it again. Do not forget to put the batteryconnector back before closing.

## Step 3: The installing plan. 
Make a plan for the installation. You need it, because before installing some USB-sticks have to be prepared, depending on what how you want the endresult. Best is to think in layers to be placed on top or besides eachother. You want MacOs in a new version? Or just Windows? Or Linux? Or combination of all of them? Make a plan.
###  Preparing what you need for your plan
#### 1 
Because you run modern systems on an old machine, always there is an "in between old en new" needed. There are more options, but the best I could find is Open Core Legacy Patcher (OCLP). https://dortania.github.io/OpenCore-Legacy-Patcher/
Read on the website, and dowload the application. It is all MacOs, so you will need an MacOs computer for next steps with OCLP. (I will come back to that). 
#### 2
If you want to install Windows you will need an installer for that. To create that, the most easy is to do that with a Windows computer. To create the installer we will use Rufus. Go here https://rufus.ie/ to read about it and download the version you need onto the Windows computer. 
#### 3
For MacOs decide on what you want, OCLP will help with the downloading, so this can be done later. 
#### 4 
For Linux, no explanation here. There are many versions, wich all have there own manuals. 
#### 5
To run Windows on a Macbook the software Bootcamp is needed. This has to be downloaded (not easy to find, see later), and should be unzipped and placed on an USB.
#### 6
When installing the operation systems, there are moments that the drivers for wifi, keyboard or touchpad are not installed, so you cannot use them. So have a USB keybord and USB mouse (not wireless) ready, to be plugged in when needed. 

### Installing
Oh wait. What if you do not have a MacOs computer and also no Windows, how to get OCLP and other stuff on your machine and USB?
It will you a couple of hours extra, but can be done with the Macbook you just bought :-) You will needed Wifi
### Install step 0: Recover your macbook
Starting from scratch: 
- Start up your macbook in Recovery mode.
  Hold Down Command (⌘) + R: As soon as your MacBook begins to restart (you'll hear the startup chime or see the Apple logo), press and hold the Command (⌘) and R keys simultaneously. Continue holding them until the Apple logo or a spinning globe are visible.
- Choose Recovery with Internet. Connect to your Wifi.
The machine will now download the MacOS version it was build for (so very old). When started choose to restore the OS and all installation. Just let it do what it wants. If it cannot write to the disk (because there is old stuff on it), just wipe all off, untill you have a complete free SSD.
- It will take some time, but at some moment it will restart and you have a running Macbook with the original MacOs on it. Connect it to Wifi. 
No need to update the MacOS. It will be used only short time. 
NB: If no Windows computer available, it might be usefull to install windows on the Macbook, using Bootcamp. It is a Mac application what is capable of adding a windows partition + installation. Takes a lot of time, but worked fine, when I needed it. You can then login to Windows for using rufus + creating Windows Installer. See further. 

### Install step 0.1: Install OCLP
Download OCLP latest version, Install, and Create an Installer, just follow the instructions. Choose the MacOS you want (I would always try the latest one (now Seqouia). It will take time, because it is 15 Gb download, unpack, prepare, and then upload to the USB. But then you have an Installer, and the real work can start. 
### Install step 1. Install MacOs + OCLP 
NB: If the Installer was made with an other Mac computer, you can start the installing process here. 
Think about how to divide the SDD in partitions. When you want more then 1 OS (windows + MacOs ? linux) you need to know how big the partitions need to be. 
- Just put the USB in, restart, hold down Alt/Option untill you can choose. Choose the EFI-boot (This makes the USB boot with OCLP working!). Otherwise it will say you cannot install this OS. 
- Then you can choose the MacOs Installer. Just follow all steps. 
- When you come to choosing the disk, wipe the disk, and create a partition for Mac as big as you want it. 
- Force the installer to use that partition.
- Run the whole process. With restarts. Leave the USB in.
- When the install process is almost ready you will end up on the desktop of the new OS. Wait a bit an then the OCLP installer will come up (if it does not, use Finder to go to the USB. There you will find OCLP. Double click.
NB If the keyboard an touchpad do not work. No problem, just insert USB Keyboard and USB Mouse!
Let OCLP do its job. Install to disk, Install to EFI (be sure to choose the SDD here!).
Reboot (Pull USB out first), Hold down the Alt/OPtion. Choose EFI first, then MacOS. 
Connect to Wifi, start the OCLP again. And choose Post Install Root Patch. OCLP might say it is already done. Just install the patches again. My experience is that it downloads more then first time and the install is more complete. (to be sure I might do this more often after a new reboot).
Do all updates on MacOs. 

When you only want MacOs, you are OK now, when you only want Windows or a combination: READ ON. 

### Install step 2. Install MacOs + Windows 
OK, for Windows you need an installer. And latest Windows10 (or even 11) will install like that on an Intel Macbook. This is where rufus comes in. 
Rufus will download a recent Windows10 or 11 ISO; add a couple of bypass, tricks etcetera, to make the installer work. Just follow the manual. Almost impossible to do anything wrong :-) And if so, just start over. 
OK. when you got your Windows Install USB 

#### Add Bootcamp software. 
Windows needs a couple of drivers etcetera to run on a Macbook. Apple provides these Bootcamp files when you run Bootcamp installation from within MacOs. You will need an extra USB (third one!) to place those files on. Sometimes these Bootcamp files are to old, and you have to download a newer version (and these are hard to find on internet). See links page. 

##### A Install Windows + MacOS. 
Same as in step 0. Start Bootcamp from MacOS, set the size of the harddisk you want for Windows and go. 
Now the Bootcamp files are created (on USB 3). 
When done shutdown; insert the Windows Rufus installer, boot the machine; hold down Option/Alt. Choose EFI boot and then Windows installer. 
Do diskmanagement and check if the partition for windows is removed and/or formatted in correct version. 
When Windows is almost finished: DO NOT REBOOT (if you do, you might have to start over with the Windows Installer). 
Attach the keyboard + mouse. Insert USB3 and run Setup in the Bootcamp folder. 
When Setup is finished: DO NOT REBOOT. 
By now you are able to use Wifi. Do all updates in windows. Also go to Optional Updates and select all. These are mostly the Intel driver files for your Windows system. 
Also run Apple Update, this will download lateste Bootcamp files. This will probably give errors when running updates. No problem, this will be solved later. 
Now REBOOT. Pull USB's out. 
Hold down Option/Alt when rebooting, choose EFI boot, then Windows. 
All updates will take a lot of time. But and the end you are in Windows. 
Run Apple Update again. Now the updates will probably run wihtout errors. 
Run Windows updates. Keep updating untill all is done. 

##### B Install ONLY Windows  
Almost the same as A. The start is different. 
Because you installed OCLP with MacOS, you now have a nice OpenCore buffer between the old Macbook and the new Windows. 
We will use that:
Insert the Windows installer, hold Option/Alt first choose EFI boot, then the Windows installer. 
Go to diskmanager: Be carefull to keep the EFI partition 200 mB at the beginning and delete all other partitions. 
Install Windows on the free space. 
Pick up instructions at A for the rest. 
Last reboot use Option/Alt -> EFI boot -> Windows. 
Next time the machine will go in these two steps to Windows by itself. 

Congratulations: You have a Macbook installed with latest systems you wanted. 


Specials:
- Displays from 2014 not working in 2015 (have magnet ready)
- Use Labor for special stuff (Windows 11)
- Disable  Bootpicker
- WIndows LOT for long time 
- Where to find Bootcamp files?
- 
