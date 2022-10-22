10 Things To Do After You Have Installed Ubuntu 21.10
=====================================================


Switching to Ubuntu from Windows should go as smoothly as possible. Here are the most important things to do after installing Ubuntu.


Switching to Ubuntu from Windows might be a big step, but it's one that you want to go as smoothly as possible. Just as you might configure Windows and the desktop theme, install the latest updates, and make tweaks to get things running to your preference, so Ubuntu can be updated and setup to aid your productivity.

Once you have your computer running Ubuntu, this is what you need to do post Ubuntu installation.

1\. Check for and Install Ubuntu Package Updates
------------------------------------------------

For the best performance on your new Ubuntu PC and to avoid any potential stability and security issues with older applications, you should run an update immediately.

Two options are available:

-   Use Software Updater
-   Update and upgrade from the command line

To use the Software Updater:

1.  Open the app drawer
2.  Click **Software Updater**
3.  **Wait as it **checks for updates
4.  When it's done, click **Install Updates**
5.  **Input your password if requested**

**Updates in the terminal are quicker:**

1.  In the app drawer, open a Terminal window (or press **CTRL+SHIFT+T**)
2.  Enter **sudo apt-get update**
3.  Wait while the repository information is updated
4.  Next, enter **sudo apt-get upgrade**
5.  When prompted, press **Y** to confirm the update

Once everything is updated, you'll be ready to start enjoying Ubuntu.

If you ever need to check what is installed, the easiest way is to list the installed packages in Ubuntu

```
sudo apt list --installed
```

This will display a list of everything installed on your computer.

2\. Set Up Ubuntu Livepatch
---------------------------

Another thing to do after installing Ubuntu is to enable its built-in patching tool, Livepatch. This is an updater that keeps your computer secure.

To enable Ubuntu Livepatch:

1.  Open **Software & Updates**
2.  Go to the **Livepatch** tab
3.  Click **Sign in**
4.  Sign in to your Ubuntu One account
5.  Input your Ubuntu system password when prompted

Livepatch is then enabled on your system.

3\. Install and Run the Snap Store
----------------------------------

Screenshot by author

In the latest versions of Ubuntu, Snap is pre-installed. In fact, some of Ubuntu's pre-installed applications are in fact Snap packages.

But you cannot install the Snap Store. Instead, it is incorporated into GNOME Software. So, all you need to do to find the Snap package you're looking for is to launch GNOME Software and search for it.

You can check which applications are available as Snaps through GNOME Software by reading the notes for that app. If it is a Snap, it will be listed as such.

4\. Choose a Browser for Ubuntu
-------------------------------

Mozilla Firefox is the default browser for Ubuntu. What if you wanted to use Google Chrome instead?

You have two options here. The first is to install Chromium, the browser that Google Chrome is based on. This can be installed from GNOME Software or from the command line with:

```
sudo apt install chromium-browser
```

Chromium is functionally identical to Google Chrome in most scenarios.

### How to Install Chrome on Ubuntu

