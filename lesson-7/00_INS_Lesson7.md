# Instructor File

## Order

1. Go over `git stash`
2. Start an example with branch switching
   + Create a repo `harry-potter-characters`, echo students.txt
   	* Branch: gryffindor, hufflepuff, ravenclaw, slytherin
   	* Add students to one of the branches:
   		- Harry Potter, Hermione Granger, Ronald Weasley
   		- Commit
   	* Switch, ravenclaw:
   		-  Luna Lovegood, Rowena Ravenclaw, Gilderoy Lockhart
   		-  git switch back to gryffindor; conflict.
   		-  git stash; show difference in status; difference in switch
   		-  git stash pop somewhere else (say slytherin); re-stash; 
   		-  move to appropriate branch. show an overwrite conflict with stash (add three new ravenclaw)
   		-  try git stash pop; conflict. retains working dir changes. 
   		-  git diff stash@{0} to show difference between stash changes and WD changes
   		-  Keep stash by removing WD changes.
   		-  Commit
3. Go over git restore
   + Continue with `harry-potter-characters`
   + EXAMPLE: Restore WD from a commit.
   	*  switch slytherin; commit a few characters, and an obvious problematic one (not committed).
   		-  Draco Malfoy, Vincent Crabbe, Gregory Goyle, (Albus Dumbledore)
   			+  Stress that this is easy to remove in this situation, but assume your whole morning's work is moot. You want a quick way to restore.
   		-  git restore <filename>
   +  EXAMPLE: Restore staged back to WD. Notice that changes still there (git status.)
   	*  There are ways to restore a few versions back, but won't show here otherwise it can be confusing
   	
3. Go over git reset.
  + Stress that this can be dangerous
  	* Show with examples here in slytherin. Walk back a commit (think commit level, vs. file level for restore (not a hard and fast rule))
4. Go over git revert.
  + Same example; formal commit added to history