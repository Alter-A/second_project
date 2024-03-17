# This is repo for learning Git courses

## git bash commands 
Some good for start commands and useful info

### Create local repository

Note: To create repository firstly create a project folder which will contain all project files, e.g. code files, small databases, disruption and documentation files.

To create repository navigate to local folder and use this command:
`git init`

*Oh it's mean to be a cheat sheet.*

### View status of repo
Viewing current branch, what files are changed since last commit
`git status`

### Change branch name
Change name to e.g. main
`git branch -m main`

### Set username and email
Set up username and email for committing
NOTE: can differ from the GitHub username and login email, but usually they are same
```
git config --global user.name "username"
git config --global user.email "name@example.com"
```

### Prepare for commit
After creating files prepare files for commit
`git add <file name>`

### Commit to repo
Then commit and add optional comment
`git commit -m "note for commit"`

### Add link to remote repo
Example GitHub
`git remote add origin git@github.com:<username>/<repo name>.git`

### Copy local changes to remote repo
After adding link to remote repository you are ready to put project files to remote repository. In this example git push local branch 'main' to remote repository.
- for the first  time to save link in config
    `git push -u origin main`
- for subsequent pushes
    `git push`

## Commit, it's hash and commit logging

### Commit hash
After executing`git commit`, each commit obtains a unique hash. Even changing a single symbol will result in a new hash.
Git or GitHub uses hash as ID number.

### Commit logging
To see commit log use command
`git log`
The output will display the hash, author, date, and optional message of each commit.

If there are too many of commit use command
`git log --oneline`
The output will display only a few symbols of the hash and optional message

### HEAD - service file
Last commit hash stores in special service file named HEAD. You can use `HEAD` instead of last commit hash on git bash commands

## File status in git 
Several file status displayed in the `git status` output. 

### untracked
- obtaining the status
    new file
- lost of status
    `git add`

### tracked
- obtaining the status
    `git add` or `git commit`
- lost of status
    `git reset` or `git rm --cached` or changes in file 

### staged 
- obtaining the status
    `git add`
- lost of status
    `git reset` or `git rm --cached`

### modified
- obtaining the status
    changes in file
- lost of status
    `git add` or `git reset` or `git rm --cached`
