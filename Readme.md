# git assignment
<br>

## git add
This command __stages changes__ , making them ready for commit

### git add file1.txt
Stage a single file ___file1.txt__
```
PS C:\Users\acer\Desktop\git_assign> git add file1.txt
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        new file:   file1.txt

Changes not staged for commit:
  (use "git add "file"..." to update what will be committed)
  (use "git restore "file"..." to discard changes in working directory)
        modified:   Readme.md
```

### git add file1.txt file2.txt
Stages multiple files __file1.txt__ && __file2.txt__
```
PS C:\Users\acer\Desktop\git_assign> git add file1.txt file2.txt
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        new file:   file1.txt
        new file:   file2.txt

Changes not staged for commit:
  (use "git add "file"..." to update what will be committed)
  (use "git restore "file"..." to discard changes in working directory)
        modified:   Readme.md
```

### git add -A
stages all changes in the entire repository
```
PS C:\Users\acer\Desktop\git_assign> git add -A
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file2.txt
```

### git add -u
stages all changes but does not add new files
```
PS C:\Users\acer\Desktop\git_assign> git add -u
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file2.txt

Untracked files:
  (use "git add "file"..." to include in what will be committed)
        file3.txt
```

### git add .
stages new files and modifications
```
PS C:\Users\acer\Desktop\git_assign> git add .
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file3.txt
```


### git add *.txt
Stages all content from *.txt files
```
PS C:\Users\acer\Desktop\git_assign> git add *.txt
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file2.txt
        new file:   file3.txt

Changes not staged for commit:
  (use "git add "file"..." to update what will be committed)
  (use "git restore "file"..." to discard changes in working directory)
        modified:   Readme.md
```
<br>

## git status
It shows state of the working directory and the staging area.
```
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file2.txt
        new file:   file3.txt

Changes not staged for commit:
  (use "git add "file"..." to update what will be committed)
  (use "git restore "file"..." to discard changes in working directory)
        modified:   Readme.md
```
<br>

## git diff
Show changes between commits, commit and working tree
```
PS C:\Users\acer\Desktop\git_assign> git diff
diff --git a/Readme.md b/Readme.md
index 33fb511..11da29b 100644
--- a/Readme.md
+++ b/Readme.md
@@ -111,6 +111,28 @@ Changes not staged for commit:
   (use "git restore "file"..." to discard changes in working directory)
         modified:   Readme.md
 
+<br>
+
+## git status
+It shows state of the working directory and the staging area.
+
+PS C:\Users\acer\Desktop\git_assign> git status
+On branch main
+Your branch is up to date with 'origin/main'.
+
+Changes to be committed:
+  (use "git restore --staged "file"..." to unstage)
+        modified:   Readme.md
+        new file:   file1.txt
+        new file:   file2.txt
+        new file:   file3.txt
+
+Changes not staged for commit:
+  (use "git add "file"..." to update what will be committed)
+  (use "git restore "file"..." to discard changes in working directory)
+        modified:   Readme.md
+
+
```

### git diff --cached
It shows difference between staging area and last commit

```
PS C:\Users\acer\Desktop\git_assign> git diff --cached
diff --git a/Readme.md b/Readme.md
index 33fb511..7f64649 100644
--- a/Readme.md
+++ b/Readme.md
@@ -111,7 +111,34 @@ Changes not staged for commit:
   (use "git restore "file"..." to discard changes in working directory)
         modified:   Readme.md
 
+<br>
+
+## git status
+It shows state of the working directory and the staging area.
+
+PS C:\Users\acer\Desktop\git_assign> git status
+On branch main
+Your branch is up to date with 'origin/main'.
+
```

### git diff HEAD
shows the differences between the working directory and the last commit.

```
PS C:\Users\acer\Desktop\git_assign> git diff HEAD
diff --git a/Readme.md b/Readme.md
index 6c536ba..210a68d 100644
--- a/Readme.md
+++ b/Readme.md
@@ -194,5 +194,7 @@ index 33fb511..7f64649 100644
 +

+### git diff HEAD
+shows the differences between the working directory and the last commit.

```

