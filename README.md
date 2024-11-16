# My_.vimrc 

# General Overview

This repository contains my custom config for Vim such as essential vim settings and vim plugs.

## Installation

1. Rename your current **.vimrc** to **.vimrc.backup** to backup it up if you don't like mine :(
	- 		$ mv ~/.vimrc ~/.vimrc.backup

2. Then download my **.vimrc** and place it in **$HOME**
	- Download the .vimrc
	- Place it **~/.vimrc**

3. Next, create 3 folders in the ~/.vim directory (backup, undo, swap)
	- 		mkdir -p ~/.vim/backup ~/.vim/undo ~/.vim/swap

4. Install fzf in your OS:
	- Debian side:
 		- 		$ sudo apt install fzf
	- Fedora side:
 		- 		$ sudo dnf install fzf
	- Arch side
 		- 		$ sudo pacman -S fzf
	- SUSE side
		- 		$ sudo zypper install fzf
	- MACOS
 		- 		% brew install fzf

5. Next, you need to set up vim-plug (used for plugin management) for the fzf plugin
```bash 
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
   https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

6. After installing vim-plug and the above steps, open vim or Gvim
	- 		$ vim

7. Open the command line in vim and then type
	- 		:PlugInstall

- Installation Complete!!

--------------------------------------------------------------------------------------------------

## Uninstallation

1. Rename your current .vimrc.backup to .vimrc to restore your previous .vimrc 
    - 		$ mv ~/.vimrc.backup ~/.vimrc

2. Remove the backup, undo and swap directory .vim
    - 		$ rm -rf ~/.vim/backup ~/.vim/undo ~/.vim/swap

3. Remove vim-plug (if you don't need it)
    - 		$ rm -rf ~/.vim/autoload ~/.vim/plugged

4. Install fzf in your OS:                                                                          
    - Debian side
   	- 		$ sudo apt remove --purge fzf                                                          
    - Fedora side
    	- 		$ sudo dnf remove fzf                                                          
    - Arch side
    	- 		$ sudo pacman -Rns fzf                                                    
    - SUSE side
    	- 		$ sudo zypper remove fzf                                                       
    - MACOS
    	- 		% brew uninstall fzf

- Uninstallation Complete!!

--------------------------------------------------------------------------------------------------

## Vim-Plug Operations

#### Should have open vim ($ vim)

1. To Install:
    - 		:PlugInstall 	## Installs everything you added in your .vimrc

2. To Update:
    1. 		:PlugUpdate <plugin_name>	## Specific Package(s)

    2. 		:PlugUpdate (Update everything)	## All Packages

3. To Remove:
    - Comment or remove the line for the plugin (in .vimrc):
        - Example: "Plug 'junegunn/fzf'"
            - Using " in the begining of the line (and also end of line but this is unneccessary)

    - Open vim and type
        - 		:PlugClean	## Removes every package you commented or removed from your .vimrc

--------------------------------------------------------------------------------------------------

Thanks for trying out my .vimrc and hope you have a great rest of the day or night :))
