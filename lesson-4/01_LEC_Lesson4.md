# Lesson 4: Merging

[[_TOC_]]

## Learning Objectives

1. Understand common types of merges (fast-forward merge, 3-way merges with or without conflicts)
2. Understand how to resolve conflicts

## When to merge?

Merging is a key step and tends to happen when the changes made within a branch are mature enough to become part of the `main` development branch. The question of "when" is a good time to merge will depend on the specific goal of the branch being developed, but in all cases, merging can take on three flavours:

1. Fast-forward merge
2. 3-way merge (without conflict)
3. 3-way merge (with conflict)

In all cases, merging happens **at the branch level and not at the commit level**. Merging involves consolidating the whole commit history across two branches since they initially diverged. 
Secondly, merging happens where the HEAD branch is: you are merging changes **into the branch that's currently checked-out**. For example, to merge something into `main`, you have to have switched to the main branch first. 

## Fast-forward merge
A fast-forward merge is done when the branch being merged into has not deviated since branching happened. For example, `green-branch` was created at commit `f0b140c`. Three new commits are part of the green branch, and when green-branch is being merged back into main, main is still at the same point as before.

![A fast-forward merge shown](assets/01_ffwd_merge_anim.gif)

Merging is therefore a simple process of just updating the pointers in this scenario. Note that the git merge command was run from the blue branch. Also note that the green branch still exists (the pointer still exists); but both green and blue branches now share the same history.


## 3-way merge (without conflict)

More often than not, the `main` branch would have received commits by the time a branch is ready to be merged back. In this case, git will attempt a 3-way merge (named because it'll look at three commits: branch-tip, main-tip, and the shared common ancestor).

Sometimes the new commit in `main` has no relation to the changes that were made in the branch. For example, say the branch has been modifying script1 whereas the main branch has been modifying its wiki. In this case, while there were changes made not reflected in the branch, there are no conflicts between the changes. In this case, the merge will happen automatically, and git will create a new commit called the **"merge commit"**. The merge commit is a "content-less" commit that just marks when two branches were merged into one.

![A merge commit with no conflict shown](assets/02_3_way_merge_no_conflict.gif)

Note that until the commit merge is committed, your console will read (MERGING). This can inform that a merge process is still ongoing.

## 3-way merge (with conflict)

In the case that a merge does involve the same files being modified, git will identify all the files that are affected by conflicts. This is an important point: **files must have diverged (as in received conflicting commits across branches) to be considered in conflict**. If a file has been changed in only one of the branches, then git will not consider it a conflict, and changes will be fast-forwarded. 

Within the conflicting files themselves, you will notice new entries, generally following this format:

```
<<<<<<<<<<<<<<< HEAD
On line 1 of the branch being merged to, this line exists
================
On line 1 of the green-branch, this line exists
>>>>>>>>>>>>>>> green-branch

```

This shows where the conflict occured. **Git doesn't care which version is kept**: the resolution could be keeping the source file, the incoming file, a mix of the two, or even plain deleting everything, **so long as the markings are removed from all the conflicting files.** Once all of the conflict markers are removed, it tells Git that all conflicts have been addressed.

Resolving merge conflicts is therefore purely user driven:

On [merge conflict resolution](https://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging):

> Git does not try to be overly clever about merge conflict resolution. Git’s philosophy is to be smart about determining when a merge resolution is unambiguous, but if there is a conflict, it does not try to be clever about automatically resolving it. 
> 

Once the correct version is determined, then it's a usual work-stage-commit workflow. The merged changes have their own commit.

![A merge commit with conflict shown](assets/03_3_way_merge_conflict.gif)


## Merging commands

### Initiate a merge

To initiate a merging process, switch to the branch being merged into, and execute `git merge <branch-name>`. Git will attempt a fast-forward by default. If not, a 3-way merge is attempted.


### 