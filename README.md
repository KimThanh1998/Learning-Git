# Learning-Git

#1st Issue: When create a repo with README file
-- Root cause: because README file is a new file and not present in our local repo
-- Problem: [rejected]
	error: failed to push some refs to 'https://github.com/KimThanh1998/Learning-Git.git'
	hint: Updates were rejected because the tip of your current branch is behind
	hint: its remote counterpart. Integrate the remote changes (e.g.
	hint: 'git pull ...') before pushing again.
	hint: See the 'Note about fast-forwards' in 'git push --help' for details.
--Solve: 
	git pull origin master --allow-unrelated-histories
	git pull origin master
	git push -u origin master

#2nd Issue: Conflict when updating same line
