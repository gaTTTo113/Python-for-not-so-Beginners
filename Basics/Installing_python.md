# Installing Python 
###  Windows:

  

On Windows you have a choice between *32-bit* and *64-bit* versions, you don't need the *64-bit* version even if you have *64-bit* Windows, the *32-bit* Python will work just fine, so just select latest release and click “*download*” button [here](https://www.python.org/downloads/windows/).

  

Run the installer and follow instructions, but be careful: **You want to be sure to check the box “Add Python 3.x to PATH”** to ensure that the interpreter will be placed in your execution path.

  

If your version of Windows include a feature called the Windows Subsystem for Linux, which allows you to run a Linux environment directly in Windows, you can install Python 3 from a Bash console window, just as you would if you were running that Linux distribution [see below](#linux).

  
### macOS:  

The best way to install Python 3 on macOS is through the Homebrew package manager.

Open a browser and navigate to [brew.sh](http://brew.sh/) , select the Homebrew bootstrap code under “Install Homebrew”, then copy it to the clipboard, paste the Homebrew bootstrap code to Terminal.app window, and hit Enter. Once Homebrew has finished installing, **run the following command**:  

`brew install python3`

You can make sure everything went correctly by typing `pip3` to terminal.

### Linux:

Most of Linux distributions have Python 3 already installed, to check that type `python3 --version` in terminal, if not succeed try `python --version`, if it is not Python 2, you can skip this part of tutorial.

  

- Ubuntu:

`sudo apt-get update`
`sudo apt-get install python3`

if not succeed try:

`sudo add-apt-repository ppa:deadsnakes/ppa`

and than again:

`sudo apt-get update`
`sudo apt-get install python3`

  

- CentOS:

`sudo yum install -y https://repo.ius.io/ius-release-el7.rpm`
`sudo yum update`
`sudo yum install -y python36u python36u-libs python36u-devel python36u-pip`

## Installing IDE
You can write Python code using a shell. However, if you want to work on larger projects, it's much easier to use a dedicated code editor or an integrated development environment (IDE).

It's always difficult to place an IDE or code editor on the podium of "Best IDE of all time", so I just give you some options available for all operating systems:

- [**PyCharm**](https://www.jetbrains.com/pycharm/)
- [**Sublime Text**](http://www.sublimetext.com/)
- [**Vim**](https://www.vim.org/)
- [**Atom**](https://atom.io/)
- [**IDLE**](https://docs.python.org/3/library/idle.html)


