## How to work with rebase in git:

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
