## Basic commands in Git

##### first run git status to see the status of the working dir
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

##### run git log to see the if any changes are done
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git log
fatal: your current branch 'master' does not have any commits yet

##### create a test.txt file
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ touch test.txt

##### run git status 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	./

nothing added to commit but untracked files present (use "git add" to track)

##### run git add and git status to see changes in working repo
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git add test.txt 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   test.txt

##### commit the changes 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git commit -m "created test.txt empty file"
[master (root-commit) 2234024] created test.txt empty file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Basic Commands/test.txt
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master
nothing to commit, working tree clean

##### modify the contents of the file and then check the status
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ nano test.txt 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   test.txt

no changes added to commit (use "git add" and/or "git commit -a")

##### add the changes to stagging area and then check the status
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git add test.txt 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   test.txt


##### again change the contents of the file, add to stagging area and commit the changes done to the file
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ nano test.txt 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git add test.txt 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git commit -m "file changed for first time"
[master 6329ecd] file changed for first time
 1 file changed, 2 insertions(+)
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master
nothing to commit, working tree clean

##### check for git log after performing commit operation
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git log
commit 6329ecdea66bb657b5a2905da0a2d3ee43750196 (HEAD -> master)
Author: azeem <mohd.abazeem@gmail.com>
Date:   Thu Jan 20 16:08:25 2022 +0530

    file changed for first time

commit 22340240a324a2a204867de3962d35af05c259b1
Author: azeem <mohd.abazeem@gmail.com>
Date:   Thu Jan 20 16:06:44 2022 +0530

    created test.txt empty file


##### again modify the contents of the file, check for the status of the dir, add to stagging area and commit the changes
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ nano test.txt 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   test.txt

no changes added to commit (use "git add" and/or "git commit -a")
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git add test.txt 
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   test.txt

(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git commit -m "file changed for second time"
[master 6ad258d] file changed for second time
 1 file changed, 1 insertion(+)

##### check the status now after 3 commits
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git status
On branch master
nothing to commit, working tree clean
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git log
commit 6ad258d75370d24568de9a7e8cabcf84561d8423 (HEAD -> master)
Author: azeem <mohd.abazeem@gmail.com>
Date:   Thu Jan 20 16:09:18 2022 +0530

    file changed for second time

commit 6329ecdea66bb657b5a2905da0a2d3ee43750196
Author: azeem <mohd.abazeem@gmail.com>
Date:   Thu Jan 20 16:08:25 2022 +0530

    file changed for first time

commit 22340240a324a2a204867de3962d35af05c259b1
Author: azeem <mohd.abazeem@gmail.com>
Date:   Thu Jan 20 16:06:44 2022 +0530

    created test.txt empty file

##### If you want to see the message only, run the below command
(base) azeem@azeem:~/Zemoso/Git Tasks/Basic Commands$ git log --oneline
6ad258d (HEAD -> master) file changed for second time
6329ecd file changed for first time
2234024 created test.txt empty file