### git diff 'commit1' 'commit2'
This command shows the differences between two specific commits.
```
 git diff 497ecf18b4ea10f13f0ba0db63fb0757119d8732 667beda7fb1a8b604f087b0ba39d884cc529daf1
diff --git a/Readme.md b/Readme.md
index 6c536ba..33fb511 100644
--- a/Readme.md
+++ b/Readme.md
@@ -111,88 +111,7 @@ Changes not staged for commit:
   (use "git restore "file"..." to discard changes in working directory)
         modified:   Readme.md

-<br>
-
-## git status
-It shows state of the working directory and the staging area.
-
-PS C:\Users\acer\Desktop\git_assign> git status
-On branch main
-Your branch is up to date with 'origin/main'.
-
```

### git diff --stat
This command provides a summary of changes, showing the number of insertions and deletions per file.

```
PS C:\Users\acer\Desktop\git_assign> git diff --stat
 Readme.md | 39 +++++++++++++++++++++++++++++++++++++++
 1 file changed, 39 insertions(+)
```

<br>

## git commit
It records changes to repo

### git commit -m "message"
This command commits staged changes with a descriptive message.
```
 git commit -m "5: commit commands"
[main ab4f701] 5: commit commands
 4 files changed, 12 insertions(+), 3 deletions(-)
```

### git commit --amend -m "Updated message"
This modifies the last commit, including updating the commit message or adding new changes.
```
 git commit --amend -m "5.1: updated commit message commit" 
[main a356a1d] 5.1: updated commit message commit
 Date: Fri Jun 21 00:59:44 2024 +0530
 4 files changed, 12 insertions(+), 3 deletions(-)
 ```

<br>

## git notes
Add or inspect object notes

### git notes -m "note message" 'commit'
adds note to commit

```
git notes add -m "redundant commit" 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
```

### git notes list
it gives all notes in the repo
```
PS C:\Users\acer\Desktop\git_assign> git notes list
02de2541005af2779c152bc52292bd4e91057001 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
43a65668771a41ec76366be09c20582036b503dd ee697e0b348a7faf337caf0df371835d52ee1ce5
```

### git notes show 'commit'
to view the note

```
PS C:\Users\acer\Desktop\git_assign> git notes show 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
redundant commit
```

### git notes append -m "Additional note" 'commit'
it add to additional notes to commit

```
PS C:\Users\acer\Desktop\git_assign> git notes append -m "test" 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
PS C:\Users\acer\Desktop\git_assign> git notes show 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
redundant commit

test
```

### git notes remove 'commit'
to remove note from a commit

```
PS C:\Users\acer\Desktop\git_assign> git notes list
02de2541005af2779c152bc52292bd4e91057001 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
43a65668771a41ec76366be09c20582036b503dd ee697e0b348a7faf337caf0df371835d52ee1ce5
PS C:\Users\acer\Desktop\git_assign> git notes remove 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
Removing note for object 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
PS C:\Users\acer\Desktop\git_assign> git notes list
43a65668771a41ec76366be09c20582036b503dd ee697e0b348a7faf337caf0df371835d52ee1ce5
PS C:\Users\acer\Desktop\git_assign>
```

<br>

## git restore
it is used to restore working tree files.


### git restore file
it is used to restore the specified file to the state of the last commit.
```
PS C:\Users\acer\Desktop\git_assign> git restore file3.txt
```

### git restore file1 file2
it is used to restore multiple files to the state of the last commit.
```
git restore file1.txt file2.txt
```

### git restore --staged file
This command is used to unstage a file
```
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        modified:   Readme.md
        modified:   file3.txt

PS C:\Users\acer\Desktop\git_assign> git restore --staged .
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add "file"..." to update what will be committed)
  (use "git restore "file"..." to discard changes in working directory)
        modified:   Readme.md
        modified:   file3.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

### git restore --source 'commit'
 "file"
This restores a file to the state it was in a specific commit.
```
PS C:\Users\acer\Desktop\git_assign> git restore --source a356a1dbfb6a04aca02fffea84f7331fe1c20c28 file1.txt
```


<br>

## git restore --'mode' 'commit'

It is used to undo changes by resetting the current branch to a specified state.


### git reset --soft 'commit'

This mode resets the HEAD to the specified commit but leaves the staging area and working directory unchanged.
```
 git reset --soft HEAD~1
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged "file"..." to unstage)
        modified:   Readme.md
        modified:   file3.txt

