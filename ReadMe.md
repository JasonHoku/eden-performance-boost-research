
Lag Fix Guide for High/Medium End PCs on EdenServer

Ensure your game client is closed before proceeding with steps 1-4.


========================================
Step 1 Installing DGVOODOO 
=============================================

Extract DGVOODOO from this github post to PlayOnline/SquareEnix/PlayOnlineViwer. (some older/other install methods may lead to needing the DGVOODOO files in another location... Either besides pol.exe , polboot.exe or the bootloader. (EdenXI.exe)

Launch dgVoodooCpl.exe as Administrator once for it to create a config file.

========================================
Step 2 Installing D3Dcompiler 
=============================================

Do not overwrite the dll (skip this step) if d3dcompiler_47.dll already exists on your primary disk in either Windows/System32/ or Windows/SysWOW64/.

If you do not have d3dcompiler_47.dll :

1.)Copy or cut d3dcompiler_47. (from this github post)

If you are running a Windows 32 bit operating system, paste it in Windows/System32/

If you are running a Windows 64 bit operating system, paste it in Windows/SysWOW64/


2.)Confirm it is being applied to FFXI:
 
Launch FFXI and check if the dgVoodoo watermark is in the bottom right, if so it is installed correctly.

========================================
Step 3 Setting up dgvoodoo 
=============================================
Steps1&2 required.

1.)Open dgVoodooCpl.exe as Admin (for the final time) again and turn off the watermarks on Glide, and Directx tabs.
Update the Vram on the Directx tab to above 64mb. 1024mb if your machine will allow it. ( See next step for pushing past 1gb)
Anisotropic and Antialiasing (MSAA) can be configured higher.
Save the config in the /SquareEnix/PlayOnlineViewer/ folder.

2.)Pushing past 1GB VRAM allotment requires editing and saving one text file. (close game and dgvoodoo first)

Open dgVoodoo.conf with notepad or any text editor (Install Directories require run as admin to save)

In your text editor scroll down to the DirectX section and find:

=============================================
[DirectX]

;  VideoCard: "svga", "internal3D", "geforce_ti_4800", "ati_radeon_8500",
;             "matrox_parhelia-512", "geforce_fx_5700_ultra"
;       VRAM: in MBs
;  Filtering: "appdriven", "pointsampled", "bilinear", "linearmip", "trilinear"
;             or the integer value of an anisotropic filtering level (1-16)

DisableAndPassThru                  = false

VideoCard                           = internal3D
VRAM                                = 1024

=============================================

That last line there is what you want to edit to push your VRAM past what the old .exe offers. Make it into this for 4GB:

VRAM                                = 4096


========================================
Step 4 Correcting Z-Indexing & Reducing DirectX glow: 
=============================================

Remember to backup your files before overwriting vital game data.


Copy the ROM and ROM5 folders to your ffxi install and merge them with overwrite into \PlayOnline\SquareEnix\FINAL FANTASY XI


========================================
Step 5 Correcting Low Priority Native FFXI Resting 
=============================================

Additionally Task Manager --> Details --> EdenXI.exe (Right Click) --> Set Priority --> High should clear up lag as well.
This setting will revert after the game is closed each time but there are softwares you can use to make them permanent, I recommend TechCenter's Project Mercury (works while running as admin and use reccomended settings):

https://techcenterdk.wordpress.com/2017/10/08/project-mercury-v1-2-9-0-beta/ (download link on right of page)





Optional Final Bonus Instructions:

1.)Log into FFXI and be AMAZED (like I was) LAG IS FINALLY GONE

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
