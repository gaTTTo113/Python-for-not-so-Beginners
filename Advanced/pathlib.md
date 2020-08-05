# pathlib

Earlier Python had library `os.path` - the way to interact with file-system, but more officiant might be using `pathlib` module, which provides objective oriented  approach, using `Path` object.
The  `pathlib`  module was introduced in Python 3.4 [PEP 428](https://www.python.org/dev/peps/pep-0428/) and nowadays it's officially part of standard library.

## Creating Paths
To begin with `pathlib` you need to import it.
```
import pathlib
```
But I recommend to use `from` keyword to make code more readable, using `Path` directly:
```
from pathlib import Path
```
There are a few different ways of creating a `Path` object:

- `.cwd()` current working directory.
- `.home()` user's home directory.
- and also by providing path as a string.

`pathlib` will automatically handle all differences between operating systems, so don't worry about that, but be careful with **\\** symbol on Windows, just use `raw string literals` to represent Windows paths.

```
from pathlib import Path

my_current_directory = Path.cwd()
my_home_directory = Path.home()
my_custom_path = Path(r'C:\Users\some_user\some_folder')
```

Another way to construct a path is to join the parts of the path using the special operator  `/`.
The `/` operator is used independently of the actual path separator on the platform.
You can do the same thing with the  `.joinpath()`  method:

```
my_path = Path.home() / 'some_folder' / 'my_script.py'
my_second_path = Path.home().joinpath('some_another_folder')
```

Paths can also be specified as simple file names, the  `.resolve()`  method will find the full path.
```
my_path = Path('test.py')
print(path.resolve())
```
> /home/user/some_folder/test.py

## Reading and Writing Files

`open()`  function can use  `Path`  objects directly, but an equivalent alternative is to call  `.open()`  on the  `Path`  object:
```
my_path = Path.cwd() / 'my_text.txt'
with open(my_path, mode='r') as my_text_file:
    # some code here

with my_path.open(mode='r') as my_text_file:
	# some code here
```
For simple reading and writing of files, use this methods of `Path`:

-   `.read_text()`: return contents as a string.
-   `.read_bytes()`: return contents as a bytestring.
-   `.write_text()`: open the path and write string data to it.
-   `.write_bytes()`: open the path in binary/bytes mode and write data to it.

Each of these methods handles the opening and closing of the file.
```
my_path = pathlib.Path.cwd() / 'my_text_file.txt'
my_text = my_path.read_text()
print(my_text)
```
> Contents of my_text_file here!
 
## Moving and Deleting Files

Through  `pathlib`, you also have access to basic file system level operations like moving, updating, and even deleting files.
To move a file, use  `.replace()`. Note that if the destination already exists,  `.replace()`  **will overwrite it**. Unfortunately,  `pathlib`  **does not explicitly support safe moving of files**. To avoid possibly overwriting the destination path, the simplest is to test whether the destination exists before replacing:
```
if not destination.exists():
    source.replace(destination)
```
Directories and files can be deleted using  `.rmdir()`  and  `.unlink()`.

-------

[Here](https://pathlib.readthedocs.io/en/pep428/) you can find more of `pathlib` useful features! Good luck!
