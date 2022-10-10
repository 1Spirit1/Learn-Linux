# Installation of Linux Mint
Linux Mint is a modern, polished, easy-to-use, and comfortable community-driven GNU/Linux desktop distribution based on the popular Ubuntu Linux distribution. It is a great and recommended distribution for computer users switching from Windows or Mac OS X operating system to the Linux platform.

Linux Mint 21 code-named “Vanessa” is the latest version of the popular Linux Mint desktop operating system that is available in three versions, namely Cinnamon, Xfce, and MATE. It is an LTS (Long Term Support) release that is built atop Ubuntu 22.04 and will be supported until 2027.

*Before you proceed, ensure that you have a 4 GB USB drive for the installation medium and a stable broadband internet connection to download the ISO image.*

## Step 1: Download Linux Mint 21 ISO Images

First of all, you need to download the ISO image from the links below:

Download Linux Mint 21 – [Cinnamon Edition](https://linuxmint.com/edition.php?id=299)
Download Linux Mint 21 – [Mate Edition](https://linuxmint.com/edition.php?id=300)
Download Linux Mint 21 – [XFCE Edition](https://linuxmint.com/edition.php?id=301)


Once you downloaded the preferred desktop edition, make sure to verify the ISO image by generating the SHS256 sum as shown:
<pre>
$ sha256sum -b linuxmint-21-cinnamon-64bit.iso  [for Cinnamon]
$ sha256sum -b linuxmint-21-mate-64bit.iso      [for Mate]
$ sha256sum -b linuxmint-21-xfce-64bit.iso      [for XFCE]

</pre>

![Verify-Linux-Mint-ISO](https://user-images.githubusercontent.com/93483932/194723116-825fbc17-ad02-4d87-8bde-0df9636a4df5.png)

<br>

![Verify-Linux-Mint-ISO-Image](https://user-images.githubusercontent.com/93483932/194723134-db2e4b94-4a29-4dfb-9355-53bcea69f12a.png)

Next, you need to create a bootable media-USB flash/DVD using the Rufus utility or these useful USB creator tools in order to create a Linux Mint bootable USB drive.

## Step 2: Installation of Linux Mint 21 Cinnamon Edition

Now plug in the bootable USB flash drive into your computer and reboot. Once the system has rebooted, press your BIOS key for selecting the boot device and select the USB drive to boot from it. Once the system has booted, from the grub menu, select the first option and click enter to load Linux Mint

![Linux-Mint-21-Boot-Menu](https://user-images.githubusercontent.com/93483932/194723200-3224f950-73ce-4004-bbf0-b3e6784194d9.png)

From the desktop, click Install Linux Mint to launch the installation wizard as highlighted in the following screenshot.

![Install-Linux-Mint-21](https://user-images.githubusercontent.com/93483932/194723218-40a949e8-ad1b-4708-82e2-b4f5e53f9b06.jpg)

After the installation wizard opens up, you can optionally read the release note, then click Continue.

![Choose-Linux-Mint-Language](https://user-images.githubusercontent.com/93483932/194723229-1429ddaf-2115-46c2-96bc-97d1f908736f.png)

Next, select the keyboard layout and click Continue.

![Choose-Linux-Mint-Keyboard](https://user-images.githubusercontent.com/93483932/194723247-29571fa5-5c71-4698-9875-25c347a49d3e.png)

In the next windows, check the option Install Multimedia codes (which are required to play certain video formats and more), and click Continue.

![Install-Multimedia-Codecs-1](https://user-images.githubusercontent.com/93483932/194723260-e112bdf5-819d-4d05-ac21-65ac1dbabbb8.png)

Now pick the installation type by selecting the second option, Something else to enable you to manage partitions for installing Linux Mint.

***Note: If you already have existing partitions where you wish to install Linux Mint, for example, a partition with an existing installation of another Linux Mint version installation or Linux distribution, simply ignore the partition creation steps, simply select the root, and swap partitions and set the properties.***

 ![Choose-Linux-Mint-Install-Type](https://user-images.githubusercontent.com/93483932/194723300-ca7786cc-a493-47b5-a64b-7699ad84ace4.png)

 Next, in the partition setup window, click New Partition Table.

 ![Choose-New-Partition-Table](https://user-images.githubusercontent.com/93483932/194723311-8085ce0c-7bed-41e1-95d5-196b5d8d2861.png)

 And confirm the new partition table creation step by clicking Continue in the pop-up window.


![Confirm-New-Partition-Table](https://user-images.githubusercontent.com/93483932/194723321-087a109c-72ab-4deb-9303-d848de54d383.png)

Next, you need to create the EFI system partition, a mandatory partition for UEFI systems. It will hold the EFI bootloaders and drivers to be launched by the UEFI firmware. Select the free space, and click the add (+) button to create a new partition.

![Create-New-Partition](https://user-images.githubusercontent.com/93483932/194723329-9c94f19f-fd80-4d6f-83f9-8136690c7f7a.png)

And set the EFI partition properties:

Size – you can set a size between 100 to 550 MB, and
Use as – set to EFI System Partition and click OK.

![Create-EFI-Partition](https://user-images.githubusercontent.com/93483932/194723342-44cd89bd-c70f-4379-883c-c895e92c6acf.png)


Next, create the root partition which will store the system files. Select the free space again, and click the add (+) button to create a new partition with the following properties:

Size – minimum size should be 20 GB but recommended is 100 or more GB
Use as – file system type you wish the partition to use e.g EXT4, and
Mount point – should be / (for root partition) and click OK.

![Create-Root-Partition-1](https://user-images.githubusercontent.com/93483932/194723355-67842f49-b6d1-4ca3-8031-965851ecd34f.png)


Next, create the swap space by selecting the free space and clicking on the plus (+) sign to create a new partition with the following properties:

Size – you can set a size of 500 MB or more if you have more free space, and
Use as – set value to swap area.

![Create-Swap-Partition-1](https://user-images.githubusercontent.com/93483932/194723361-f4ffdfee-2a03-4349-81dd-9ac049a12f38.png)

Create Swap Partition
Finally, create a “Reserved BIOS Boot area” partition of at least 1 MB, which will store the boot loader code.

 
![Create-Reserved-BIOS-Boot-Partition](https://user-images.githubusercontent.com/93483932/194723377-bc7ed65a-aa97-49b5-949d-1bb4a69d4c26.png)

After creating all your partitions as shown in the following screenshot, click Install Now.

![Linux-Mint-Partition-Summary](https://user-images.githubusercontent.com/93483932/194723388-461698a0-f8cd-4cd8-8d60-e907e41e315d.png)

In the pop-up window, click Continue to accept the new partition table setup.

![Confirm-New-Partition-Table-1](https://user-images.githubusercontent.com/93483932/194723410-99843613-354e-4cc9-9712-334074ac5331.png)


Now select your location and click **Continue.

**

![Choose-Linux-Mint-Timezone](https://user-images.githubusercontent.com/93483932/194723438-3f98e2f7-8b0b-457f-91fa-3e359a7ae9d2.png)

Next, create a user account with a password and set the computer name as shown in the following screenshot. Then click Continue to start the actual installation of system files and packages to the root partition.

![Create-Linux-Mint-User](https://user-images.githubusercontent.com/93483932/194723451-2e8dbd93-9746-4259-b32e-2384fc38beb0.png)

Wait for the installation of the system files and packages to complete. Once all is done, click on *** Restart Now ***

![Linux-Mint-Installation-Completes](https://user-images.githubusercontent.com/93483932/194723462-09bb072e-00a8-4bac-8c9e-1084546e5ede.png)

Once the system has rebooted, log into your new *** Linux Mint 21 Cinnamon edition installation.***

![Linux-Mint-Login](https://user-images.githubusercontent.com/93483932/194723516-20dd1cf2-f824-484f-b271-ee1ed0b43326.jpg)

![Linux-Mint-21-Desktop](https://user-images.githubusercontent.com/93483932/194723517-8d16fa45-5adc-4795-abef-9733e6b95d06.png)


***Congratulations!*** You have just successfully installed Linux Mint 21 Cinnamon edition on your computer. 
