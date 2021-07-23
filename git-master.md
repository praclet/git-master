# Learning Git : Part 1

This first part of the tutorial will make you think about the internal basics of Git (from an individual point of view)

You will find little exercises aimed to put you in difficult situations. Next to it, there will be the global command recommanded to fix your situation (without giving the answer). Please, talk with your neighbor, there are no dumb questions, and with Philippe, we'll be here to help you. Please follow the tutorial's order, as the learnings are progressive and will help you for the next points.

> Don't hesitate to fail, do crazy thing !!!!!!!

### What is Git ?

A **decentralized version control system** (:exclamation: important, often asked on job interviews). What does that mean ? Do you have an idea ? https://fr.wikipedia.org/wiki/Git

It only has 17 years, with the first really usable version released in 2007. 

The `decentralized ` word is important (cf. wikipedia)

#### Basic repo

As this part of the tutorial is only focused on your individual manoeuvres, you will have to create your own dumb repo:

1. Create a repo named `learn-git-part1` on the github website
2. Follow the creation steps
3. clone it locally

> You're good to go ! :smile:



## Let's dive in

If you followed properly the initialization process, you should be on `main` branch with a first commit.

> <u>IMPORTANT POINT</u>:
>
> Git is decentralized, which means that your local clone is exactly like a `branch` of the remote (distant) repository

You may already be familiar with `add`, `commit`, `push`. Are you ?

Git has several management levels for modified files:

* unfollowed / Modified
* followed (git add)
* staged (git commit)
* Synced (git pushed)

[for accurate naming, check there](https://ndpsoftware.com/git-cheatsheet.html)

<u>Exercises:</u>

> PS: I'm using synonyms/confusing words for a reason



### 0. Followed file

1. Create a new file `test0.c`

2. Set to to a followed state [cf. above `dive in` might help]
3. Verify its status
4. Do a `git log`, did it appear in your history ? What do you conclude ?

5. UNDO IT ! (git cli should help)



### 1. Staged file

1. Create a new file `test1.c`

2. Set it to a `staged` state  [cf. above `dive in` might help]

3. Verify its status
4. Do a `git log`, did it appear in your history ? What do you conclude ?

5. UNDO IT: make it go from `staged` state to `followed` state 
6. Then, undo from `followed` to `unfollowed` state

> **What can you conclude about the history from the differences in these exercises ?**



### 2. Changing the content of a commit

1. Create a new file `test2a.c`

2. Set it to a `staged` state  [cf. above `dive in` might help]
3. Verify its status / git log <- it should appear in the history // TAKE A GOOD LOOK AT THE GENERAL STATUS OF THE HISTORY

4. Create another file `test2b.c` 
5. Add it to the previous commit and change its name (the number of commits shouldn't change!)
6. Push it



### 3. branch 101

1. Create a branch named `bogoss`

2. Create a file `test3-bogoss.c` inside this branch and commit it
3. Inside the `main` branch, create `test3-main.c`, and commit it
4. Check `bogoss`'s branch history
5. Rebase the` bogoss` branch with the `main` branch
6. Check `bogoss`'s branch history (again)
7. Merge the `bogoss` branch inside the `main` branch

8. Delete the `bogoss` branch



### 4. Stash

1. Create a file `test4-main.c` on `main` branch

2. You have an urgent fix to do on the ANTEPENULTIMATE (:wink:) commit, take the necessary measures to simultanously save your current work and have a clean working directory
3. Change the ANTEPENULTIMATE commit name :wink:
4. Get your saved work back



### 5. Undo 

1. Create a file `test5-main.c` on `main` branch and commit it

2. Modify it again, and `commit` the modification again
3. Undo last commit
4. Undo last changes



### 6. Squash

1. Create a new branch `cherstylé`

2. Make some random changes so that the branch history has 4 different new commits
3. And now, these 4 different new commits must become one



### 7. Conflicts

1. Create and commit a new file `test-7.c` on `main` branch
2. Create and commit a new file `test-7.c` on `cherstylé` branch with a different content (on the same lines)

3. Merge `cherstylé` on `main`

4. Resolve conflict(s) :smirk:



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