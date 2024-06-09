---
 layout: post
 title: DAY FIVE AT COREDGE
 date: 2024-6-8
---
**2024-6-8- AS A LINUX ADMIN**

On day 5 it was a great feelings as always i have covered some topics like shell scripting
i have covered lots of things about scripting. lets talk about
what is exactly shell scripting is....


**What is a Shell?**

A shell is essentially a program that provides a way for users to interact with the operating system 
by executing commands. It serves as an intermediary between the user and the system kernel. The shell 
interprets user inputs (commands) and translates them into actions performed by the system.


**What is Shell Scripting?**

A shell script is a text file containing a series of commands that are executed by the shell, which is
the command-line interface of the operating system. In Linux, common shells include Bash (Bourne Again Shell),
Zsh (Z Shell), and others. Shell scripts can be used to perform a wide range of tasks, from simple file 
operations to complex system management.

**Why Use Shell Scripting?**

Automation: Automate repetitive tasks to save time and reduce the risk of human error.

Efficiency: Execute multiple commands in a sequence without manual intervention.

Customization: Create tailored solutions to specific problems or workflows.

Portability: Write scripts that can be run on various Unix-like systems with minimal modifications.

**Basic Components of a Shell Script**

Shebang (#!/bin/bash): Specifies the interpreter for the script.

Comments: Lines beginning with # are comments and are ignored by the shell.

Variables: Store data that can be used and manipulated within the script.

Control Structures: Include conditionals (if, case) and loops (for, while, until).

Functions: Modularize code for reuse and better organization.

**Basic bash scripting**

#!/bin/bash

echo "hi hazique how are you " > ~/output.txt
echo "" >> ~/output.txt
echo "#############################" >> ~/output.txt

lsblk >> ~/output.txt
df -h >> ~/output.txt

**Used some variable**

**variables:**

#!/bin/bash

### using Variable

age=23
name="hazique"
id=777

echo "my name is $name and age is $age and my id no is $id"

### var to store output of command ###

HOSTNAME=$(hostname)
echo "Name of this machine $HOSTNAME"

**constant var**

#!/bin/bash

####constant  variable
readonly College=$"JMI"
readonly name=$"khan"


echo "what is your college name $College"
echo "what is your name $name" 

**Arrays-var**
#!/bin/bash

### Arryas variables ###

haikarray=( 1 2 "khan" 30.5 "hello" )

echo "${haikarray[*]}"

echo "${haikarray[3]}"

echo "${haikarray[0]}"

##########################

####### How to find no. of value from array var #############

echo "${#haikarray[*]}"

### find  specific value from array ###

echo "${haikarray[*]:0:4}"

### Add more value in var ####

haikarray+=( new 111 core )
echo "${haikarray[*]}"

**Example of String**

#!/bin/bash

mystring="hi hazique how are you"

mystringlength=${#mystring}
echo "length of the string is $mystringlength"

#### To replace a string ###
newvar=${mystring/hazique/sameer}

echo "$newvar"