Changes not staged for commit:
  (use "git add "file"..." to update what will be committed)
  (use "git restore "file"..." to discard changes in working directory)
        modified:   Readme.md

```

### git reset --mixed 'commit'

This mode resets the HEAD to the specified commit and updates the staging area to match the commit, but leaves the working directory unchanged.
```
git reset --mixed HEAD~1
Unstaged changes after reset:
M       Readme.md
M       file3.txt
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes not staged for commit:
  (use "git add "file"..." to update what will be committed)
  (use "git restore "file"..." to discard changes in working directory)
        modified:   Readme.md
        modified:   file3.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

### git reset --hard 'commit'

This mode resets the HEAD to the specified commit and updates both the staging area and working directory to match the commit.
```
 git reset --hard HEAD~1 
HEAD is now at 4fab482 5.4: Commleted commit
PS C:\Users\acer\Desktop\git_assign> git status
On branch main
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

nothing to commit, working tree clean
```

<br>

## git rm
remove files from working directory
```
PS C:\Users\acer\Desktop\git_assign> ls


    Directory: C:\Users\acer\Desktop\git_assign


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         6/21/2024   2:56 AM             10 file1.txt
-a----         6/21/2024   2:34 AM             22 file3.txt
-a----         6/21/2024   2:54 AM          12736 Readme.md


PS C:\Users\acer\Desktop\git_assign> git rm file3.txt
rm 'file3.txt'
PS C:\Users\acer\Desktop\git_assign> ls


    Directory: C:\Users\acer\Desktop\git_assign


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         6/21/2024   2:56 AM             10 file1.txt
-a----         6/21/2024   2:54 AM          12736 Readme.md
```
<br>

## git mv
It is used to rename and move a file


### git mv oldname newname
rename a file
```
PS C:\Users\acer\Desktop\git_assign> git mv FILE.txt file4.txt
```

### git mv file4 folder1/
move a file to differend directory

<br>

### git checkout 'branch-name'
This command switches your working directory to the specified branch.
```
 git checkout main   
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```

### git checkout -b new-branch-name
create and switch to new branch
```
PS C:\Users\acer\Desktop\git_assign> git checkout -b new-branch-name
Switched to a new branch 'new-branch-name'
```

<br>

## git switch
it is used to switch branches


### git switch branch-name
switch to specific branch
```
PS C:\Users\acer\Desktop\git_assign> git branch        
  branch1
  branch2
* main
  new-branch-name
PS C:\Users\acer\Desktop\git_assign> git switch branch1
Switched to branch 'branch1'
PS C:\Users\acer\Desktop\git_assign> git branch        
* branch1
  branch2
  main
  new-branch-name
```

### git switch -c branch-name
Creates a new branch and sitches to it
```
PS C:\Users\acer\Desktop\git_assign> git branch
  branch1
  branch2
* main
  new-branch-name
PS C:\Users\acer\Desktop\git_assign> git switch -c branch3
Switched to a new branch 'branch3'
PS C:\Users\acer\Desktop\git_assign> git branch
  branch1
  branch2
* branch3
  main
  new-branch-name
```

<br>

## git merge 
This command is used to integrate changes from different branches.


### git merge branch-name
this command is used to merge changes into current branch