If you specifically want to install Google Chrome in Ubuntu, go to [www.google.com/chrome](http://www.google.com/chrome) and click **Download Chrome**. You will see the option to select **64-bit .deb (For Debian/Ubuntu)** so choose this and **Accept and Install **to proceed.

This will commence the download of the DEB file. Once this completes, launch the DEB file to commence installation in Ubuntu Software. Click **Install **and a few moments later, Google Chrome will be installed on Ubuntu.

5\. Install Nvidia Drivers on Ubuntu
------------------------------------


Another important thing to do after installing Ubuntu is to ensure your graphics drivers are installed.

With Intel Graphics and AMD GPUs, the graphics drivers are installed automatically. However, Nvidia drivers must be installed manually. So, if your computer or laptop has Nvidia graphics, you'll need to install suitable drivers to get the most out of the Nvidia GPU.

Our tutorial to [installing Nvidia drivers on Ubuntu](https://www.makeuseof.com/install-nvidia-drivers-ubuntu/) will guide you through the full process.

6\. Enjoy Video and Music: Install VLC Player on Ubuntu
-------------------------------------------------------

Ubuntu has its own media players pre-installed. Videos, surprisingly, plays videos, while Rhythmbox handles music, podcasts, and streamed internet radio.

If you prefer a tool that does all the above plus adds all the media codecs you need for complete video and audio playback, VLC media player is the answer.

Enter the following to install VLC player:

```
sudo apt install vlc
```

You can also install VLC as a Snap using GNOME Software.

7\. Customize Ubuntu: Install GNOME Tweaks
------------------------------------------

While Ubuntu's GNOME desktop looks good, it can be customized further using the GNOME Tweaks tool. This adds various useful features, such as a configurable desktop dock, battery percentage indicator for laptops, desktop icons, and much more.

To install, open a terminal and in the command line enter:

```
sudo apt install gnome-tweaks
```

You'll find GNOME Tweaks in the app drawer. GNOME Tweaks can be used on any Linux OS using the GNOME desktop. For example, you can [use GNOME Tweaks on Pop!_OS](https://www.makeuseof.com/customize-pop_os-21-04-with-gnome-tweaks/).

8\. Set Up Dropbox or Another Cloud Syncing Service
---------------------------------------------------

Various cloud syncing services are compatible with Ubuntu. First and third-party client software for local syncing with Dropbox, Nextcloud, and others.

You can install Dropbox easily:

1.  Open GNOME Software
2.  Search for "dropbox*"*
3.  Click **Install**

Once installed, simply sign in to the client and manage your sync settings.

9\. Install Microsoft Core Fonts and Other Restricted Extras on Ubuntu
----------------------------------------------------------------------

Microsoft True Type fonts and other software can be installed with Ubuntu Restricted Extras. The contents of this package are legally restricted in some countries, hence the name.

However, it contains Microsoft's Core True Type Fonts, along with some media codecs. As the installer states:

> These fonts were provided by Microsoft "in the interest of cross-platform compatibility". This is no longer the case, but they are still available from third parties.
>
> You are free to download these fonts and use them for your own use, but you may not redistribute them in modified form, including changes to the file name or packaging format.

To install Microsoft Core Fonts, open a terminal and enter:

```
sudo apt install ubuntu-restricted-extras
```

You'll need to agree to the EULA to proceed with the download.

Screenshot by author

A few moments later, the fonts and other restricted extras will be available to use.

Screenshot by author

10\. Run Ubuntu Backups
-----------------------

With your Ubuntu system configured how you want it, now is a good time to use the Ubuntu backup tool.

Launch this by hitting the Super button on your keyboard and typing "backups."

This is a relatively simple tool to use. To create a backup:

1.  Click **Folders to save**
2.  Click **+**
3.  Browse and select the folder or folders (hold **CTRL** and **left-click **for multiple choices) you wish to back up
4.  Click **Add**
5.  Click **Storage location **and choose a destination for the backup---external devices can be used
6.  Select **Scheduling** if you wish to create a regular backup
7.  Otherwise, click **Overview** then **Back Up Now**

A completed backup can be restored from the backup location using **Overview > Restore**.

## Now You Know What to Do After Installing Ubuntu
As with any operating system, there are things to do before you start using your computer again. For example, a Windows user will often need to run an update, select an operating system, upgrade any outdated drivers, and grab a decent media player (again, probably VLC Player).

The same is true for almost every other operating system, including Ubuntu.

So to recap, after you have installed Ubuntu, you should:

Check and install any Ubuntu package updates
Set up Ubuntu Livepatch
Install the Ubuntu Snap Store
If you don’t like Firefox, install Chrome on Ubuntu
Install graphics drivers if you use an Nvidia GPU
Install VLC on Ubuntu
Install GNOME Tweaks
Configure cloud account syncing
Install Microsoft Core Fonts on Ubuntu
Learn how to use and run Ubuntu Backup

With all these tasks completed, you’re now ready to start using Ubuntu. Get started by installing your favorite software.
