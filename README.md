### Simple Shell Project

A simple UNIX command interpreter which is part of the low-level0programming and algorithm track at ALX Holberton School.

## Description
Shellby command language interpreter was use to read and execute commands either by file or standard input.

#Invocation 
To compile all .c files in the respositroy and run the result.
gcc *.c -o shellby
./shellby


Shellby is both iteractively and non-interactively invoke. The command interpreter invokewith standard input not connected to a terminal, it reads and executes received commands in order.
If shellby is invoked with standard input connected to a terminal, an interactive shell is opened. When executing interactively, shellby displays the prompt when it is ready to read a command.


##Environment
Shellby recieves and copies the environment of the parent process in which it was executed. This environment is an array of name-value strings describing variables in the format NAME = VALUE. A few key envronment variables are:
Home
Pwd
Oldpwd
Path

#Command Execution

After receiving a command, shellby tokenizes it into words using "" as  as delimite. The first word is considered the command and all remaing words are considered argument to command. Shellby then proceeds with the following actions:
- I the first characer of the command is neiter a slash (\) nor dot (.), the shell searches for it in the list of shell bultins. If there exists a builtin by that name, the builtin is invoked.
- If the first character of the command is none of a slash (\) bir dit (.), the shell searches for it in the list of shell builtins. If there exists a builtin by that name, the builtins is invoked.
-If the character of the command is noe of a slash (\), dot(.), nor builyin, shellby searches each element of the PATH environmental variables for a directory containing an executable file by that name.
- If the first character of the command is a slash (\) or dot (.) or either of the above searches was succesful, the shell executes the named program with any remaining given arguments in a separate execution environment.