```
PS C:\Users\acer\Desktop\git_assign> git checkout branch1
Switched to branch 'branch1'
PS C:\Users\acer\Desktop\git_assign> git add .           
PS C:\Users\acer\Desktop\git_assign> git commit -m "14.1 : Temporary changes for merge command"
[branch1 a9620f3] 14.1 : Temporary changes for merge command
 1 file changed, 1 deletion(-)
 delete mode 100644 folder1/file4.txt
PS C:\Users\acer\Desktop\git_assign> git push origin branch1
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (1/1), done.
Writing objects: 100% (2/2), 265 bytes | 265.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Murshid652/Git_Assignment.git
   e9e02f8..a9620f3  branch1 -> branch1
PS C:\Users\acer\Desktop\git_assign> git checkout branch2
Switched to branch 'branch2'
PS C:\Users\acer\Desktop\git_assign> git merge branch1
Updating e9e02f8..a9620f3
Fast-forward
 folder1/file4.txt | 1 -
 1 file changed, 1 deletion(-)
 delete mode 100644 folder1/file4.txt
PS C:\Users\acer\Desktop\git_assign> git push origin branch2
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Murshid652/Git_Assignment.git
   e9e02f8..a9620f3  branch2 -> branch2
```

<br>

## git log 
this command is used to get commit history of repo

```
PS C:\Users\acer\Desktop\git_assign> git log
commit dafee0c512c7441af29e580f2f013f60190312bf (HEAD -> main, origin/main)
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 10:22:01 2024 +0530

    12.3 : updating git checkout command

commit 0c04e8f2feb0efadbe1299f111864fcb3d039e22
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 10:09:49 2024 +0530

    14: git merge commands

commit 217bc2988d3de0159664015a57aeaf303aebc3ca
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 09:52:50 2024 +0530

    13.1: git switch commands

commit c3a71a3e824e299590fe404c19ab8423287fdfb3 (branch3)
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 03:57:58 2024 +0530

    12.2: checkout command (create and switch to branch)

commit be1e4ecff1136feae1bdcb6f66ca548a3fc80e02 (new-branch-name)
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 03:51:00 2024 +0530

    12.1: checkout command

commit e20fb079878ff7ad2dc753c009e3b98b268dfbcb
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 03:34:50 2024 +0530

    11: git branch command

commit e9e02f8b9b6341906d5cd871c2566ace545db091
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 03:18:53 2024 +0530

    10: git mv command

commit c4a38b53560357e51b8073c0460ca1ce901b674b
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 03:01:28 2024 +0530

    9: git rm command

commit 44689088a98e0742db59afd62a150c6021154625
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 02:41:14 2024 +0530

    8: git restore commands

commit fe16926fb721afa3773e3e405e56c554b1636c2b
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 02:26:13 2024 +0530

    7: git restore commands

commit a9a80d8feaf3dbf8882137a0a4c15d54f995cc25
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 01:54:25 2024 +0530

    6: Git notes commands

commit ee697e0b348a7faf337caf0df371835d52ee1ce5
Merge: 4fab482 191f986
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 01:27:40 2024 +0530

    5.4: Commleted commit

Notes:
    redundant commit and spelling mistake

commit 4fab4825f8773975b0278aa5ef08e4f5ceb52a13
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 01:25:43 2024 +0530

    5.4: Commleted commit

commit 191f986d86e276bb1a29bd00ce5e0d5792fc3e9c
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 01:12:15 2024 +0530

    5.3: updated commit message

commit 79b96e04b23c0b93f43a9ed3bfe440d8f006fbb6
Merge: 0d6480a a356a1d
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 01:09:07 2024 +0530

    5.2: updated commit message

commit 0d6480a89d20d80b1dba060927bd7f95b8522d66
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 00:59:44 2024 +0530

    5.2: updated commit message

commit a356a1dbfb6a04aca02fffea84f7331fe1c20c28
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 00:59:44 2024 +0530

    5.1: updated commit message commit

commit f73e4fab25ba8012d688eea8be89e731e2e8d22c
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 00:48:08 2024 +0530

    4: git diff command

commit 497ecf18b4ea10f13f0ba0db63fb0757119d8732
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 00:38:06 2024 +0530

    3: git status command

commit 667beda7fb1a8b604f087b0ba39d884cc529daf1
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 00:00:35 2024 +0530

    2.1 : Retry git add commands

commit 392590750dccce5dfc431edad580f5e6c8e94765
Author: Murshid Raja <murshidraja652@example.com>
Date:   Thu Jun 20 23:59:09 2024 +0530

    2: git add commands

commit d79d6d8cca12f5761c44e965e27d35316501dead
Author: Murshid Raja <murshidraja652@example.com>
Date:   Thu Jun 20 23:08:15 2024 +0530

    first commit
```

