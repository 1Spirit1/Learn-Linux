# How to Set Environment Variables in Linux

Bash shell is used for various purposes under Linux. How do I customize the shell environment variable under Linux operating systems? How can I set and view environment variable on Linux?

You can use shell variables to store data, set configuration options and customize the shell environment under Linux. The default shell is Bash under Linux and can be used for the following purposes:
## Follow the steps listed below:-

1.To set an environment variable the export command is used. We give the variable a name, which is what is used to access it in shell scripts and configurations and then a value to hold whatever data is needed in the variable.

"export NAME=VALUE"


2.For example, to set the environment variable for the home directory of a manual OpenJDK 11 installation, we would use something similar to the following.

"export JAVA_HOME=/opt/openjdk11"


3.To output the value of the environment variable from the shell, we use the echo command and prepend the variable’s name with a dollar ($) sign.

"echo $JAVA_HOME"


And so long as the variable has a value it will be echoed out. If no value is set then an empty line will be displayed instead.
