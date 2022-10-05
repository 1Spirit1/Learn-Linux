# Installing VSCode on manjaro 💻

### 1. Installing VS Code in Manjaro Linux using AUR helper

Yay is an acronym for “Yet Another Yogurt”. It is written in the Go programming language. 
Being an AUR helper, yay permits you to automate the installation of packages from PKGBUILDS. 
If you want to install VS Code in Manjaro Linux by utilizing “yay”, then you only have to use the following command in the terminal:

```
yay -S visual-studio-code-bin
```

&nbsp;

### 2. Installing VS Code in Manjaro Linux using pacman

Visual Studio Code has installer for debian (.deb) and rpm (.rpm) based Linux distributions. 
Officially, no such installer is available for Arch Linux. 
You can download a .tar.gz file from the official website of Visual Studio Code at https://code.visualstudio.com/ and use it on any Linux distribution though. 
But it won’t integrate well with the system.
Gladly, Visual Studio Code is available in the Arch User Repository (AUR).

First update the pacman package repository cache with the following command:
```
sudo pacman -Sy
```

Now you have to install Git version control system. It is required to install packages from AUR and also for Visual Studio Code.
Run the following command to install Git:
Press y and then press Enter to continue.
```
sudo pacman -S git
```

Now navigate to the Downloads directory with the following command:
```
cd ~/Downloads
```

Now clone the Visual Studio Code’s AUR repository with the following command:
```
git clone https://AUR.archlinux.org/visual-studio-code-bin.git
```

Now navigate to the visual-studio-code-bin/ directory with the following command:
```
cd visual-studio-code-bin/
```

Now run the following command to make a pacman package of Visual Studio Code:
```
makepkg -s
```

Now run the following command to install the generated pacman package with pacman package manager:
```
sudo pacman -U visual-studio-code-bin-*.pkg.tar.xz
```

### 3. You can also download it using GUI in Add/Remove software.














  
