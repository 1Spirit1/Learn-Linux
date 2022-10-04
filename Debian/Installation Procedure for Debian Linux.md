# How to Easily Install Debian Linux

Installing Debian could be easy or complicated depending upon the ISO you choose.

If you go with the default ISO provided by the Debian website, you’ll have a hard time installing Debian. You’ll be stuck at a screen that asks for network drivers to be installed from external removable media.

![](https://itsfoss.com/wp-content/uploads/2021/08/Debian-firmware.png)

You may, of course, troubleshoot that, but it makes things unnecessarily complicated.

Don’t worry. Let me show the steps for installing Debian comfortably and easily.


## The easy way of installing Debian as a desktop

Before you see the steps, please have a look at the things you need.

- A USB key (pen drive) with at least 4 GB in size.
- A system with an active internet connection (could be the same system where it will be installed).
- A system where you’ll be installing Debian. It will wipe out everything on this system, so please copy your important data to some other external disk.

What kind of system specification you should have for Debian? It depends on the desktop environment you are going to use. For example, the GNOME desktop environment could work on 4 GB RAM but it will work a lot better on 8 GB RAM. If you have 4 GB or less, try using KDE, Cinnamon or Xfce desktops.

Debian also has both 32-bit and 64-bit architecture support. You’ll have to get the Debian ISO according to your processor architecture.

Your system should have at least 25 GB of disk space to function. The more, the merrier.

> _**Warning!** This method removes all the other operating systems along with the data present on the disk. You may save your personal files, documents, pictures etc on an external USB disk or cloud storage if you want to use it later._

In this tutorial, I am going to show the steps for installing Debian 11 Bullseye with GNOME desktop environment. The steps should be the same even if you choose some other desktop environment.

**_This tutorial is tested on a UEFI system with GPT partitioning. If you have MBR instead of GPT or legacy BIOS instead of UEFI, the live USB creation step will be different._**

### Step 1: Getting the correct Debian ISO
Half of the battle in installing Debian is choosing the correct ISO. Surprisingly, it is really difficult to navigate through its website and find that ISO which is the easiest for a new Debian user.

If you click the Download button on the homepage of Debian website, it downloads a minimal net install file which will be super complicated for a regular user. Please DO NOT use this.

Instead, you should go for the live ISO. But here is a catch, there are separate live versions with non-free software (includes drivers for your networking hardware).

You should download this non-free live ISO. Another problem here is that you won’t get it mentioned prominently on the website and there are various URLs for torrents or direct downloads for various architecture.

Let me link them here.

<b><i><a href="https://cdimage.debian.org/images/unofficial/non-free/images-including-firmware/current-live/" class="button">Main repo for 32 and 64 bit</a></i></b>
&nbsp;
&nbsp;
&nbsp;
&nbsp;
<b><i><a href="https://cdimage.debian.org/images/unofficial/non-free/images-including-firmware/current-live/amd64/iso-hybrid/" class="button">Debian 11 Direct</a></i></b>
&nbsp;
&nbsp;
&nbsp;
&nbsp;
<b><i><a href="https://cdimage.debian.org/images/unofficial/non-free/images-including-firmware/current-live/amd64/bt-hybrid/" class="button">Debian 11 Torrent</a></i></b>

You’ll see several files with the of desktop environment mentioned in the filename. Choose the one with desktop environment of your choice. For direct downloads, click on the links that end with .iso.

![](https://itsfoss.com/wp-content/uploads/2021/08/downloading-Debian-live-non-free-iso.png)

Once you have the appropriate ISO downloaded, the rest is standard procedure that you may have experienced with other Linux distributions.

### Step 2: Creating live USB of Debian

Plug in the USB into your system. It will be wise to format it just for the sake of it. It will be formatted anyway.

You can use any live USB creation tool of your choice. If you are using Windows, go with Rufus. I am going to use Etcher here because it is available for both Windows and Linux.

Download Etcher from its website.

[***Download Etcher***](https://www.balena.io/etcher/)

Just run the downloaded executable file, browse to the Debian ISO, make sure that the correct USB is selected and then hit the Flash button.

![](https://itsfoss.com/wp-content/uploads/2021/08/creating-live-debian-usb-with-etcher.png)

It may take a couple of minutes to create the live USB. Once that is ready, it is time to boot from it.

### Step 3: Boot from the live USB

Restart the system where you want to install Debian. When it is showing the manufacturer’s logo, press F2/F10 or F12 key to access the boot settings. You may also access the UEFI firmware settings from Windows.

Some systems do not allow booting from live USB if secure boot is enabled. If that is the case, please disable secure boot from the BIOS settings.

The screen may look different for different manufacturers.

![](https://itsfoss.com/wp-content/uploads/2014/05/Disable_Secure_Boot_Windows8.jpg)

Once you make the change, press F10 to save and exit. Your system will boot once again.

Again, press F2/F10 or F12 to access the boot settings when it shows the manufacturer’s logo. You should see the option to boot from the USB. Select it.

![](https://itsfoss.com/wp-content/uploads/2021/04/boot-from-windows-disk-ventoy.jpg)

It takes a little bit of time and then you should see a screen like this. Go with the first option here.

![Debian live boot screen](https://itsfoss.com/wp-content/uploads/2021/08/debian-live-boot-screen.png)


### Step 4: Start Debian installation

When you enter the live Debian session, it may show some welcome screen with option to choose your keyboard and language if you are using GNOME desktop. Just hit next when you see those screens.

![Debian live welcome screen](https://itsfoss.com/wp-content/uploads/2021/08/debian-live-welcome-screen.png)

Once you are past the welcome screen, press the Windows/Super key to bring the activity area. You should see the Debian install button here.

![Start Debian Installation](https://itsfoss.com/wp-content/uploads/2021/08/start-Debian-installation.webp)

It opens the friendly Calamares graphical installer. Things are pretty straightforward from here.

![Debian 11 Calamers Graphical Installer](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-1.png)

It asks you to select your geographical location and time zone.

![Select your location and time zone](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-2.webp)

On the next screen, you’ll be asked to select the keyboard. Please pay attention here. Your keyboard is automatically selected based on your location. For example, I had used India as my location and it automatically set the default Indian keyboard with Hindi language. I had to change it to English India.

![Choosing keyboard layout](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-4.webp)

The next screen is about the disk partition and where you would like to install Debian. In this case, you are going to install Debian as the only operating system on your computer.

The easiest option would to go with ‘Erase disk’ option. Debian will put everything under root except the mandatory ESP partition and Swap space. In fact, it shows what your disk would like after your chosen installation method.

![Disk Partitioning](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-5.png)

If you want to take matter in your hands, you may also opt for manual partitioning and choose how much you want to allot to root, home, boot or swap. Only do that when you know what you are doing.

On the next screen, you have to provide the username and password. It does not set root password and keeps it empty.

![Set Username and Password](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-6.png)

This also means that you can use sudo with the newly created user. In the ‘complicated Debian install’, you could also set root password but then you’ll have to add the normal user to sudoer list manually. See, this installation method is easier for beginners, right?

Before it goes on with the actual installation, it presents you with a summary of the choices you have made. If things look good, hit the install button.

![Summary of your installation choices](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-7.webp)

Now it is just a matter of waiting for the installation to finish.

![Installing Debian](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-8.png)

It takes a few minutes to complete the installation. When the installation finishes, it asks for a restart.

![Finished Debian Installation](https://itsfoss.com/wp-content/uploads/2021/08/Installing-Debian-9.png)

Restart your system and if everything goes well, you should see the grub screen with Debian.

![Debian boot screen](https://itsfoss.com/wp-content/uploads/2021/08/debian-boot-screen.webp)

## Were you able to install Debian?
I hope I made things simpler here. It is not that you cannot install Debian from the default net installer ISO. It just takes (a lot) more effort.

Was this tutorial helpful for you in installing Debian? Are you still facing issues? Please let me know by raising an issue and I’ll try to help you out.
