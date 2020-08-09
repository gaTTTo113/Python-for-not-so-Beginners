
# Subprocess 
`subprocess` module let you communicate from your script to the shell and get output from it.

first import the module:
```
import subprocess
```
 And now you can use all of the power of `subprocess` module :)
 For beginning let's create something basic:
 ```
 subprocess.call('ls', shell=True)
 ```
 > Desktop \
 > Documents \
 > user \
 > Downloads \
 > 0
 
 by using `call` method you can execute a command and see output in your terminal.
 To catch output use `check_output`:
 ```
 output = subprocess.check_output('ls', shell=True)
 print(output)
 ```
 > b' Desktop\nDocuments\nuser\nDownloads\n'

### Popen Constructor

To execute a child program in a new process use `Popen` class.
Passing some arguments to an external program as a sequence:
```
Popen(["ls", "-la"])
```
Some useful case to use `Popen` with `stderr` and `stdout` catching:
```
process = subprocess.Popen(  
    ['sshpass', '-p', password, 'ls'],  
	 stdout=subprocess.PIPE,  
	 stderr=subprocess.STDOUT  
    )  
stdout, stderr = process.communicate()
```
You can find more [here](https://docs.python.org/3/library/subprocess.html)
