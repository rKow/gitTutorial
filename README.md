GitTutorial


Instruction:

*Check command: git status, gitk. 


/******************* LEVEL 1: Creating repo, adding files, editing commit, pushing commit *******************/

1. Create git repository on server
2. In local folder, where you want to keep your project files via command line:
touch README.md // fill the file
touch .gitignore // fill the file, example: *~
touch add myFile.txt
git init
git add README.md
git add .gitignore
git add myFile.txt
git commit -m "First commit"
git remote add origin https://github.com/rKow/gitTutorial.git

*run check command

4. Edit file myFile.txt. 
*run check command - Commit must be edited before push, so run command:

git add myFile.txt (or for all modified files: git add -A )
git commit --amend // leave comment with no modification

*run check command

5. Change the comment of the commit (new comment: "First commit (renamed)"):
git commit --amend -m "First commit (renamed)"

*run check command

6. Push the files on the server:
git push -u origin master (or git push)

7. Add new file (notTrackedFile.txt) - edit commit after push

*run check command
git add -A
git commit --amend
*run check command

git pull (git fetch + git merge -> maybe you will have to edit manually conflict in files, just only leave content you want)

8.

 