<br>

## git stash
saves uncommited changes while switching to other branch
```
PS C:\Users\acer\Desktop\git_assign> git stash
Saved working directory and index state WIP on main: 5e5738a 15: git log command
```


### git stash list
shows list of stashes saved
```
 git stash list
stash@{0}: WIP on main: 5e5738a 15: git log command
stash@{1}: WIP on main: 5e5738a 15: git log command
stash@{2}: WIP on main: 5e5738a 15: git log command
```

### git stash apply
applies most recent stash to working directory

```
PS C:\Users\acer\Desktop\git_assign> git stash apply
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md
```

### git stash drop stash@{1}
drop the given stash


### git stash show
show the file that is stashed and changes made to it
```
PS C:\Users\acer\Desktop\git_assign> git stash show
 Readme.md | 13 ++++++++++++-
 1 file changed, 12 insertions(+), 1 deletion(-)
PS C:\Users\acer\Desktop\git_assign> git stash show -p
diff --git a/Readme.md b/Readme.md
index 24314f9..6327ad5 100644
--- a/Readme.md
+++ b/Readme.md
@@ -757,6 +757,17 @@ Changes not staged for commit:
         modified:   Readme.md

-### git stash drop stash@{1}
+### git stash drop 2^M
 drop the given stash
+^M
+PS C:\Users\acer\Desktop\git_assign> git stash list ^M
+stash@{0}: WIP on main: 5e5738a 15: git log command^M
+stash@{1}: WIP on main: 5e5738a 15: git log command^M
+stash@{2}: WIP on main: 5e5738a 15: git log command^M
+PS C:\Users\acer\Desktop\git_assign> git stash drop -q 2        ^M
+PS C:\Users\acer\Desktop\git_assign> git stash list^M
+stash@{0}: WIP on main: 5e5738a 15: git log command^M
+stash@{1}: WIP on main: 5e5738a 15: git log command^M
+^M
+

 ```

 ### git stash pop
 applies stash and deleted from stash list

 ```
 PS C:\Users\acer\Desktop\git_assign> git stash list
stash@{0}: WIP on main: 33b8b33 16.1: git stash command
stash@{1}: WIP on main: 33b8b33 16.1: git stash command
stash@{2}: WIP on main: 5e5738a 15: git log command
stash@{3}: WIP on main: 5e5738a 15: git log command
PS C:\Users\acer\Desktop\git_assign> git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (072f27ed594be87bfefcd48593642b2c079bfd9c)
PS C:\Users\acer\Desktop\git_assign> git stash list
stash@{0}: WIP on main: 33b8b33 16.1: git stash command
stash@{1}: WIP on main: 5e5738a 15: git log command
stash@{2}: WIP on main: 5e5738a 15: git log command
 ```

<br>

## git tag
tags are references that point to specific points in a Git repository's history.
git tags shows list of all tags
```
PS C:\Users\acer\Desktop\git_assign> git tag       
v1.0.0
```

### git tag v1.0.0
this command used to create lightweight tag 
```
PS C:\Users\acer\Desktop\git_assign> git tag v1.0.0
PS C:\Users\acer\Desktop\git_assign> git tag       
v1.0.0
```

### git tag -a v1.0.1 -m "annoted tag"
this command used to create annoted tag 
```
PS C:\Users\acer\Desktop\git_assign> git tag -a v1.0.1 -m "annoted tag"
PS C:\Users\acer\Desktop\git_assign> git tag
v1.0.0
v1.0.1
```

### git tag -d v1.0.0
delete tag locally
```
PS C:\Users\acer\Desktop\git_assign> git tag          
v1.0.0
v1.0.1
PS C:\Users\acer\Desktop\git_assign> git tag -d v1.0.0
Deleted tag 'v1.0.0' (was 5f5dcc1)
PS C:\Users\acer\Desktop\git_assign> git tag
v1.0.1
```

