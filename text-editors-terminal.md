# Choosing a Text Editor

A text editor is one of the primary tools of a developer, but there are enough options that choosing one can be overwhelming. All operating systems come with a simple text editor, but there are much more advanced options with built-in tools and features to help you code.

## Available Features

Text editors can offer features such as auto-complete, which can automatically complete words you've typed before or even snippets of code; syntax highlighting, which uses text colors to differentiate elements of your code; and display options including themes that make staring at a screen all day more comfortable. Many text editors also allow the integration of extensions, which can add many more features and tools. 

## Integrated Development Environments

IDEs are suites of software that include text editors along with file managers, code compilers, and debuggers. They're probably overkill for simple web development projects, but as you get more advanced, they're worth looking at.

## How to Choose?

For very simple coding projects, you could use the text editor that comes with your computer, but for anything more complex, the tools included with a more advanced text editor will make you much more efficient. It can be a little overwhelming to choose, but many editors are free or have free versions, so you can check out lots of options before picking one:

- [Notepad++](https://notepad-plus-plus.org/downloads/)
- [BBEdit](https://www.barebones.com/products/bbedit/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Atom](https://atom.io/)
- [Brackets](https://brackets.io/)
- [Sublime Text](https://www.sublimetext.com/)

# Using the Terminal

We mostly interact with our computers using the graphical user interface, or GUI. You can also use the command line, or terminal, which allows you to "talk" more directly to the computer but can be intimidating. To open the command line in Windows, tap the start button, type cmd, and hit enter.

### Getting Started

When you open a command line window, the first line will be a prompt. After the prompt, you can type a command, along with arguments, or options, that change the behavior of the command. **Always put a space between the command and the argument, and between different arguments.**

After you enter the command, the result may be displayed in the terminal. When the command is complete, a new prompt will appear. 

### The Shell

The shell determines how the terminal behaves and looks. The most common is Bash, but we'll be using [Zsh](https://www.zsh.org/).

## Navigating in the Terminal

The first thing you need to know is where you are. To output (**p**rint) your current location (**w**orking **d**irectory), type `pwd`. To **l**i**s**t what's in that directory, type `ls`. You can add options and arguments to `ls`; for example, the option `-l` will give you a long list of the directory's contents, while the argument `/etc` will list the contents of your current directory, rather than the directory itself. 

Note that the commands and options are case-sensitive, so `-l` and `-L` will give you different results.

### Paths

Every file on the computer has a unique path. The origin of every path is the root directory. Absolute paths situate the file or directory in relation to the root directory, like a street address, while relative paths tell you how to get to the file from where you are now (like "go two blocks that way, then take a left"). Absolute paths start with `/`.

### Moving to a New Directory

To **c**hange **d**irectories, use the command `cd`, followed by the absolute or relative path of your target directory.

## Files

Ultimately, everything in the computer is a file. Files are how the system talks to itself and to the devices like monitors and keyboards that people use to interact with it. Windows uses file extensions, like .exe, .jpg, or .docx, to determine what the file does, while Linux looks inside the file itself. If you're not sure what kind of file something is, use the command `file` followed by the file's path.

Another key difference between Windows and Linux is that Linux is case-sensitive - that is, Linux considers a and A to be distinct characters. Windows sees file.txt and File.TXT as the same file, but Linux doesn't. 

### Spaces in File Names

Earlier, we noted that there must be spaces between commands, options, and arguments. There are also often spaces in file paths - how do we keep the system from getting confused?

- Put single or double quotation marks around the entire item ("Holiday Photos")
- Use the backslash to escape the space character (Holiday\ Photos)

### Hidden Files

Some files may be hidden, usually to reduce clutter and avoid accidental modification. In Linux, you can hide a file by adding a `.` to the beginning of its name. To un-hide the file, remove the `.`. To list hidden files, use the option `-a` with your `ls` command.

## Shortcuts

- Use the up and down arrow keys to reuse commands you've used before
- When building paths:
    - `~` is shorthand for the home directory
    - `.` refers to the current directory
    - `..` refers to the parent directory, and can be repeated to move up the path (`../../`)
- `cd` with no arguments will return you to your home directory
- When you're typing a path in the command line, hit tab at any time to bring up the autocomplete option (if nothing happens, there are multiple options; hit tab again to list the options). If you're auto-completing a file path with spaces in it, this method will automatically escape the spaces.
