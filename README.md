# Git Glossary used in training

### Repository (repo)
A folder containing all the files relating to a particular projeect. (The folder also has hidden files that contain all the git details and version history of the files)

### Fork
An online copy of an an entire repo. This is usually so different users can work indenpendently.

### Clone
A clone is a duplicate of an entire repository that lives on your computer instead of on a website's server.  
With your clone you can edit the files in your preferred editor and use Git to keep track of your changes without having to be online. It is, however, associated to the remote version so that changes can be synced between the two. You can push your local changes to the remote to keep them synced when you're online.

### Remote
Your local clone refers to its online counterpart as a remote.  
By default, you have a remote called "origin" that points to your own fork, and a remote called "grantadesign" that points to the official version shared by everyone.

### Commit
To commit is like saving your changes to the repository. Each commit is added to a previous, or parent commit. They can be stacked up and branch into a tree structure resulting in different versions of the whote repository.  
A commit has a unique SHA reference (looks like a guid 1a410efbd13591db07496601ebc7a059dd55cfe9).  
Depending on the context, it can refer to:
* the set of changes made in that commit
* a snapshot of the repository at that point, like a version number for the whole repository.

### Notes about committing changes
* Once changes have been committed, they are safe. It is very hard (or impossible) to break a repository. Don't worry about making a mistake, it is always possible to go back to a previous state of the files. However uncommitted changes can be lost, so don't be afraid to commit!
* Try to make each commit contain an single coherent change. If you have made several changes at once commit them separately.

### Branch
A branch is a parallel version development. It is contained within the repository, but can be separate to the primary or "master" branch allowing you to work freely without disrupting the official version of files. When you've made the changes you want, you can merge your branch back into the master branch to publish your changes.  
In reality though, a branch is more like a label pointing to a particular commit. When you make a new commit onto a branch, it just makes a new commit on top of the one the 'label' points to. It then moves the label to point to your new commit.

### Git
Git is the open source method for tracking changes in text files. It was ritten by the author of the Linux operating system.

### GitHub
A company that runs the GitHub website, based on the core technology Git. It is designed for collaborative work between many users.

### GitHub Desktop
The Windows application that runs on your desktop to manage your repository and files locally on your machine.  
It is designed to work with the GitHoob website, but it is not the only client you can use. We use it because it is the simplest to use.  
The graphical interface only supports the basic Git functionality, but everything else can be achieved via the command line (Git Shell)

### Checkout
To "checkout" a branch is to switch to to that that branch on your local machine. All the files in the folder will be replaced to match the state of the repository at that point in time.  
You can also checkout to any point in time by using the SHA reference of the commit. This is called a detached-head, as it does not have a branch label associated with it.

### Head
Either:
* The tip (last commit) of a branch.
* Or the current checked-out commit.

### Undo
In GitHub Desktop, you can "Undo most recent commit"  
This should only be applied to only your own work. Once the commit has been pushed (ie. you can see it online) you should not undo, but instead "revert".  
Remember that you can never truly delete any changes in Git, so what this actually does is move the branch "label" to the previous commit. The old commit is still there, you just cant see it because it's no longer part of the current branch.

### Revert
"Undo" can only be applied to that last commit. You can undo multiple times, but what if you want to undo the second-last commit, but keep the last?  
Here you must "revert" a commit. What this actually does is create a new commit that reverses the changes

### Push
Push any new commits from the current branch on your local machine to an online repository (a remote).  Either your fork (the remote called "origin") or the official shared version (the remote called "grantadesign")

### Pull
As with push, but instead pulling changes from online onto you local machine.

### Merge
To add the changes contained in one branch into another branch, or from one fork into another fork. This is will usually be where you make changes in your own fork, and then merge them into the official grantadesign version. Merging is often done through a Pull Request

### Pull Request
A request for a particular merge to be made. If you have permissions you can manually merge, otherwise you have to request someone else does it. When you create the pull request, anyone who is authorised will be emailed and can review it.  
* Even if you do have permissions, it is a good idea to create a pull request so a second person can review it before adding to the master.  
* Try to create a pull request that encompases a set of related changes, if it is two seperate features, creat two pull requests.  
* If you push more changes to the branch after creating the pull request, they will be automatically included when it is finally merged.  
