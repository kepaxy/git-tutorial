#4.1
mkdir git-tutorial
cd git-tutorial
git init
git status
touch README.md
git status
git add README.md
git status
git commit -m "First commit"
git commit
git status
git log
git log --pretty=short
git log README.md
git log -p
git log -p README.md
vim README.md
git diff
git add README.md
git diff HEAD
git commit -m "Add index"
git log

#4.2
git branch
git checkout -b feature-A
- git branch feature-A; git checkout feature-A
git branch
vim README.md
git add README.md
git commit -m "Add feature-A"
git checkout master
cat README.md
git checkout -
cat README.md
git checkout master
git merge --no-ff feature-A
git log --graph

#4.3
git reset --hard ea11
git checkout -b fix-B
vim README.md
git add README.md
git commit -m "Fix B"
git reflog
git checkout master
git reset --hard 9cbff
git merge --no-ff fix-B
vim README.md
git add README.md
git commit -m "Fix conflict"
git commit --amend
a Merge branch 'fix-B'
git checkout -b feature-C
vim README.md
git commit -am "Add feature-C"
!vim
git diff
git commit -am "Fix typo"
git rebase -i HEAD~2
cw fixup
git log --graph
git checkout master
git merge --no-ff feature-C

#4.4
リモートリポジトリ「git-tutorial」作成	作成すると駄目！
git remote add origin git@github.com:kepaxy/git-tutorial.git
git push -u origin master
ライセンスファイルを作ったせいか失敗する	リモートを作成しておくと失敗する，削除しておくこと
git checkout -b feature-D
git push -u origin feature-D

#4.5
cd ../..
mkdir Git2
cd Git2
git clone git@github.com:kepaxy/git-tutorial.git
cd git-tutorial
git branch -a
git checkout -b feature-D origin/feature-D
vim
git commit -am "Add feature-D"
git push
cd ../../Git/git-tutorial/
git pull origin feature-D

