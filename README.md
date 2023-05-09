# Git_Examples
**Git Practice Examples for DevOps Engineer**

Quick setup — if you’ve done this kind of thing before
https://github.com/xxxxx/Test_Repo.git

…or create a new repository on the command line
```
  echo "# Test_Repo" >> README.md
  git init
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin https://github.com/xxxxx/Test_Repo2.git
  git push -u origin main
  ```
  
…or push an existing repository from the command line
```
git init
git config --global user.name "xxxxx"
git config --global user.email "xxxxxe@gmail.com"
touch f2.txt
git add .
git commit -m "a"
git remote add origin https://github.com/xxxxx/Git_Test.git
git push -u origin main / master (**first time only**)
touch f3.txt
git status
git add .
git commit -m "b"
git push 
```
