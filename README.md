[Grub2] Ettery theme
===========

![Ettery preview](EtteryPreview.png?raw=true "Preview of theme")
[![AUR package](https://repology.org/badge/version-for-repo/aur/grub2-theme-ettery.svg)](https://aur.archlinux.org/packages/grub2-theme-ettery/)

Ettery is Grub2 theme. This theme is based on
	
 - ZorinOS grub2 theme (code)
 - [Vimix by vinceliuice](http://vinceliuice.deviantart.com/art/Grub-themes-vimix-0-1-532580485) (icons)

Designed primary for 1920x1080 resolution, but should work for common resolutions as well. (not tested)

For further customization use [grub-customizer](https://launchpad.net/grub-customizer) to add/remove/change/rearrange entry and etc... 

-------------------------

Quick install guide
----------------------

> **Note:**
> There is ***install.sh*** script from original ZorinOS theme that automates install process, but it is not tested with this theme, therefore I recommend manual installation.

> **Note:**
> If you use Arch Linux or a Arch based distribution you can also install this theme from the [AUR](https://aur.archlinux.org/packages/grub2-theme-ettery/).
>
>  AUR package is created and maintained by @Lukas1818.

#### Preparation
Find out supported resolution by your grub. 

 * Reboot to grub
 * Open command line by pressing "C"
 * Enter `vbeinfo`
 * Check for maximum supported resolution. (eg. 1920x1080)

#### Installation

 - Copy entire **Ettery** folder to **/boot/grub/themes/**
		`sudo cp -r Ettery /boot/grub/themes/`

> **Note:**
> Depending of your distribution it location might be **/boot/grub2/themes/** or **/grub/themes/**

 - Open **/etc/default/grub** in text editor with root
		`sudo gedit /etc/default/grub`
 - Add/change following lines 
	```
	GRUB_GFXMODE="1920x1080" #replace with your supported resolution
	GRUB_GFXPAYLOAD_LINUX="keep"
	GRUB_THEME="/boot/grub/themes/Ettery/theme.txt"
	```
		
 - Save changes in text editor
 - Update grub
    `sudo update-grub`
    
    > **Note:**
    > Depending of your distribution, you might use **update-grub2** or **grub2-mkconfig -o /boot/grub/grub.cfg** , but usualy all 3 commands are the same.


#### Disabling theme
Just remove/comment (put # at beginning) following line in **/etc/default/grub** file:

    GRUB_THEME="/boot/grub/themes/Ettery/theme.txt"
Update grub to take effect:  `sudo update-grub`

#### Uninstalling theme
Disable theme and delete **Ettery** folder from **/boot/grub/themes**
		

    sudo rm -r /boot/grub/themes/Ettery

-------------------------

Known issues and bugs
----------------------------
>**[Version 1.0]**
>
>- [FIXED] Text align issue. Text moves when switching between selections.

Please report if you find more bugs.

---------------------------
Current version: 1.1

2015
