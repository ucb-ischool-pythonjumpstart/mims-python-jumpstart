# Breakout Exercise 1

Goal: Create a git repository, start tracking files and checkout an earlier commit.

# Intro (as a group)

1. Make a directory called "my-repo"
  `mkdir my-repo`
2. Initialize this directory as a git repository:
  `cd my-repo`
  `git init .`
3. Make a file in this directory called "lunch.txt"
  `touch lunch.txt`
4. Aside: lets look at what files are being tracked
  `git status`
5. Add the blank file to tracking using:
  `git add lunch.txt`
6. Make your first commit by running the command:
  `git commit -m "Initial Commit"`
7. We made our first commit! Let's look at our commits:
  `git log`
8. Look at changes between a commit and our current head
   `git diff <commithash> HEAD`


# Breakout 1 (groups of 2)

6. Modify lunch.txt. 
Use Vim to write what Parter A had for lunch today inside the lunch.txt file
7. Check git status - does git think things changed? 
8. Make a second commit with the new change.
9. Modify lunch.txt again to add what Partner B had for lunch today on another line.
10. See what changes have been made since your last commit
11. Commit Again
