```git
git stash //Remove all changes
git pull //Get all files from this branch
```

▼ **Initialization of git** ▼
```git
cd monDossier
git init
git add --all
git commit -m "Titre de la Save" -m "Description de la Save"
```


▼ **Check commits, create new branch** ▼
```git
git log (--all) // See all saves
git checkout xxxxxxxxxxxx (commit's code) // Change from save to save
git checkout -b // create a new branch	
git switch -c "newBranch" // Create new branch
git switch // switch to another branch
```
▼ **Merge** ▼
```git
git merge "the branch to take into the one I'm" // fusionne les 2 branches
```

▼ **Basic commands** ▼
```git
git init 
git add --all
git commit -m "new commit"
git branch Dev1
git checkout Dev1
```
	
### …or create a new repository on the command line
```git
echo "# testOne" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:NiakaGaming/testOne.git
git push -u origin master      

```
### …or push an existing repository from the command line
```git
git remote add origin git@github.com:NiakaGaming/testOne.git
git push -u origin master
```


<!--stackedit_data:
eyJoaXN0b3J5IjpbOTY0MzA1NjQ1XX0=
-->