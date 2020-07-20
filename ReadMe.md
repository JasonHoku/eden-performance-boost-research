

Lag Improvements on EdenServer
===

**Ensure your game client is closed before proceeding with steps 1-4.**



## Step 1 Installing dgvoodoo 


Extract/copy the contents of DGVOODOO from this github post to \PlayOnline\Ashita\ffxi-bootmod for Ashita or C:\Program Files (x86)\PlayOnline\SquareEnix\PlayOnlineViewer for Windower. 

Launch dgVoodooCpl.exe as Administrator once and to create a config file, click the add button at the top of the app and select EdenXI.exe. Apply & Close.


## Step 2 Installing D3Dcompiler (Only if dgvoodoo doesn't work)

Extract/copy the contents of DGVOODOO/contents/ to:

If you are running a Windows 64 bit operating system, paste it in Windows/SysWOW64/

2.)Confirm it is being applied to FFXI:
 
Launch FFXI and check if the dgVoodoo watermark is in the bottom right, if so it is installed correctly.


## Step 3 Setting up dgvoodoo 

Steps1&2 required.

1.)Open dgVoodooCpl.exe as Admin (for the final time) again and turn off the watermarks on Glide, and Directx tabs.
Update the Vram on the Directx tab *See Note.
Ex. settings:
https://i.imgur.com/bqWMypt.png

* Note :

For the VRAM setting, this will be dependent upon your graphics card VRAM amount. Higher is not necessarily better if your graphics card memory isn't high enough. You can look up your graphics card VRAM amount or test around with this setting. I reccomend 20-40% of total VRAM if you are dual boxing.





## Step 4 Correcting Z-Indexing & Reducing DirectX glow: 

Remember to backup your files before overwriting vital game data.


Copy the ROM and ROM5 folders to your ffxi install and merge them with overwrite into \PlayOnline\SquareEnix\FINAL FANTASY XI



## Step 5 Correcting Low Priority Native FFXI Resting 


Additionally Task Manager --> Details --> EdenXI.exe (Right Click) --> Set Priority --> High should clear up lag as well.
This setting will revert after the game is closed each time but there are softwares you can use to make them permanent, I recommend TechCenter's Project Mercury (works while running as admin and use reccomended settings):

https://techcenterdk.wordpress.com/2017/10/08/project-mercury-v1-2-9-0-beta/ (download link on right of page)





Optional Final Bonus Instructions:

1.)Log into FFXI and be AMAZED (like I was)

2.)???????

3.)Profit.



Yours Truly,

Lumi


===================

Sources of info:

===================

DGVOODOO:
http://dege.freeweb.hu/

FFXI dgvoodoo Install Guide:
https://balanceffxi.fandom.com/wiki/DgVoodoo2_%26_Reshade_Setup

CPU Priority Issues & ROM Patch Lag Fix:
https://www.ffxiah.com/forum/topic/37945/ffxi-lag-and-you/

ROM Files Lag Fix Patch (I converted the EXE to files for you):
GaiaRorshack's No lag Patch v1.1
https://docs.google.com/file/d/0B6va8E7NdnpWdkRZRzcwQkE2cUE/edit?usp=sharing
