# Command Line Interface
Many tasks can be performed using graphical user interface which is provided by the fedora. However command line interface provides more details and handy to use, so most developers prefer to use the CUI. The command line is also called a shell prompt, because the commands are processed by a program called a shell; the standard shell on a Fedora system is the Bourne-again shell (bash).


# How to access the terminal in Fedora
Terminal can is easily opened through shortcut key, ctrl-alt-f2 or select the menu option Applications→Accessories→Terminal (System→Terminal in KDE), or right-click on the desktop background and select Konsole under KDE.

## Commands
* Left Arrow -----> move left one character
* Right Arrow ---> move right one charcter 
* Backspace -----> delete one character on left
* Delete -----------> Delete the character under/to the right of the cursor
* Esc, DAlt-D -----> Delete to the end of the current word
* Esc, BackspaceAlt-Backspace ---> Delete to the start of the current word
* HomeCtrl-A ---> Go to the start of the line
* EndCtrl-E ---> Go to the end of the line

## How to access the previous commands

You can easily access the previous entered comands using the up and down arrow key. This will help the user to not type the commands again and again.

You can also search for a previous command by pressing Ctrl-R (for reverse search) and then typing a few characters that appear in the command.


## Obtaining a root prompt to enter commands as the superuser

The superuser account, root, is also called the privileged account, because it is not subject to the security restrictions that are applied to regular user accounts. root access is required for many system administration commands. Although it’s tempting to use the root account all the time on a single-user computer, it is unwise because Fedora assumes that you know what you’re doing and won’t ask for confirmation if you enter a dangerous command; it will just go ahead and execute it. If you’re using the root account, an incorrect command can cause a lot more damage than the same command executed in a normal account.



Although you can directly log in as a root user, it’s usually much safer to take on root privilege only when necessary, using the su (switch user) command:

```
$ su
Password: {root-password}
```
The shell prompt will change to end in a pound sign (#) instead of a dollar sign ($) when you are in root mode. Press Ctrl-D or type exit to drop superuser access and return to your regular shell prompt.

## Logging out of a shell prompt

You can leave a shell by pressing Ctrl-D or typing exit. If you are using a terminal window and don’t have any programs running, you can simply close the window using the X button on the title bar.

# Linux terminal accepts three type of arguments

## Options

These start with a hyphen or double-hyphen ( - or --) and modify the way the command operates.For example, the ls (list-files) command will include hidden files in its output if the -a argument is given, and will list detailed information about files when the -l option is specified. These options may be used individually, used together in any order, or combined after one hyphen if they all use a single hyphen:

```
$ ls -l
$ ls -a
$ ls -l -a
$ ls -a -l
$ ls -al
$ ls -la
```

## Positonal Arguments

These have significance according to the order in which they are specified. For example, the cp (copy) command accepts two or more filenames:

```
$ cp                  
one two                     
```
## Options with a value

These combine options with positional arguments. An option with a value may be placed before or after other arguments, but the value must be placed directly after the option.

```
$ ls -a -l -w 60
$ ls -w 60 -al
$ ls -l -w 60 -a
$ ls -l -w60  -a
$ ls -alw60
```


# The End

All of the commands which runs in other linux distributions also works here. So, don't worry I haven't inserted many of the commands as there is enough linux basic commands in other repos which you may refer.


