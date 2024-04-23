# Git_Examples
**Git Practice Examples for DevOps Engineer**

Quick setup — if you’ve done this kind of thing before
https://github.com/xxxxx/Test_Repo.git


**Prerequisite:**

1 Open URL https://github.com/ and click on Sign Up and create account

2 Download Git from https://git-scm.com/download/win and install it


**I. Create a new repository on the Github site:**

1. Logon to https://github.com/ 

2. Click on "+" sign at right corner and select "New Repository"

3. Give Name to the new repository and click on "Create reposotory"


**…or create a new repository on the command line:**

Create new folder Named "Git_Practice" and run git bash from the same folder 

```
  echo "# Test_Repo" >> README.md
  git init
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin https://github.com/xxxxx/Test_Repo2.git
  git push -u origin main
  ```
  
**II. …or push an existing repository from the command line**

Create new folder Named "Git_Practice" and run git bash from the same folder 

```
git init
git config --global user.name "xxxxx"
git config --global user.email "xxxxxe@gmail.com"
touch f2.txt
git add .
git commit -m "a"
git remote add origin https://github.com/xxxxx/Git_Test.git
git push -u origin main / master (first time only)
touch f3.txt
git status
git add .
git commit -m "b"
git push 
```

# Git Basics

### Run For the first time
```
git config --global user.name "subrotoice"
git config --global user.email "subroto.iu@gmail.com"
```

### Upload a new project
```
git init // Basically 3 steps, 1. add, 2. Commit, 3. Push; https://prnt.sc/9_BUPJ6VX53L
git add . // added to staged area, and ready for commmit; git add -A // same, all files; git add index.html // only index.html file
git commit -m "first commit" // Save as a snapshot what remain in staged area
git remote add origin https://github.com/subrotoice/ccn.git // ("origin Userdifine", origin=url.git, variable e value assign korar moto)
git push -u origin master // push, origin user define name like variable contain url. (master default brunch name, you can create brunch like, https://prnt.sc/26pq9x2
```

### Work on an existing Project
```
First you have to download project otherwise it will not work
git clone https://github.com/Tilotiti/jQuery-LightBox-Responsive.git // Pull
cd folder_name // Need to change to inside folder
git add . For all new file and folder (git add file_names.exten it is for single file)
git commit -m "committed message" For asingle file(git commit -m "committed message" file_names.exten)
git push -u origin master // First time pushing the branch or if you've made changes that conflict with the remote repository, you might need to use the '-u'
git pull origin master // Change in github, it take effect in local reprository. 'Synchronization'
```

### Work on existing Project - Delete Some files and add new files | It is possible to rename reposiotry
```
1. Delete files manually using mouse keyboard
2. git add .
3. git commit -m "Deleted Files"
4. git push -u origin master
// Another way
1. git rm file1.txt file2.txt file3.txt // remove files and here not need to stage(git add)
2. git commit -m "Remove files: file1.txt, file2.txt, file3.txt"
3. git push -u origin master
```

### Commit: goto a commit number
```
git checkout 736259f3b3fc9404ec7f8104dc3df98ab84e6b7e // commit number
git log --oneline // in One Line; 
git log // in details
```

### Remove top commit from github
```
git reset --hard HEAD~1  // to remove top 2: git reset --hard HEAD~2
git log --oneline
git push -f
```

### Branch Practice--- master(default)
```
git bracnh // show all branch and current branch in green; (for details) git branch -v / git branch -a
git branch main // Create main new branch; git checkout -b newBranch // create+Switch to newBranch
git checkout main // switch to main branch
git merge main // first go to master using git checkout master then run merge command; it also brings all commit histor; Merge er pore abar commit kora lagte pare
git branch -d newBranch // delete branch
```

### Remote(GitHub)
```
git add remote <UrlName> <URL-www.>
git remote -v // See URL; git remote aslo work but show only git name
git remote set-url secondURL https://github.com/subrotoice/kst.git // Change URL for second identifier
git push -u third master // you can push without switching branch, ie. from master branch you can push to other branch; https://prnt.sc/QAaFTy0Lt1_s
git push -f second main // Forch Push
git clone -b <branchName> <remote-repo-url> // Clone a Specic Branch from remote repo; ie. git clone -b main9 https://github.com/subrotoice/test9.git // Working, Here brunch name main9
```

### Basic Windows command like cd
```
cd\ = back to root directory c drive does not metter where its current postion
cd .. = One step back
cd /d D: = C Drive to D drive
dir or ls(LS) = List all file and folder of current directory. "ls" is more clear to read
mkdir mynewfolder = Create New Folder
echo tailwind-landing >> README.md // Create file and put content Best*  shor: echo > asdfwe.txt (Create file only no content)
cd "folderName" = To enter Folder for doing some task
cls = Clear Screen // "clear" in git bash
```

### Rename Commit
```
git commit --amend -m "Modified Message"
git push origin main --force
```

### Committed changes to a repository and then made additional changes that you want to include in that same commit
```
git add <file(s)> // ie. git add README.md
git commit --amend
git push --force // Need to force push to the remote repository if you've already pushed the previous commit.
```

### Miscellaneous (Code WIth harry)
```
4 state of git: https://prnt.sc/oqsuL3IZ2wwt GitBash: https://prnt.sc/9_BUPJ6VX53L
git add . // added files to stage area (stage area te gelei green hoy, unstated red)
git commit // Store what content in last stage area
git add a.html // Added to stage arae if we now again modify file not run git add a.html and commit then it will save content before second modification
git status -s // short https://prnt.sc/2KdzsfURr71n
git commit -a -m "add & commit" // Skeeping staging area. add+commit
git checkout index.html // Back to last commit
git checkout -f // Back to last commit all files
git log -p -1 // See one commit; q to exit from git log
git diff // stage area and working tree difference
git diff --staged // stage and last commit difference
git rm --cached waste.html // remove from stage area, but file reamain as untrack file
git rm --f waste.html // Remove stage area + Delete File; --f to force removal
```


************* VS Code ******************************************************
https://www.youtube.com/watch?v=2oihkInZ880 (Hindi)
1st time step: -----(Local: 1-3, Remote: a-d)--------------

1. Initialize Repository // https://prnt.sc/V7oDXeeOi9CO
2. Commit // Visually Commit
3. COnfig Git(If ask)

a. Add Remote // Visually Commit https://prnt.sc/-IWSFNeadc1H
b. Push // Commit and push option ase vscode
c. Github Auth
d. Push Again (If required)

2nd Time (Old Project):

1. Pule (clone) // https://prnt.sc/K2us0_eYZFuq
2. Commit

a. Push

### https://github.com/ajit-dherange/Git_Examples
