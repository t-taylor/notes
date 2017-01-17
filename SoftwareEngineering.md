Software Engineering

#16/01/17

Load of stuff about git.....

```sh
git diff
#Shows difference between all different commits
git reset --hard c724e12 
#cleans history so it looks like there was never a mistake
git reset --soft c724e12
#You know, just google this shit
```

##Branches

In order not to mess up the trunk (master) while you're working in a repo
create a branch to work in while you're working on the code
```sh
git branch feature
#Creates new branch called feature
git checkout feature
#Switches local repo with the feature branch
```
