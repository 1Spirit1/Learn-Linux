# How to Install and Remove Software in Manjaro Linux

There are many people who would like to use Linux instead of Windows but are deterred because they believe in [Linux Myths](https://itsfoss.com/myths-about-linux/ "Linux Myths") such as it is difficult to use. This tutorial will try to overcome that error by showing how easy it is to install and remove software on Linux.

You probably already know by now that [I love Manjaro Linux](https://itsfoss.com/why-use-manjaro-linux/ "I love Manjaro Linux"), so in this article, I will be focusing on [Manjaro](https://manjaro.org/ "Manjaro"). There is a similar article on [Managing software in ubuntu](https://itsfoss.com/remove-install-software-ubuntu/ "Managing software in Ubuntu") that Ubuntu users can follow.

Since Manjaro is based on [Arch Linux](https://archlinux.org/ "Arch Linux"), most of this tutorial can also be used for Arch Linux and its derivatives. The methods will be listed from easiest to more advanced.

## Using the Pamac graphical software manager tool from Manjaro
## Using pacman GUI front-end Octopi
## Using pacman commands
## Using yay AUR helper to install software from Arch User Repository


I am also adding several tricks to make things easier.

For this tutorial, I will be using Manjaro 20 with [Gnome](https://www.gnome.org/ "Gnome") and [lxqt](https://lxqt-project.org/ "LXQT") desktop environments. This tutorial should also work with other desktop environments.

## Method 1: Install and Remove Software in Manjaro Linux with Pamac

Install Remove Software Manjaro

Here, we’ll be using Pamac to install/remove software in Manjaro Linux.

### Install Software in Manjaro Linux with Pamac

[Pacmac](https://wiki.manjaro.org/index.php?title=Pacman_Overview "Pacman") is the package manager created by the Arch team and used by Manjaro. This is probably the easiest way to install the software. We will cover it in depth later on. Right now, we focus on Pamac.

[Pamac](https://github.com/manjaro/pamac "Pamac") is a graphical application created to make Pacman easy to use. Like synaptic for apt.

You can either access Pamac by selecting “Add/Remove Software” from the menu or by right clicking the icon in the system tray as shown below.

Pamac allows you to view software already installed, search for new software by name or by category. If you don’t find something you search for, you can also look for it in the Arch User Repository (AUR)[Arc User Repository](https://aur.archlinux.org/ "Arch User Repository").

Your application will not be installed until you click “Apply”. You will be prompted to enter your password and after showing you a list of files it will download it will go to work.

It’s optional to click the “right arrow” next to the “Apply” button to see the terminal output.

### Enabling AUR and Snap/Flatpak support in Pamac
Enabling the AUR and Snap or Flatpak support takes a couple of extra steps in Pamac. Click the 3 dotted menu in the upper right corner and select “Preferences”. You will be prompted to enter your password.

Now, select the “AUR” tab. Now flip the switch (toggle it on). Now, you will be able to install software from the AUR and keep them up-to-date.

Similarly, you can just head to the Snap and Flatpak options to “Enable Snap support” and “Enable Flatpak support” if you need.

### Remove Software in Manjaro Linux with Pamac
Removing software using Pamac is as easy as installing it. All you have to do just click on the “remove” button on the right side of the screen. Once you selected all the packages you want to remove, click on “apply” button.

## Method 2: Install and Remove Software in Manjaro Linux with [Octopi.](https://tintaescura.com/projects/octopi/ "Octopi")

[Octopi](https://tintaescura.com/projects/octopi/ "Octopi") is a Qt-based Pacman front end used in KDE and LXQt. Just like Pamac, it can install applications from the Manjaro repositories or the AUR.

Let’s take a look at how to use it.

Install Software in Manjaro Linux with Octopi

In order to find an application to install, you can either search for it by name or search for it by a group. You can see a description of each application, as well as, what files are included. Octopi also offers distro new and usage instructions.

Once you find the application you are looking for, right click the name from the list and click “Install”. If you select several applications to install, they will be listed under the “Transactions” tab. When you are ready to install, click the check mark icon on the left or press CTRL + M to commit changes.

You will then be prompted to approve the installation process. You can also choose to see the output in the terminal. After you enter your password, your application will be installed.

In order to search for an application in the AUR using Octopi, click on the little green alien to the left of the search box. Once you right click on an application title and select “Install”, you will be taken to the terminal where the install will begin.

You will be asked if you want to edit PKGBUILD. Select “no” for this query and “yes” for the rest. Unfortunately, this means you will only be able to install one application at a time from the AUR.

Please note that Octopi does not allow you to install applications from Manjaro repositories and AUR at the same time.

### Remove Software in Manjaro Linux with Octopi

Uninstalling applications with Octopi is just as easy as Pamac.

Search for the application, right-click the title from the list, right-click and select “Remove“. Once you click the “Apply” button in toolbar, it will be removed.

## Method 3: Install and Remove Software in Manjaro Linux with Pacman command

Graphical applications are easy to use, but terminal or command line programs are more powerful and faster.

### Install Software in Manjaro Linux with pacman

As I stated above, Pacman is the command line package manager for Arch based distros. To install an application, all you have to do is enter sudo pacman ```-S PACKAGENAME```. Just replace PACKAGENAME with the name of the application that you want to install.

You will be prompted to enter your password. Once you enter it, your application will be downloaded and installed.

You can also install a group of packages such a GNOME using this command:

```sudo pacman -S gnome```

It’s that easy!

### Remove Software in Manjaro Linux with pacman

Removing software with Pacman is just as easy. All you have to do is enter the following command:

```sudo pacman -R PACKAGENAME```

Just replace PACKAGENAME with the name of the package you want to remove.

### Tips to Improve Pacman Experience

Since it’s a terminal application, Pacman can run pretty quickly, Unfortunately, the process can be slowed down by a bad mirror.

You can use this command to rank mirrors by speed and remove out of date mirrors:

```pacman-mirrors -g```

When that is finished you will need to sync the Pacman database with this command:

```sudo pacman -Syy```
You may learn more about [Using pacman command for package management in Arch-based distributions](https://itsfoss.com/pacman-command/ "gg") in our detailed guide.

## Method 4: Install and Remove Software in Manjaro Linux with yay

While you can’t install an application from the AUR using Pacman, there are a number of terminal programs that allow you to do just that. One of the most well-known examples is yay.

### Install Software in Manjaro Linux with yay

You can install packages from both official repository and AUR. You first need to install yay on your machine. To do this, type in the commands below:

```git clone https://aur.archlinux.org/yay.git```

```cd yay```

```makepkg -si```

One nice thing about yay is that it gives you the ability to search for the application you want to install, all you have to do is use this command:

```yay -S PACKAGENAME```

Don’t forget to replace PACKAGENAME with the name of the application you are looking for.

You will be prompted to enter “y” to continue. You will be prompted to enter your password and asked a couple more questions verifying that you want to install this application.

Depending on how large the file is and how much work “yay” has to do to prepare the file, the install may be finished quickly or take a while to complete.

### Remove Software in Manjaro Linux with yay
To remove an AUR application with yay, just use the following command:

```yay -R PACKAGENAME```

## This is a beginnners guide on How to install packages in Manjaro.
