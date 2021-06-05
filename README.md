# Learning-Git

#1st Issue: When create a repo with README file
-- **Root cause**: because README file is a new file and not present in our local repo
-- **Problem**: [rejected]
	error: failed to push some refs to 'https://github.com/KimThanh1998/Learning-Git.git'
	hint: Updates were rejected because the tip of your current branch is behind
	hint: its remote counterpart. Integrate the remote changes (e.g.
	hint: 'git pull ...') before pushing again.
	hint: See the 'Note about fast-forwards' in 'git push --help' for details.
-- **Solve**: 
	git pull origin master --allow-unrelated-histories
	git pull origin master
	git push -u origin master

#2nd Issue: Conflict when updating same line
-- **Root cause**: When more than two people working on the same files, occasionally they change the same line with different contents.
-- **Problem**: CONFLICT (content): Merge conflict in xxx.xxx 
Automatic merge failed; fix conflicts and then commit the result.
-- **Solve**: 
	git pull orgin master
	sudo gedit xxx (file conflict -> fix conflict manually by choosing head or local, or reconstruct)
	git add xxx
	git commit 
	git push
	
#3rd Issue: Working with branch
-- **Procedure**:
	git checkout -b <name> (create and checkout new branch)
	git add <file>
	git commit
	git push --new-upstream origin <branch>
	
#4th Issue: Merge with master branch
-- **Procedure**:
	git checkout master (change code back to origin)
	git merge <branch>
