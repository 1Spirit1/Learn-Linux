# Must know commands of Linux.
## All the basic commands follow below:-

1. pwd â€” When you first open the terminal, you are in the  home directory of your user. To know which directory you are in, you can use the â€œpwdâ€ command. It gives us the absolute path, which means the path that starts from the root. The root is the base of the Linux file system. It is denoted by a forward slash( / ). The user directory is usually something like "/home/username".


2. ls â€” Use the "ls" command to know what files are in the directory you are in. You can see all the hidden files by using the command â€œls -aâ€.

3. cd â€” Use the "cd" command to go to a directory. For example, if you are in the home folder, and you want to go to the downloads folder, then you can type in â€œcd Downloadsâ€. Remember, this command is case sensitive, and you have to type in the name of the folder exactly as it is. But there is a problem with these commands. Imagine you have a folder named â€œRaspberry Piâ€. In this case, when you type in â€œcd Raspberry Piâ€, the shell will take the second argument of the command as a different one, so you will get an error saying that the directory does not exist. Here, you can use a backward slash. That is, you can use â€œcd Raspberry\ Piâ€ in this case. Spaces are denoted like this: If you just type â€œcdâ€ and press enter, it takes you to the home directory. To go back from a folder to the folder before that, you can type â€œcd ..â€ . The two dots represent back.

4. mkdir & rmdir â€” Use the mkdir command when you need to create a folder or a directory. For example, if you want to make a directory called â€œDIYâ€, then you can type â€œmkdir DIYâ€. Remember, as told before, if you want to create a directory named â€œDIY Hackingâ€, then you can type â€œmkdir DIY\ Hackingâ€. Use rmdir to delete a directory. But rmdir can only be used to delete an empty directory. To delete a directory containing files, use rm.

5.  rm - Use the rm command to delete files and directories.  Use "rm -r" to delete just the directory. It deletes both the folder and the files it contains when using only the rm command.

6.  touch â€” The touch command is used to create a file. It can be anything, from an empty txt file to an empty zip file. For example, â€œtouch new.txtâ€.

7. man & --help â€” To know more about a command and how to use it, use the man command. It shows the manual pages of the command. For example, â€œman cdâ€ shows the manual pages of the cd command. Typing in the command name and the argument helps it show which ways the command can be used (e.g., cd â€“help).

8. cp â€” Use the cp command to copy files through the command line. It takes two arguments: The first is the location of the file to be copied, the second is where to copy.

9. mv â€” Use the mv command to move files through the command line. We can also use the mv command to rename a file. For example, if we want to rename the file â€œtextâ€ to â€œnewâ€, we can use â€œmv text newâ€. It takes the two arguments, just like the cp command.

10. locate â€” The locate command is used to locate a file in a Linux system, just like the search command in Windows. This command is useful when you don't know where a file is saved or the actual name of the file. Using the -i argument with the command helps to ignore the case (it doesn't matter if it is uppercase or lowercase). So, if you want a file that has the word â€œhelloâ€, it gives the list of all the files in your Linux system containing the word "hello" when you type in â€œlocate -i helloâ€. If you remember two words, you can separate them using an asterisk (*). For example, to locate a file containing the words "hello" and "this", you can use the command â€œlocate -i *hello*thisâ€.