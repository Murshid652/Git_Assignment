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
  (use "git restore --staged <file>..." to unstage)
        new file:   file1.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
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
  (use "git restore --staged <file>..." to unstage)
        new file:   file1.txt
        new file:   file2.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
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
  (use "git restore --staged <file>..." to unstage)
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
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file2.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
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
  (use "git restore --staged <file>..." to unstage)
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
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file2.txt
        new file:   file3.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
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
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md
        new file:   file1.txt
        new file:   file2.txt
        new file:   file3.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
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
   (use "git restore <file>..." to discard changes in working directory)
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
+  (use "git restore --staged <file>..." to unstage)
+        modified:   Readme.md
+        new file:   file1.txt
+        new file:   file2.txt
+        new file:   file3.txt
+
+Changes not staged for commit:
+  (use "git add <file>..." to update what will be committed)
+  (use "git restore <file>..." to discard changes in working directory)
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
   (use "git restore <file>..." to discard changes in working directory)
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
   (use "git restore <file>..." to discard changes in working directory)
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

### git commit --allow-empty -m "Empty commit"
