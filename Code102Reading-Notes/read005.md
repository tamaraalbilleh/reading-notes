# Choosing a Text Editor
- When learning how to code you need to find a text editor that you can use and enjoy using.
- different text editors come with a wide verity of features but almost all are pretty similar at heart.
## What is a text editor?
 a text editor is a software that you download on your computer, or access online, that allows you to write and manage text, especially the text that you write to build a web site.
- It is one of the most important tools you can use as an aspiring web developer.
What features should you look for in a text editor?
1. code completion (display possible suggestions and closing tags and brackets).
1. syntax highlighting (makes the text you type more noticeable by colorizing it)
1.  a nice variety of themes
1. the ability to choose from a healthy selection of extensions available.
1. Every computer will come with its own text editor and for windows its notepad
1. there is no code completion in text editors
 
## NotePad++
NotePad++ is a free text editor for Windows Computers. It has syntax highlighting and code completion, as well as word completion and function completion. 
## Textwrangler
TextWrangler is for Mac computers This was one of the go-to text editors for Mac Computers and now is retired
## BB Edit
BB Edit another feature packed text editor, s incorporated TextWrangler into its more robust, big,
## Visual Studio Code
VS Code has the Emmet shorthand for HTML and CSS already built-in with no additional work from you at all. VS Code has everything: syntax highlighting, themes, extensions and code completion
## Atom
Atom is a free text editor that’s available for download for Windows computers
## GitHub
GitHub is a great service online where you can host and review code, or you can post and get help with the development of your own projects
## Brackets
Brackets is a free text editor that’s available for download for Windows computers, Mac computers and Linux computers (only supports HTML, CSS and JavaScript)
## Sublime Text 3
Sublime Text 3 is premium software that can be purchased in full for $70. Otherwise you’ll use the free version
The Difference Between Text Editors and IDEs
Ide is a multiple use tool while text editor only edits text .

***
# The Command Line
## Introduction
* A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.
* Typically a command is always the first thing you type. After that we have what are referred to as command line arguments (must be separated by space)
* The first command line argument is also referred to as an option. and are typically used to modify the behavior of the command usually listed before other arguments and typically start with a dash ( - ).
* Most commands produce output and it will be listed straight under the issuing of the command. Other commands just perform their task and don't display any information unless there was an error
* After the command has run and the terminal is ready for you to enter another command
* If no prompt is displayed then the command may still be running
## Opening a Terminal
* You can open windows terminal after instating it form Microsoft app store in windows
* If you intend to remotely log into another machine when using windows then you will need an SSH client. like Putty (Links to an external site.) 
## The Shell, Bash
* This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you
* the most common one is called bash which stands for Bourne again shell.
> use a command called echo to display a system variable stating your current shell
As long as it prints something to the screen that ends in bash then all is good.
Shortcuts
* When you enter commands, they are actually stored in a history. You can traverse this history using the up and down arrow keys. So don't bother re-typing out commands you have previously entered, you can usually just hit the up arrow a few times. You can also edit these commands using the left and right arrow keys to move the cursor where you want.
## More About Files!
**Everything is a File**

A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc.
Linux is an Extension less System
### A file extension
 is normally a set of 2 - 4 characters after a full stop at the end of a file
In other systems such as Windows the extension is important and the system uses it to determine what type of file it is
Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is.
file [path] command to know for certain what type of file a particular file is
Linux is Case Sensitive
it is possible to have two or more files and directories with the same name but letters of different case in linux not in windows
Spaces in names
* a space on the command line is how we separate items
* Anything inside quotes is considered a single item.
### Escape Characters
Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.
the space would normally have a special meaning which is to separate words as distinct command line arguments. Because we placed a backslash in front of it, that special meaning was removed.
**Short cut** 
 If you use Tab Completion before encountering the space in the directory name then the terminal will automatically escape any spaces in the name for you
Hidden Files and Directories
* In Linux If the file or directory's name begins with a . (full stop) then it is considered to be hidden
To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a .
or rename it to be as such. Likewise you may rename a hidden file to remove the . 
### Summary
#### file
* obtain information about what type of file a file or directory is.
#### ls -a
* List the contents of a directory, including hidden files.

***
# Basic Navigation!
## So where are we?
* **pwd** which stands for Print Working Directory is a command that tells you what your current or present working directory is.
What's in Our Current Location?
* **ls.** It's short for list
We have run it here with no arguments in which case it will just do a plain listing of our current location
**ls [options] [location]**
In the above example, the square brackets ( [ ] ) mean that those items are optional,
Ls , basic form. Will list  the contents of our current directory
*	Ls –l , single command line option ( -l ) which indicates we are going to do a long listing which contain First character indicates whether it is a normal file ( - ) or directory ( d )
*	Next 9 characters are permissions for the file or directory (we'll learn more about them in section 6).
*	The next field is the number of blocks (don't worry too much about this).
*	The next field is the owner of the file or directory (ryan in this case).
*	The next field is the group the file or directory belongs to (users in this case).
*	Following this is the file size.
*	Next up is the file modification time.
*	Finally we have the actual name of the file or directory.
 
**ls /etc** ,a command line argument ( /etc ). When we do this it tells ls not to list our current directory but instead to list that directories contents.
**ls -l /etc** ,both a command line option and argument. As such it did a long listing of the directory /etc.
Paths
* There are 2 types of paths we can use, **absolute** and **relative** . Whenever we refer to a file or directory we are using one of these paths. (either way, the system will still be directed to the same location).
> root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories
Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )
Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.
## Let's Move Around a Bit
In order to move around in the system we use a command called cd which stands for change directory. It works as follows:
**cd [location]**
short cut ; If you run the command cd without any arguments then it will always take you back to your home directory.
### Summary
#### pwd
* Print Working Directory - ie. Where are we currently.
#### ls
* List the contents of a directory.
#### cd
* Change Directories - ie. move to another directory

***
*the end*  ...
