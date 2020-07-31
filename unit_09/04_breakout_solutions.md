# Git: Commit & Checkout

## Intro (as a group)

1. Make a directory called "my-repo"
  `mkdir my-repo`
2. Initialize this directory as a git repository:
  `cd my-repo`
  `git init .`
3. View the new .git file that's created in the directory
  `ls -a` 
3. Make a file in this directory called "lunch.txt"
  `touch lunch.txt`
4. Aside: lets look at what files are being tracked
  `git status`
5. Add the blank file to tracking using:
  `git add lunch.txt`
6. Show status updated
  `git status`
6. Make your first commit by running the command:
  `git commit -m "Initial Commit"`
7. We made our first commit! Let's look at our commits:
  `git log`
8. Look at changes between a commit and our current head
  `echo "Apple" >> lunch.txt`
  `git diff lunch.txt`
9. Commit Again, and we can compare between commits
  `git commit -m "Add second lunch"`
10. Look at our commit history, now we have two commits 
  `git log`
11. Look at the difference between any commit and another
  `git diff <commithash> HEAD`

## Breakout 1 (groups of 2)

Goal: Create a git repository, start tracking files and checkout an earlier commit.

6. Modify lunch.txt. 
Use Vim to write what Partner A had for lunch today inside the lunch.txt file
  `vim lunch.txt`
  `i` enter insert mode 
  type and add the text you want to
  `esc` leave editing mode
  `:w` write your changes to the file
  `:q` quit Vim
We can also do this with echo and pipe commands we learned about yesterday.
  `echo "burrito" > lunch.txt`
7. Check git status - does git think things changed? 
  `git status`
8. Make a second commit with the new change.
  `git commit -m "Add PartnerA lunch`
9. Modify lunch.txt again to add what Partner B had for lunch today on another line.
  `echo "PB&J" >> lunch.txt`
10. See what changes have been made since your last commit
  `git diff`
11. Commit Again
  `git commit -m "Add PartnerB lunch`

## Checkout Overview (as a group)

1. Checkout an earlier commit
  `git checkout 4c608b0d1226`
2. Files have changed to what they were in previous commit
  `cat lunch.txt`

# Breakout 2 (groups of 2)

1. Using the same repository from Exercise 1, make a new file named dinner.txt with both partners dinner plans for tonight in it.
  `echo "burger" >> dinner.txt`
  `echo "pho" >> dinner.txt`
2. Also modify the lunch.txt file. Use vim to edit what Partner B had for lunch, and change the line to say their favorite meal to eat for lunch, rather than what they had today.
  `vim lunch.txt`
3. Add both files to staging area.
  `git add -A`
4. Make a new commit with the changes
  `git commit -m `
5. Checkout an earlier version of the lunch.txt file
  `git checkout 1021 lunch.txt`

# Merging / Branching (as a group)
## Visual Overview
1. Walkthrough Visual Overview of GitHub Merging
  http://git-school.github.io/visualizing-git/#free
  `git commit -m "Initial commit"`
  `git checkout -b feat-a-branch`
  `git checkout master`
  `git commit -m "commit three"`
  `git checkout feat-a-branch`
  `git commit -m "Finish feature A`
  `git checkout master`
  `git merge feat-a-branch`

## Merging on the Command Line 
1. Make a new branch for Feature A
  `git checkout -b feat-a-branch`
2. Make some changes
  `touch newfile.txt`
3. Commit Changes to Feature A Branch
  `git add newfile.txt`
  `git commit -m "Finish Feature A"`
4. Merge in new Feature branch
  `git checkout master`
  `git merge feat-a-branch`
  `git branch -d feat-a-branch`

## Merge Conf
5. Merge conflicts and debugging
  `git log --merge`
  `get diff`
  `git merge --abort`

## Breakout 3 (groups of 2)
1. Make a new branch with name "fav-din-branch"
  `git branch fav-din-branch`
2. Add you and partners dinners to dinner.txt on new branch
  `vim dinner.txt`
3. Use diff to look at difference in dinner.txt between the branch and the master
  `git diff 5115HashFavDin MASTER dinner.txt`
4. Check status to see what files are tracked
  `git status`
4. Commit the changes to dinner.txt to the branch
  `git add .`
  `git commit -m "`
5. Merge dinner 
`git merge fav-din-branch`

## Merging/ Branching with Two Features

2. Make a new branch for Feature B
`git checkout -b feat-B-branch`
3. Make some changes
  `touch newfile.txt`
  `git add newfile.txt`
  `git commit -m "Finish Feature B"`
4. Make some changes
  `touch newfile.txt`
  `git add newfile.txt`
  `git commit -m "Finish Feature B"`
3. Make a new branch Feature B
`git branch bugfix-b-branch`
4. Look at existing branches
`git branches`
5. Check status that HEAD is pointing to merge-receiving branch (in our casemaster)
`git status`
`git checkout master`
5. Git Merge
`git merge `



`git checkout -b fav-din-branch`








