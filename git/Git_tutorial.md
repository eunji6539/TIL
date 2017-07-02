
Git Tutorial Summary
=============
>[GitTutorial](https://try.github.io/levels/1/challenges/1).



### 1.1. git init
Initialize a Git repository here
octobox 폴더 내에 /.git/ 내에서 empty repository 를 가지고 있음. 
/.git/은 hidden directory

### 1.2. git status
현재의 project 의 status 를 보여줌

### 1.3. git add octocat.txt
로컬에서 새로 생겼으므로 아직 untracked
**Tracking** 하도록 하려면 **git add** 를 이용하여 **staging area** 에 octocat.txt 를 추가해야 함.

### 1.4. git commit -m "Add cute octocat story"
**Staging Area**에 있지, 아직 repository 에 존재하지 않음. Repository 에 올리기 전 add 하거나 remove 가능.
**Commit** 을수행하여 repository 에 올림.
m 이후에 있는 글은 변경한 이유를 서술한 것.

### 1.5. git add '*.txt'
같은 type 의 여러 파일들을 한 번에 add 하기 위해 필요.

### 1.6. git commit -m 'Add all the octocat txt files'
올린 모든 파일을 commit

### 1.7. git log
어떤 것들을 변화(commit)시켰었는지 확인 가능.

### 1.8. git remote add origin https://github.com/try-git/try_git.git
Local repo 에서 GitHub server 로 올리기 위해 remote repository 를 추가함.
이름이 origin

### 1.9. git push -u origin master
**push** command 는 git 에 우리의 commit 들이 어디에 있는지 알려줌. 우리의 local change 를 origin repo(github) 로 **push**
**master** 는 default local branch
**-u** 를 이용하여 **git push** 뒤에 들어가야하는 parameter 를 다음부터는 안써도 되게 만듦

### 1.10. git pull origin master
Origin 에서 다른 사람이 변화시킨 부분을 Local repo 로 받아옴?

### 1.11. git diff HEAD
마지막 commit과 현재의 차이를 확인. HEAD pointer 이용

### 1.12. git diff --staged
staged file 에서도 차이를 확인해볼 수 있음

### 1.13. git reset octofamily/octodog.txt
unstage 로 만듦

### 1.14. git checkout -- octocat.txt
octocat.txt 에 대한 마지막 commit 상태일 때로 전체 변화를 돌림.

### 1.15. git branch clean_up
feature 이나 bug 에 대해 work 할 때 copy (**branch**)를 만들기도 함
**master** 가 가장 main 인 branch
수정이 완료되면 나중에 **master** 와 **copy** 가 merge 되기도 함.
우선은 clean_up 이라는 branch 를 형성

### 1.17. git branch
어떤 branch 가 있는지와, 현재 상태의 git branch를 알 수 있음(지금은 master 일듯)

### 1.16. git checkout clean_up
branch 를 clean_up 으로 switching

### 1.17. git rm '*.txt'
disk 와 stage 의 모든 파일을 제거함.
(적용하려면 commit 을 수행하여야함)

### 1.18. git checkout master
우선 git checkout master 를 통해 clean_up branch에서 master branch 로 돌아가고 그 이후 변화를 master 로 copy(mergy)하여 master branch 에 적용함.

### 1.19. git merge clean_up
clean_up 에서 수행하였던 작업을 master 에 merge 함.

### 1.20. git branch -d clean_up
branch 를 delete

### 1.21. git push
origin 에 해당 내용을 적용함.
(왜 마지막에 yellow_octocat.txt 가 남을까?)

> Written with [StackEdit](https://stackedit.io/).
