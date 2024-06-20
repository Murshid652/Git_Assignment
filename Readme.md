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

### git mv file folder1/
move a file to different directory
```
PS C:\Users\acer\Desktop\git_assign> git mv file4.txt folder1/
```

<br>

## git branch
The git branch command lets you create, list, rename, and delete branches

### git branch
list all branches
```
PS C:\Users\acer\Desktop\git_assign> git branch
* main
```

### git branch 'branchname'
create a branch
```
PS C:\Users\acer\Desktop\git_assign> git branch branch1 
PS C:\Users\acer\Desktop\git_assign> git branch 
  branch1
* main
```

### git branch -m branch1 branch2
rename a branch
```
PS C:\Users\acer\Desktop\git_assign> git branch
  branch1
* main
PS C:\Users\acer\Desktop\git_assign> git branch -m branch1 branch2 
PS C:\Users\acer\Desktop\git_assign> git branch
  branch2
* main
```

### git branch -d 'branchname'
delete a branch
```
PS C:\Users\acer\Desktop\git_assign> git branch -d branch1
Deleted branch branch1 (was e9e02f8).
PS C:\Users\acer\Desktop\git_assign> git branch
* main
```

<br>

## git checkout
It is used to switch branches or restore working tree files

### git checkout 'branch-name'
This command switches your working directory to the specified branch.



