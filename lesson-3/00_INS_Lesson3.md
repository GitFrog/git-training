# Instructor File - Lesson 3

## Order

1. Go over sections
	+  What are branches
	+  About the main branch
2. Start example:
	+ Current state: Creation of AIW repo. Showed init, added a few commits, and showed git log. No branching shown
	+ We're going to replace the name Alice with [some-name], but might change my mind
	+ Create branch from current position. Use git branch. Move to branch.
	+ Stress difference between `main` and new `branch-name`. Show `git branch -v`
	+ Do change, commit. Switch and show differences in file/workspace between branches.
3. Back to sections:
	+ Idea of how things are kept straight in git. How does it know to populate the right files in my work folder?
	+ Section git internals: hash, pointers **up to branch-tip**
4. Back to example:
	+ Show git log, add a new commit, show how branch tip has moved.
	+ Explain that once you switch branch, git knows to clear your workspace and populate with the contents of that commit.
5. Back to sections:
	+ How does git know where **you** are located. HEAD pointer. Explain when that everything is in synch, HEAD points to what branch-tip is pointing (sync)
	+ What if you wanted to check out a particular commit?
		* Detached head!
6. Back to example:
	+ Show example of a detached head. And how to switch back.