### git push origin --delete tag v1.0.0
delete tags on remote repository
```
 git push origin --delete tag v1.0.1
To https://github.com/Murshid652/Git_Assignment.git
 - [deleted]         v1.0.1
```

<br>

## git worktree
Git Worktree is a feature that allows you to check out multiple branches at once.


### git worktree ../branch branch
creates a new directory for another branch
```
PS C:\Users\acer\Desktop\git_assign> git worktree add ../branch1 branch1
Preparing worktree (checking out 'branch1')
HEAD is now at a9620f3 14.1 : Temporary changes for merge command
```

### git worktree list
get list of all worktree created
```
C:/Users/acer/Desktop/git_assign  fbf3c82 [main]
C:/Users/acer/Desktop/branch1     a9620f3 [branch1]
```

### git worktree remove 'path'
remove a worktree
```
PS C:\Users\acer\Desktop\git_assign> git worktree list
C:/Users/acer/Desktop/git_assign  fbf3c82 [main]
C:/Users/acer/Desktop/branch1     a9620f3 [branch1]
PS C:\Users\acer\Desktop\git_assign> git worktree remove ../branch1
PS C:\Users\acer\Desktop\git_assign> git worktree list
C:/Users/acer/Desktop/git_assign  fbf3c82 [main]
```

<br>

## git fetch
it updates the local repositiry with remote repository


### git fetch origin main
updates local repository with main branch
```
PS C:\Users\acer\Desktop\git_assign> git fetch origin main
From https://github.com/Murshid652/Git_Assignment
 * branch            main       -> FETCH_HEAD
```

<br>

## git pull
updates local repository with content of remote repository
```
PS C:\Users\acer\Desktop\git_assign> git pull origin main
From https://github.com/Murshid652/Git_Assignment
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.
 Readme.md | 434 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 434 insertions(+)
```

<br>

## git push
Update remote repository with local repository
```
PS C:\Users\acer\Desktop\git_assign> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 465 bytes | 465.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
```

<br>

## git remote
use to add, remove, rename remote repository

```
 git remote
origin
PS C:\Users\acer\Desktop\git_assign> git remote show origin
* remote origin
  Fetch URL: https://github.com/Murshid652/Git_Assignment.git
  Push  URL: https://github.com/Murshid652/Git_Assignment.git
  HEAD branch: main
  Remote branches:
    branch1 tracked
    branch2 tracked
    main    tracked
  Local branch configured for 'git pull':
    main merges with remote main
  Local refs configured for 'git push':
    branch1 pushes to branch1 (up to date)
    branch2 pushes to branch2 (fast-forwardable)
    main    pushes to main    (up to date)
PS C:\Users\acer\Desktop\git_assign> git remote add hello https://github.com/Murshid652/git.git
PS C:\Users\acer\Desktop\git_assign> git remote
hello
origin
PS C:\Users\acer\Desktop\git_assign> git remote remove hello
PS C:\Users\acer\Desktop\git_assign> git remote             
origin
```

<br>

## git submodule
to get a secondary remote repository as a module

```
PS C:\Users\acer\Desktop\git_assign> git submodule add https://github.com/Murshid652/git.git gitsubmodule/ 
Cloning into 'C:/Users/acer/Desktop/git_assign/gitsubmodule'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 12 (delta 1), reused 12 (delta 1), pack-reused 0
Receiving objects: 100% (12/12), done.
Resolving deltas: 100% (1/1), done.
```

### git submodule status
to check availiable submodule 
```
PS C:\Users\acer\Desktop\git_assign\gitsubmodule> cd ../
PS C:\Users\acer\Desktop\git_assign> git submodule status
+65b62e9e882ef20186749c3174172ee4b799a7db gitsubmodule (heads/master)
```

<br>

## git show
display various objects and information in repository

