# Lesson 2: Git Basics

[_TOC_]

## Learning Objectives
1. Understand at a conceptual level a typical git workflow
2. Understand the differences between unstaged changes, staged changes, and committed changes.
3. Understand the use case for `git init`, `git add`, and `git commit`.

## Conceptual Overview

+ A git repository (AKA repo) is an "area" that git (the software) tracks changes to files and folders happening within. Git keeps a running history of changes happening to files: changes as minor as the addition of a simple blank space in a sentence. 

+ Think of it as a very nosy neighbour/HOA keeping tabs on everything happening in your neighbourhood/repository - but *worse* they have all the evidence from the beginning of time, and can bring them up at any point.

+ Git repositories are self-contained. Each project initiated will have its own separate history. For example, for the three repositories below, we'd have three independent workspaces, with their own unique histories:

![Diagram showing independent git repos](assets/00_git_repos.jpg =800x)

## Basic Workflow

The basic workflow is:

![Prototypical git worflow](assets/01_git_workflow.png)

+ **Work on things**: Create files, edit them, etc.
+ **Add/Stage changes**: Group logically related changes together prior to committing across one or multiple files.
+ **Commit changes to repo**: "Add a bubble to the chain". This unit of work (or snapshot) is now saved/source-controlled.

### A contrived example

I have been working on a new data visualization. In my work folder, there are three files:

1.  **viz_script.R** : A file that creates the visualization
2.  **powerpoint_for_review.pptx**: A PowerPoint file that'll contain the updated visualization.
3.  **TODO.txt**: A text file of all the changes that have been requested of this viz.
	- [ ] Viz: Change the chart type from line to bar chart
	- [ ] Viz: Change the background-color of the chart from white to light-grey
	- [ ] Viz: Update the data with latest month's
	- [ ] PPT: Update the figures in the PowerPoint
	- [ ] PPT: Use active voice within the slides

![Example of git](assets/02_git_steps.jpg =1000x)

+ At 9AM, I did two changes on the viz (change bg colour, and update the data), and 1 within the ppt (update the data figures). 

+ Later on in the day (11AM), I continue work on the visualization (change chart type) and finally, finish updating the ppt (change passive to active voice). This is shown in changes to the "Working Directory".

+ I now decide to "package" the changes. I grab all the changes related to the Viz to go first (Stage 1). I do a final do over, and determine the changes are ready to be written to the official project history. I add a **commit message**: "Updated visualization to staging".  Once this process is done, I have officially contributed to the project's history! 

+ Proceed in a similar fashion for "Commit 2".

### Initiating a git repository

To create a git repository for a particular folder, we use [`git init`](https://git-scm.com/docs/git-init). 

Navigate to the folder that needs to be source-controlled, then run `git init` in bash. If everything worked correctly, your work folder should have a new subfolder named .git (a hidden folder by default), and the address of your bash session should have been appended with "main":

This .git folder is how git keeps track of version history. Be careful not to rename, or add contents to it directly as it may affect functionality.

![initiating a git repo](assets/04_git_init.png)


### Working, Staging, Committing

![git workflow commands](assets/03_git_workflow2.jpg)

