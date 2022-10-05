# Pacman 👨‍🔧

Manjaro's package manager, Pamac ships with most Manjaro editions. 
All Manjaro editions include pacman, the package manager from upstream Arch Linux. 
Pacman includes some advanced features not found in Pamac.

Key points to know:

- Pacman is already installed in Manjaro Linux by default
- Pacman is mainly developed/maintained by Arch Linux developers
- Pacman can only be used from the command line, if you would prefer a graphical package manager please see Pamac or Octopi
- Pacman can only use the official Manjaro repository. There are separate articles available for accessing the Arch User Repository(AUR), using flatpaks and using snaps

&nbsp;

## Installing Updates

To update the package database and update all packages on the system
```
sudo pacman -Syu
```
To force a full refresh of the package database and update all packages on the system. You must do this when switching branches or switching mirrors.
```
sudo pacman -Syyu
```

## Searching for Packages

To install a software package, the basic syntax is pacman -S packagename. 
However, installing a package without updating the system will lead to a partial upgrade situation so all the examples here will use pacman -Syu packagename which will install the package and ensure the system is up to date. 
For example, to install smplayer the command is:
```
sudo pacman -Syu smplayer
```

Pacman can also directly install packages from the local system or a location on the internet. The format of that command is pacman -U packagelocation. 
For example, to install a copy of your package cache you could do something like:
```
sudo pacman -U /var/cache/pacman/pkg/smplayer-19.5.0-1-x86_64.pkg.tar.xz
```

## Removing Packages

To remove a software package, the basic syntax is sudo pacman -R packagename. We could remove the smplayer package we installed above with:
```
sudo pacman -R smplayer
```
This will remove the package, but will leave all the dependencies behind. 
If you also want to remove the unneeded dependencies you could use pacman -Rsu packagename as seen in this example:
```
sudo pacman -Rsu smplayer
```















