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

7. Add new file (notTrackedFile.txt) - editing commit after push will make a second commit in history

*run check command
git add -A
git commit --amend
*run check command

run: git pull (git fetch + git merge -> maybe you will have to edit manually conflicts in files, just only leave content you want)
you must commit conflicts (merge), use: git commit
now: git push

*run check command

8. Untrack file notTrackedFile.txt:

git rm --cached notTrackedFile.txt
*run check command (file exist in folder but is untracked)

git rm notTrackedFile.txt
*run check command (file not exist in folder, is deleted and untracked)

git commit -m "Commit after push"
git push

9. Create second local folder, where you will put cloned project:

git clone https://github.com/rKow/gitTutorial.git

10. Add line "From first local folder" to file myFile.txt from first clone
Add line "From second local folder" to file myFile.txt from second clone
