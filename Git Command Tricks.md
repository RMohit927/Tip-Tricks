## Basic Git Commands:
----------------------

1. Get the current config Git Username and Email ID
```
git config --global --get user.name
```
```
git config --global --get user.email
```

2. Set the Username/Email to the git
```
git config --global user.name "xyz999"
```
```
git config --global user.email "xyz@gmail.com"
```

3. Check whether the user.name has set or not?
```
git config user.name
```
```
git config user.email
```

4. checking git version
```
git --version
```

5. Create git configuration file for user.name/Email
```
git config --global -e
```
Steps:
a. first click i for made any changes on it
b. after made changes click on Esc key.
c. After click ":wq" and then Enter

6. For initialize repository
```
git init
```

7. For View the status for how many file committed or how many are not
```
git status
git status -s
```

8. Remove everyfile 
```
rm -rf *
```

9. Adding All files to the git repo
```
git add .
```

10. Commentting the file which we have added
```
git commit -m "give comment"
```

11. Creating the gitignore file so while doing push operation that file will be not push to git repo
```
echo logs/ > .gitignore
```

12. open gitignore file and add some commands
```
code .gitignore
```



## How to work with rebase in git:
----------------------------------

- git log --graph --oneline
```
git pull
git checkout -b feature: branch
```
- add some commit - 
- now fellow developer add some into master branch
```
git checkout master
git pull
```
- now my feature branch is upto date
```
git checkout feature
git rebase master
```
- if no conflict
```
git checkout master
git rebase feature
git push
```
