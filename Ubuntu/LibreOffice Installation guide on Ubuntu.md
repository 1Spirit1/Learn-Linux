# What is LibreOffice?
![Libre office icon](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRpOfAYLfQBqPxIyz2BAeANwPrykaLLXXUjFRkcT4wNbM9DrKcShhQi5Vh_kh-Bkyep0w&usqp=CAU)

LibreOffice is a **free and open source** office suite which is the default office suite for most popular linux distros.

It is a project of The Document Foundation (TDF).
The LibreOffice suite consists of programs for word processing, creating and editing spreadsheets, slideshows, diagrams, and drawings, working with 
databases, and composing mathematical formulae. It is available in 115 languages.
As its native file format to save documents for all of its applications, LibreOffice uses the Open Document Format for Office Applications (ODF), or OpenDocument.
LibreOffice also supports the file formats of most other major office suites, including Microsoft Office, through various import and export filters.

LibreOffice is available for various computing platforms, including Microsoft Windows, macOS, Linux, Android, iOS, and Chromebook. It is also available as an
online office suite called LibreOffice Online.

## 🟢 Features of LibreOffice 
The feature of LibreOffice is continuously being updated and is a work in progress. Below are some essential elements of LibreOffice:

#### 1. Included Application: It includes the following basic components, such as:

- **Writer 🖊️:** A word processor with similar functionality and file support to Microsoft Word or WordPerfect. It has extensive
word processing capabilities but can also be used as a basic text editor. 


- **Calc 📄:** A spreadsheet program, similar to Microsoft Excel. It has several unique features, including a system that automatically 
defines graphs based on the user's information.


- **Impress 🎚️:** A presentation program resembling Microsoft PowerPoint. Presentations can be exported as SWF files, allowing them to be viewed on 
any computer with Adobe Flash Player installed.


- **Draw 🖌️:** A vector graphics editor and diagramming tool similar to Microsoft Visio and CorelDRAW. It provides connectors between shapes,
which are available in a range of line styles, and facilitates building drawings such as flowcharts. It can also act as a PDF file editor.
<br/>

# LibreOffice installation Guide on Ubuntu

You can install LibreOffice easily along with other third party drivers while installing Ubuntu on your system, just by checking the third party install 
checkbox.

![](https://phoenixnap.com/kb/wp-content/uploads/2021/04/choose-starting-applications-for-ubuntu-20.04.png)

or you can install it using the terminal
**NOTE ;** Installing LibreOffice on Ubuntu through the offical website is not recommended, as it doesn't integrates automatic updates.

**Full installation**

Performing a full installation is the recommended way to install LibreOffice in Ubuntu. One would do this by installing the LibreOffice metapackage via a terminal:

```bash
sudo apt install libreoffice
```

**Selective installation**

While this isn't recommended, one may install a subset of the full installation. An example package set:

    libreoffice-writer: Word processor
    libreoffice-calc: Spreadsheet
    libreoffice-impress: Presentation
    libreoffice-draw: Drawing
    libreoffice-base: Database
    libreoffice-math: Equation editor 

Installing other related packages (dictionaries, extensions, clipart, templates, etc.)

Additional language modules, help files and extensions are also available if you search for “libreoffice” in your package manager. Example how to search:

```bash
apt-cache search libreoffice-help-en
```

To install proper support for language writing aids you may install the corresponding packages libreoffice-l10n-*, myspell-*, hyphen-*, mythes-*, libreoffice-help-* followed by your language ISO 639-1 code. A complete list of such language codes is available here.

For example, the corresponding French packages are:

    libreoffice-l10n-fr
    myspell-fr
    hyphen-fr
    mythes-fr
    libreoffice-help-fr 

Please be advised that not all languages have these corresponding packages. For more information on language support in LibreOffice please check here.

Installing a newer version of LibreOffice than available via Ubuntu repositories

If you want to get a later version of LibreOffice then provided by the Ubuntu repositories, and you have tested this appropriately for your environment, you may do so via one of the PPAs provided by the LibreOffice Packaging team. For example, one may add the LibreOffice PPA repository:

```bash
sudo apt install python-software-properties

sudo apt-add-repository ppa:libreoffice/ppa

sudo apt update
```
<br/>

**Show some love and support to the community for this amazing initiative ! ❤️**

[![Twitter icon](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/libreoffice) 
[![Twitter icon](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/libreoffice/)
[![Twitter icon](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCQAClQkZEm2rkWvU5bvCAXQ)
[![Twitter icon](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/libreoffice.org)
[![Twitter icon](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/LibreOffice)


<hr/>

