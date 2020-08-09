
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

The underlying process creation and management in this module is handled by the `Popen` class. It offers a lot of flexibility so that developers are able to handle the less common cases not covered by the convenience functions.

Execute a child program in a new process. On POSIX, the class uses `os.execvp()`-like behavior to execute the child program. On Windows, the class uses the Windows  `CreateProcess()`  function. The arguments to  `Popen` are as follows.

An example of passing some arguments to an external program as a sequence is:
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
