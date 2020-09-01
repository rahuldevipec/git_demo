-- initial git setup
git init
git status
git add main.tf
git status
git log
git commit -m "initial commit"
git log
git config --global user.name "rahul"
git config --global user.email "rahuldevipec@gmail.com"
git branch
git remote add origin https://github.com/rahuldevipec/git_demo.git
git branch -M master
git push -u origin master
git status

-- branching
git branch
git branch feature
git branch
git checkout feature
git branch
git push -u origin feature
git status

