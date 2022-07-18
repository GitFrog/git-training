# Basic UNIX Lab

This session is about getting used to UNIX commands prior to learning git specific ones.

Long-story short, git itself was built on UNIX-like system (i.e. not Microsoft), and so some of the commands that we are familiar with on Windows are not available to us in Git.

Here's a list of shortcuts/commands that are important to know:

|Name|Expanded Name|Description|Example|
|-|-|-|-|
|[cd](https://ss64.com/bash/cd.html)| Change directory| From current position, change the current directory | `cd c/`|
|[mkdir](https://ss64.com/bash/mkdir.html)| Make a/multiple directory| From current position, create the current directory|**Single**: `mkdir testFolder`<br>**Multiple**: `mkdir dir1 dir2 dir3`|
|[pwd](https://ss64.com/bash/pwd.html)|Print working directory| Get user's current directory| `pwd`|
|[ls](https://ss64.com/bash/ls.html)|List files (+ info about them)| From current position, list all the contents within the directory. Adding the `-a` flag shows hidden files/folders (a for all)|`ls`|
|[start](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/start)| NA| Start a separate program and or file explorer in current context|`start .` will open a File Explorer in the current directory. **Windows only**|
|[touch](https://ss64.com/bash/touch.html)|NA|Create a/multiple file(s) given a name/Change other param to a specified file|**Single**: `touch testfile.txt`<br> **Multiple**: `touch file1.txt file2.txt file3.txt`|
|[rm](https://ss64.com/bash/rm.html)|Remove|Remove a/multiple file/folder. NO UNDO HERE|A/multiple files:`rm somefile.txt somefil2.txt`<br>A folder: `rm -rf foldername`|

