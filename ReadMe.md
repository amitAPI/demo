git init demo -- will create new repository

Local git states
 
1. Working Directory --> (This contains all files and folder of your application. Which may or may not managed by git; either way git is aware of those files.)
2. Staging Area  --> This is between two. It is the area which is preapared for next commit. Files are  moved from the working directory state to the git staging area and then finally committed to the git repository.
3. Repository /commit history (.git folder) --> It contains all committed or saved changes to git repository . ANything here is part of git history .


4. Remote


$ mate Readme.md  (for creating a file)

$ git status  (for )

$ git add Readme.md  (It adds file into staging area from working directory)

$ git commit -m "First file in demo repo"

5. Inner working of git
----------------------------

rm -rf .git (To remove forcefully git folder which is for version contol)

Git History
------------

git log

git show

git ls-files (will show tracking file details)

git commit -a (which tells first add modified files to the staging area and then directly proceed to commiting.)
git commit -am "Updating readme " (This coomand also adds message)

git add . (for adding into staging area)

Backing out
----------
git reset HEAD <File to be unstaged>

git checkout -- <File to be fresh as working in git >


Renaming and deleting files
----------------------------

git mv <files to changed> <files name into changed>

git rm <files to deleted>

git commiting -m 'deleting demo file';


-----------------------------
Ignoring files which we dont to be tracked by git
--------------------------------------------------

mate .gitignore  then write the files name which you want to exclude

git add .gitignore
git commit -m "Adding ignore files"


git diff <commit1> HEAD

git difftool <commit1> HEAD
----------------------------------
Branch = Timeline of Commits
------
Branch names are labels 
Deletion removes label only

Merging 
=======
1. Fast Forward
   Simplest Case
   Like Never Branched(Commits on destination)
   Can be disabled
   
2. Automatic
   Non-Conflicting merge detected
   Preserves both Timelines
   Merge COmmit on Destination
   
3. Manula Merge
   Automatic Merge Not Possible
   Conflicting Merge state
   Changes Saved in merge Commit
   

Special Markers
 * Like "Pointers"
 * HEAD
       * Points to Lats Commit of Current branch
       * Can be Moved (Advanced)


git branch (List all branch)

git checkout -b updates (It craete new branch updates and switch to new branch)	  

git branch -a (SHow all branch list)

git tag mytag (Create new tag)

git tag --list (List all tag) 

git tag -d mytag (to delete a tag)

git tag -a v1.0 -m "Release 1.0"

---------
Stashing
---------

-----------------
Resetting
-------------
1. Soft -least destructive (git reset commit-id --soft)
2. Mixed - 
3. Hard - More destructive

************************GitHub**************************
git remote -v (If this cmd outputs empty it means we do not hav any remote set)

git remote add <alias if you want> https://<url of remote repo>

git push -u origin master --tags


SSH AUthentication
-------------------
  why ?
   Saves time
   
Difference between SSH and Https authentication ?

1. In https you are prompted each time in anyactivity with remote.

Setup SSH on Github
--------------------
1. create SSH key on loacl system.
    -->
    mkdir .ssh
    cd .ssh
    ssh-keygen -t -rsa -C "amit.amitkumar2@gmail.com"
	follow the guidelines.
	--
	For confirming all done correctly
	ssh -T git@github.com
    	
   


