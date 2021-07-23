In these exercices we suppose you already have an understanding of some basic Git commands such as clone, commit, push, pull.

# Learning Git : Part 1

This first part of the tutorial will give you some insigth on the internal basics of a local Git repo and a remote Github repo (from a solo worker point of view).

You will find little exercises which will put you in difficult situations, our goal is to give you the knowledge to get out of such situations. Please, talk with your mates, there are no dumb questions. Please follow the tutorial's order, as you will construct a repo and the later exercices suppose the existence of files you're going to create in the former ones.

> Don't hesitate to fail, do crazy things !!!

### What is Git ?

A **decentralized version control system** (:exclamation: important, often asked on job interviews). What does that mean ? Do you have an idea ? For some non technical information: https://fr.wikipedia.org/wiki/Git

It's only 17, with the first really usable version released in 2007. 

The `decentralized` word is important. (cf. wikipedia)

#### Basic repo

As this part of the tutorial is only focused on your individual actions, you will have to create your own dumb repo:

1. Create a `learn-git-part1` repo on your github repo
2. On your system execute the git command `git init learn-git-part1`
3. Change to the directory `learn-git-part1` 
4. To connect the local repo to the remote one, exexute the Git command (with the correct LOGIN) `git remote add origin https://github.com/LOGIN/learn-git-part1.git`

> You're good to go ! :smile:

The following exercices will done in that new repository.

## Let's dive in

If you followed properly the initialization process, you should be on the `master` (or `main`) branch with a first commit.

> <u>IMPORTANT POINT</u>:
>
> Git is decentralized, which means that your local clone is exactly like a `branch` of the remote repository.

Git has several management levels for your files:

* workspace : where you actually work
* staged/indexed (git add)
* local repository (git commit)
* remote repository (git pushed)

[more details](https://ndpsoftware.com/git-cheatsheet.html)

<u>Exercises:</u>

### 0. Indexed file

1. Create a new file `test0.c`
2. Set it to an `indexed` state [cf. above `dive in` might help]
3. Verify its status
4. Do a `git log`, does it appear in your history? What can you conclude?
5. UNDO IT! (git cli should help)

### 1. Local repository file

1. Create a new file `test1.c`
2. Add it to the local repository  [cf. above `dive in` might help]
3. Verify its status
4. Do a `git log`, does it appear in your history ? What can you conclude ?
5. UNDO IT: remove it from the local repo (it's still indexed by Git)
6. Then, remove it from the indexed files of the current repository

> **What can you conclude about the history from the differences in these two first exercises ?**

### 2. Changing the content of a commit

1. Create a new file `test2a.c`
2. Commit it.
3. Verify its status / git log <- it should appear in the history // TAKE A GOOD LOOK AT THE GENERAL STATUS OF THE HISTORY
4. Create another file `test2b.c` 
5. Add it to the previous commit and also change this commit's name (the number of commits shouldn't change!)
6. Push it

### 3. Branch 101

1. Create a branch named `bogoss`
2. Create a file `test3-bogoss.c` inside this branch and commit it
3. Inside the `main` branch, create `test3-main.c` and commit it
4. Check `bogoss`'s branch history
5. Change the `bogoss` branch so the current `main` commit becomes its direct predecessor
6. Check `bogoss`'s branch history, it should be different from what you saw in step 4
7. Merge the `bogoss` branch inside the `main` branch
8. Delete the `bogoss` branch

### 4. Undo 

1. Create a file `test5-main.c` on `main` branch and commit it
2. Modify it again and `commit` the modification again
3. Undo the last commit
4. Undo the last changes

### 5. Squash

1. Create a new branch `lesbails`
2. Make some random changes so that the branch history has 4 different new commits
3. And now, these 4 different new commits must become one

### 6. Conflicts

1. Create and commit a new file `test-7.c` on `main` branch
2. Create and commit a new file `test-7.c` on `lesbails` branch with a different content (on the same lines)
3. Merge `lesbails` on `main`
4. Resolve conflict(s) :smirk: (We're keeping the `lesbails` content)

# Learning Git : Part 2

After seeing all the `in-depth` of git for a personal usage. Let's see the development workflow for teams.

For that, I created a special open source repository for you: https://github.com/grouville/awesomeOpenSourecProject

If you're here, ping me/raise your hand and I'll add you as a contributor.

> Prerequisite: install github cli with brew

### 1. Proper setup for opensource projects

1. On github, fork the project
2. Clone the main repo
3. Remote add the fork to your repo

4. Make a modif and push it to `origin/main` 



### 2. Create a PR (Pull request)

1. Make a modif
2. Push it to your fork (important!)
3. Merge request and assign me as a reviewer
4. Ping me when the PR presents no conflicts



### 3. Work on any PR

1. Push a PR 
2. Checkout back to `main`

3. Using github CLI, try to work on any PR available on the repo (yours if you're alone :angel: )

4. Change history
5. Find a way to pass on the changes to the current PR



# Learning Git : Part 3

Good job Padawan ! 

Previous part leveraged the https://github.com/grouville/awesomeOpenSourecProject repository. It contains several automatic checks, implement them (ask me personally, I won't write them here, it could help you)