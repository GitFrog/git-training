# Lesson 5: Finding differences

[[_TOC_]]

## By the end of this module, you will be able to:

1. Understand the output of `git diff` 
2. Undertand how to compare changes that are unstaged, staged, and committed 


## Keeping track of changes

We've seen how we can navigate between commits. If we wanted to compare the changes made between commits, we can do so using `git diff`. 

Depending on the parameters used when invoking `git diff`, the comparison can be made between any two arbitrary commits. Often it can be used to compare:

1. Your working directory (as in the most recent changes made) and the last commit in your repo
2. The change from what you've staged and what's in your working directory
3. The change between two arbitrary commits

## The `git diff` command

By default, the command will look for all changes across all files between two commits. One can specify exactly which commit/branch, as well as which file to compare to make the output more manageable.

### Running: `git diff`

Running git diff with no further parameters will compare changes in your working directory and changes (if any) that have been staged. If staged changes and working directory are the same, there will be no output.

### Running: `git diff HEAD`

Running git diff HEAD will compare changes in the working directory and the last commit in HEAD. If there are no changes in the working directory (whether staged or not), there will be no output.

### Running: `git diff --staged HEAD`

Run git diff --staged HEAD will compare the difference between what's been staged and the last commit in HEAD. If nothing is staged, there will be no output.

Here's a summary of the above:


![Summary of git diff for common operations](assets/00_git_diff.png =1000x)

## Interpreting the output from `git diff`

To simplify, assume we're comparing two versions of the same file, each with the following contents. Intially we wrote File A, and then found a typo and learned that Pluto was no longer considered a planet. We generated File A':

|File A|File A'|
|-|-|
|Marcury|Mercury|
|Venus|Venus|
|Earth|Earth|
|Mars|Mars|
|Jupiter|Jupiter|
|Saturn|Saturn|
|Uranus|Uranus|
|Neptune|Neptune|
|Pluto||

If a git diff was run on this file, we can expect this kind of output:

![A typical git diff output](assets/01_git_diff_output.png =1000x)

Here is an explanation of what the lines mean:

1. **Files being compared**
	+ The line `diff --git a/fileA.txt b/fileA.txt` says that Git is comparing two versions of the same file, fileA.txt. Git will identify one of them as "a" and the other "b". This makes sense because in git diff, we're tracking changes to each file with another version of the same file.

2. **Git internals/metadata**
	+ The line `index <hash>..<hash> <6-digits>` refers to the two git objects being compared. This is not mission-critical to know, and is unlikely to be relevant at this point.

3. **File Markers/Identifiers**
	+ Here Git clarifies how it's going to annotate changes coming from file "a" and "b"
		* Any changes coming from "a" will be annotated with `-`
		* Any changes coming from "b" will be annotated with `+`
		* Context will help interprete which files come from which source.
	+ Resist the temptation of interpreting these purely as "subtraction" or "additions" between the two files. 
	
4. **First Code Chunk**
    + When 'diffing' two files, git is smart not to output the whole file onto the console. Rather, it'll zone-in on where there are differences between the files. The code-chunk identifies where the first set of changes have occured. One file can have multiple code-chunks (as is the case here)
    + `@@ -1,4 +1, 4 @@`
    	* `@@` flank the beginning and end of the code chunk header
    	* `-1,4`
    		- This means "extract 4 lines from Line 1 of file having changes annotated with `-`: in this case, this is a/fileA.txt.
    	* `+1,4`
    		- This means "extract 4 lines from Line 1 of file having changes annotated with `+`: in this case, this is b/fileA.txt.
 
 5. **Another Code Chunk**
 	+ This is another code chunk that is independent from the one that came before. The rules to interprete the changes are the same.
 

 Taken together, we can interpret the output as follows:

 1. Line 1 diverges between the files: Marcury and Mercury
 2. Lines 9/10 are different between the two files:
    + Pluto exists in the "a" file but doesn't in "b" file. Note that there is no `+ ` (+ and a blank space) as it is understood.
    

