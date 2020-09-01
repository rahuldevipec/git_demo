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


-- git merge using command and then delete the feature branch
metlifedevops21@metlifed25 MINGW64 ~/git_demo (feature)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git branch
  feature
* master

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git branch --merged
* master

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git merge feature
Updating 78cde97..7cd80c7
Fast-forward
 readme.md | 11 +++++++++++
 1 file changed, 11 insertions(+)

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git push -u origin master
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/rahuldevipec/git_demo.git
   78cde97..7cd80c7  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git branch -a
  feature
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/feature
  remotes/origin/master

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git branch -d feature
Deleted branch feature (was 7cd80c7).

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/feature
  remotes/origin/master

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git push --delete feature
fatal: --delete doesn't make sense without any refs

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git push origin --delete feature
To https://github.com/rahuldevipec/git_demo.git
 - [deleted]         feature

metlifedevops21@metlifed25 MINGW64 ~/git_demo (master)
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
