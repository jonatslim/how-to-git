#Notes
#makes changes in the windows folder and upload all results into the repo.
#1 init git on this folder
	git init
2 add all the files and folder into the git
	git add .
3 commit the "add" into git
    git commit -m "first commit"

#4 declare the branch of this files in git
git branch -M main

#5 declare the remote repo where this files are stored.
git remote set-url origin https://github.com/jonatslim/9800-WLC-Monitoring.git

#6 push all the files into git repo.
git push -u origin main

-----------------------------------
# confirm git is installed. If not installed, download git from https://git-scm.com/downloads
	git --version
# go to the folder with the files you want to "track - upload"
	cd existing_folder
# initiate a git instance 
	git init
# add a remote repository.
	git remote add origin https://gitlab-sjc.cisco.com/jonglim/nccm---gic.git
# add all the files in the directory to the staging area
	git add .
# alternatively, you can add single file ..
	git add "Cisco Nexus 3000.xlsx"
# display status
	git status
# save all changes to the staging area.
	git commit -m "type comments about the commit here!"
# at this point, all files + Cisco Nexus 3000.xlsx are in the staging area.
# sync all files in the staging area to remote repo
	git push

# to chnage the remote repo destination/source
	git remote set-url origin https://gitlab-sjc.cisco.com/jonglim/nccm---gic.git
# show what it the remote repo details after change.
	git remote show origin
# show all the commits done to the staging area.
	git log --all --decorate --oneline --graph
# checkout a specific #head. this is usefull after a git pull. head hash came from git log output.
	git checkout <head_hash>
# other usefull commands:
	git show
	git diff
	git rm "Cisco Nexus 3000 Series Switches v1.3.xlsx"
	git push
	git fetch
# Existing Git repository (don't konw wth this will do just yet...)
	cd existing_repo
	git remote rename origin old-origin
	git remote add origin https://gitlab-sjc.cisco.com/jonglim/nccm---gic---audit-policy.git
	git push -u origin --all
	git push -u origin --tags
# When password is changed, update it on the git local file
git config --edit
<then update the password...>
