

# How to Write Bash Scripts in Linux

# What is a Bash Script?

A bash script is a series of commands written in a file. These are read and executed by the bash program. The program executes line by line.


# How Do You Identify a Bash Script?

File extension of .sh. By naming conventions, bash scripts end with a .sh. However, bash scripts can run perfectly fine without the sh extension.

# Scripts start with a bash bang

Scripts are also identified with a shebang. Shebang is a combination of bash # and bang !  followed the the bash shell path. 

Example of SheBang -- "#! /bin/bash"

# How to Create Your First Bash Script

1) Firstly Create a file named hello_world.sh

    touch hello_world.sh

2) Find the path to your bash shell.

    which bash

3) Write the command

    We will use echo command to see our desired output on console

    Script will look somethig like this :

        #! usr/bin/bash
        echo "Hello World"

4)  Edit the file hello_world.sh using a text editor and add above lines .

5)  Provide Execution rights.

    Modify the permissions and allow execution of thr script by using the command as shown below:

        chmod u+x hello_world.sh

    chmod modifies the existing rights of a file for a particular user. We are adding +x to user u.

6) Now Run he Script

    You can run the script in the following ways :

        ./hello_world.sh
        bash hello_world.sh

7) At last you will able to see "Hello World " on rhe console.


  Congratulations you have successfully run your first Bash Scripit.
  <img src="https://user-images.githubusercontent.com/87846440/194099424-6bcf8bbe-cf07-433c-a6d1-3bb2622937f3.png" height="50"> 




