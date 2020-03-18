# Topics

## Ls with GREP
the ls command is actually a list directory of contents, and the grep command is used to search for lines of text that match one or many regular expressions, and outputs only the matching lines. So in this case when you use the grep command in conjunction with ls it will print the contents of the list inside of the directory.

and example command of this would be:
```
Ls(1) -1 | grep(1) <file>
```
## PIPE
a pipe is a form of redirection (transfer of standard output to some other destination) that is used in linux and other Unix like operating systems to send the output of one command/program/process to another command/program/process for further processing.

## Ps AUX
ps: command is used to get detailed information about process running on Linux, Unix and BSD systems
A: The default behaviour of the 'ps' command is listing only current user processes. All other users owned processes will be not shown. 'a' options will print all other user processes too.
U: The default behaviour about showing process information will not print the owner of the process. But in most of cases the process owner data will very helpful. So we can use u option in order to show process owner.
X: 'ps' will show only terminal attached process by default. if we want to show other processes those not attached to the terminal we can use 'x' option.

## What is PID
short for product identification or product id, pid is a unique number that helps identify a hardware product or a registered software product. For example, a computer mouse PID is often found on the bottom.

a pid is a unique number that identifies each running processes in an operating system, such as linux, unix, macOS, and Microsoft Windows.

## start a process in the background using sleep

to start sleep command test it in your vm by typing
```
sleep 10s
```
this should lock the terminal for 10seconds.

now we will run it in the background for longer:

```
sleep 60m &
```

this will put the process into the background and return the PID thanks to the & symbol.

## Searching for the process
now to search we can use two commands

```ps aux | GREP <pid>
```
this will show you all processes that are running with the value of the pid as it will contain the value somewhere within their string.

so therefore using the command
``` jobs
```
can be more effective as it will specifically show processes that are running in the background along with their status eg. running, done etc

## Kill it
now to kill the process we need to use the simple command
``` kill <pid>
```
this will specifically look for the pid and kill any process running under the pid specified.

## capture the output using STDOUT and pip it into a file (write it into a text file)
 to capture the output using STDOUT we can use

 ```ps aux | grep <pid> >> stdout.txt
 ```
this will pipe the output into a text file using stdout and can be accessed for viewing by using
```
cat stdout.text
```
this will display the contents of the text file.
