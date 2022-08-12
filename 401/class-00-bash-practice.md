# Practicing in the Terminal

## [The Command Line](https://ryanstutorials.net/linuxtutorial/commandline.php)

- Text-based interface with the computer.
- Starts with a command, optionally followed by arguments separated by spaces. The first argument may be referred to as an option.
- Shells determine how the terminal will look and behave. The most common is bash, but we're using zsh.

## [Basic Navigation](https://ryanstutorials.net/linuxtutorial/navigation.php)

- Because the terminal is text-based, you have to use commands to navigate around
- Some basic commands:
  - pwd (**p**rint **w**orking **d**irectory) outputs the directory you're currently in.
  - ls (**l**i**s**t) outputs the contents of a directory. If used without arguments, outputs the contents of the current directory.
  - cd (**c**hange **d**irectory) lets you move to a different diretory. If used without arguments, sends you to the home directory.
- File paths:
  - An absolute path starts at the root directory and points to the same location no matter where you are when you use it
  - A relative path points to a location relative to your current location, so its end might change depending on where you are
  - Useful characters: `~` represents the home directory; `.` refers to the current directory; `..` refers to the parent directory.

## [More About Files](https://ryanstutorials.net/linuxtutorial/aboutfiles.php)

- Everything on the system is some kind of file
- Linux ignores file extensions and looks at the actual file to determine what it is
- Linux is case-sensitive, so File.txt, FILE.txt, and file.txt are all distinct files
- If spaces are used in file names, either use quotes or escape the space using `\` to tell the system to ignore it
- Hidden files have a `.` in front of them. Files can be hidden to keep them out of the way or to prevent accidental modification.

## [Manual Pages](https://ryanstutorials.net/linuxtutorial/manual.php)

- Linux has a manual that can be accessed using the `man` command, followed by what you want to look up
- If you're not sure what specific command to look up, you can search by entering `man -k` followed by a search term to do a keyword search
- Command line options have a longhand and shorthand version
  - Longhand commands spell out the whole command and are preceded by `--`
  - Shorthand commands are a single letter preceded by `-`, and can be chained together. For instance, `ls -alh` returns a long (`l`) human-readable (`h`) list of all (`a`) files in the current directory.

## [File Manipulation](https://ryanstutorials.net/linuxtutorial/filemanipulation.php)

- Create directories using `mkdir`
  - Use `-p` to create any needed parent directories
  - Use `-v` to make the terminal print what it's doing as it makes the directories
-Use `rmdir` to remove a directory. This also accepts `-p` and `-v`. Note that only empty directories can be deleted this way (see `rm`, below).
- The `touch` command modifies the access/edit timestamp on an existing file, or creates a new blank file if the target file doesn't exist
- The `cp` command copies a file or directory
  - The origin and destination are paths (either relative or absolute)
  - You can copy a file to the same destination; the file will be renamed the filename specified in the command
  - Use the `-r` (**r**ecursive) option to copy directories and their contents
- The `mv` command moves files and directories (moving directories doesn't require `-r`)
  - To rename a file, "move" it to the same directory but specify a different name
- The `rm` command removes a file; use it with `-r` to remove directories that aren't empty
- **NOTE:** `rm` and `rmdir` cannot be undone, so use with caution

## [Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

- A cheat sheet!
