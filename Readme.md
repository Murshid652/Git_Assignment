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