### git show 'commithash'
display everything about that particular commit
```
PS C:\Users\acer\Desktop\git_assign> git show c3bf0e217a37d0ebf0d11bef8cd1ae930b76d879
commit c3bf0e217a37d0ebf0d11bef8cd1ae930b76d879 (HEAD -> main, origin/main)
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 14:54:37 2024 +0530

    21.1: git submodule command added readme

diff --git a/Readme.md b/Readme.md
index 4cd1e9b..2117b3e 100644
--- a/Readme.md
+++ b/Readme.md
@@ -971,6 +971,25 @@ PS C:\Users\acer\Desktop\git_assign> git remote
 origin
 

+<br>^M
+^M
+## git submodule^M
+to get a secondary remote repository as a module^M
+^M
+^M
+PS C:\Users\acer\Desktop\git_assign> git submodule add https://github.com/Murshid652/git.git gitsubmodule/ ^M
+Cloning into 'C:/Users/acer/Desktop/git_assign/gitsubmodule'...^M
+remote: Enumerating objects: 12, done.^M
+remote: Counting objects: 100% (12/12), done.^M
+remote: Compressing objects: 100% (7/7), done.^M
+remote: Total 12 (delta 1), reused 12 (delta 1), pack-reused 0^M
+Receiving objects: 100% (12/12), done.^M
+Resolving deltas: 100% (1/1), done.^M
+^M
+^M
+<br>^M
+^M
+## git ^M
```


### git show 'commithash' Readme.md
show changes in Readme.md file for a particular commit hash
```
PS C:\Users\acer\Desktop\git_assign> git show c3bf0e217a37d0ebf0d11bef8cd1ae930b76d879 Readme.md
commit c3bf0e217a37d0ebf0d11bef8cd1ae930b76d879 (HEAD -> main, origin/main)
Author: Murshid Raja <murshidraja652@example.com>
Date:   Fri Jun 21 14:54:37 2024 +0530

    21.1: git submodule command added readme

diff --git a/Readme.md b/Readme.md
index 4cd1e9b..2117b3e 100644
--- a/Readme.md
+++ b/Readme.md
@@ -971,6 +971,25 @@ PS C:\Users\acer\Desktop\git_assign> git remote
 origin

+<br>^M
+^M
+## git submodule^M
+to get a secondary remote repository as a module^M
+^M
+^M
+PS C:\Users\acer\Desktop\git_assign> git submodule add https://github.com/Murshid652/git.git gitsubmodule/ ^M
+Cloning into 'C:/Users/acer/Desktop/git_assign/gitsubmodule'...^M
+remote: Enumerating objects: 12, done.^M
+remote: Counting objects: 100% (12/12), done.^M
+remote: Compressing objects: 100% (7/7), done.^M
+remote: Total 12 (delta 1), reused 12 (delta 1), pack-reused 0^M
+Receiving objects: 100% (12/12), done.^M
+Resolving deltas: 100% (1/1), done.^M
+^M
+^M
+<br>^M
+^M
+## git ^M
```

<br>

## git range-diff
difference between two range of commits

```
PS C:\Users\acer\Desktop\git_assign> git range-diff 0c04e8f2feb0efadbe1299f111864fcb3d039e22...807952ca5d440f3dbe6267491c5ea1c08ff3d478 ee697e0b348a7faf337caf0df371835d52ee1ce5...e9e02f8b9b6341906d5cd871c2566ace545db091
1:  dafee0c < -:  ------- 12.3 : updating git checkout command
2:  5e5738a < -:  ------- 15: git log command
3:  33b8b33 < -:  ------- 16.1: git stash command
4:  5f5dcc1 < -:  ------- 16.2: Some more git stash commands
5:  fbf3c82 < -:  ------- 17: git tag commands
6:  f5dba7f < -:  ------- 18: git worktree command
7:  0fce6bf < -:  ------- 19: git fetch
8:  807952c < -:  ------- 20: git remote command
-:  ------- > 1:  a9a80d8 6: Git notes commands
-:  ------- > 2:  fe16926 7: git restore commands
-:  ------- > 3:  4468908 8: git restore commands
-:  ------- > 4:  c4a38b5 9: git rm command
-:  ------- > 5:  e9e02f8 10: git mv command
```

<br>






