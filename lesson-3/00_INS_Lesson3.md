
# Lesson 3: Git Branching

[[_TOC_]]

## Learning Objectives

1. Understand the context for branching and its benefits
2. Be able to create, move, switch, and delete branches
3. Understand the basics of `git branch`, `git stash`, `git switch`/`git checkout`
4. Understand the basics of pointers in git (HEAD/detached HEAD, etc.)


## What are branches/why are they needed?

Branches are what makes git special. While the definition of a branch itself may not be very helpful ([a branch is a lightweight movable pointer to a particular commit](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)), branching allows us to diverge from the main development line and continue working without affecting the main line at all. Think of them as alternative timelines for the same project.

Branches can be very helpful if:

+ you want to test a radical idea for your code-base but do not want to mess your previous work
+ you need to fix a bug in your code, but don't want to affect the code-base even more as you tinker around 
+ you want to develop a new feature 
+ you are collaborating on the same code-base with others and want to work concurrently

By now, we've seen the usual work-stage-commit workflow. You might even have noticed the word "main" on the right-hand side of your terminal.

![A picture showing several git branches and merges](assets/00_git_branch.png)

In this picture, we have 5 branches:

+ main (aka as "master") branch in orange
+ new-feature-1
+ branch-fix-1
+ branch-fix-2
+ new-feature-2

We notice that `new-feature-1` was branched off when `main` had two commits in. That means `new-feature-1` will have an exact snapshot of the code-base as it looked at that point. As work continued on that branch, another branch `branch-fix-1` was created after `main` received yet another commit. When `new-feature-1` was ready, it merged back into the main branch. At this point, changes from both `main` and `new-feature-1` were consolidated, in a process called **merging**. 

## About the main branch

There's nothing special about the main branch: it is a branch and has the exact same functionality as any other. Git uses main as its default name. By convention though, people tend to designate one branch as their source of "one-truth", and often that role falls to the main branch.

Note: In 2020, Github [renamed the default branch](https://github.com/github/renaming) from **master** to **main** amongst other changes, and git itself is planning to do the same in the future. Note that you might see "master" used in online documentations/books etc.

## Creating, switching branches

### Create a branch
To create a branch you use the **`git branch <branch-name>`** command with a particular branch-name.  This command will only create the branch, but won't move you to that branch. 

To move to a particular branch, you use the `git switch <branch-name>` command. The branch will be created at the particular commit you're on on your (likely) main branch.



# Things to cover

1. Provide a context for branching - why should we be branching
2. Examplify with a typical workflow
3. The main/master branch as just a default; nothing special
4. Locating yourself in the chain: HEAD and detached HEAD
5. git branch
	6. How to create new branches
	7. How to view available branches
	8. Switching branches. Moving from one workspace to the next
	9. 