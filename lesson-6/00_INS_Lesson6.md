# Instructor File - Lesson 5

## Order

1. Go over sections
	- What are remotes exactly?
	- Working with remotes
		+ Stress that remotes setting up is more of a one-time thing
		+ Two use cases:
			* Existing repo that is cloned (easiest)
			* A local repo that is being uploaded to the cloud.
2. Start example:
 	+ Move the AIW repo to Azure DevOps (existing local ==> cloud)
 		* Show `git remote -v` before and after
 	+ Clone from AIW to another folder.
 		* Show `git remote -v`
3. Go over `An example of a workflow` section
4. Start collab example:
	+ Create a new git repo (`collab-example`), upload to AzureDevOps
		* set up two bash sessions; change user name/email locally to "user1/email1", "user2/email2" respectively
		* Go through user1 work-stage-commit-push workflow
		* Go through user2 `fetch` workflow
			- Show changes between `git log` and `git log -r`
			- Merge changes
		* Go through user2 work-stage-commit-push workflow
		* Go through user1 `pull` workflow
			- Show automatic merge; show conflict merge
			- Notice how both have merge commits
		* Go through `push` workflow from user1; pull from user2; resolved history.


---

For collab example:

https://app.inferkit.com/demo "Why should DevOps be used in the OPS?" / "Do you hate git? Why or why not"