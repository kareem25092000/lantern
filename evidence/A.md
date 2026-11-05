# Evidence: A

## E1
```
$ git remote -v
origin	https://github.com/kareem25092000/lantern.git (fetch)
origin	https://github.com/kareem25092000/lantern.git (push)

```

## E2
```
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   tasks.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	lantern.py


$ git diff tasks.py

$ git diff --staged tasks.py
diff --git a/tasks.py b/tasks.py
new file mode 100644
index 0000000..f11aa91
--- /dev/null
+++ b/tasks.py
@@ -0,0 +1,7 @@
+_TASKS = []
+def add_task(title):
+    task = {"title": title}
+    _TASKS.append(task)
+    return task
+def list_tasks():
+    return list(_TASKS)
\ No newline at end of file

```

## E4
```
$ git log --oneline --graph --decorate -10 2239dbf
*   2239dbf add both features to task.p Merge branch 'feature/done-flag'
|\  
| * 5e5d47b feat(tasks): add done flag to new tasks
* | 9193a8e fix(tasks): strip whitespace from titles
|/  
*   07a72b1 Merge branch 'main' of https://github.com/kareem25092000/lantern
|\  
| *   96955f3 docs(readme): add Mohamed Hamzawi to team table
| |\  
| | *   c05d0d3 docs(readme): add Mohamed Hamzawi to team table
| | |\  
| * | \   e909245 docs(readme): add Mohamed Hamzawi to team table
| |\ \ \  
| | |/ /  
| |/| /   
| | |/    
| * | 2de2bf6 docs(readme): add Mohamed Hamzawi to team table
* | | 8f42964 chore(notes): rename draft.txt to notes.txt
* | | 7c8693f chore(notes): add draft placeholder

```

## E5 (a)
```
$ git reflog -6
cba584a HEAD@{0}: commit (amend): chore(notes): add ship note
a8ec150 HEAD@{1}: commit: chore(notes): add shpi note
e7bf0e0 HEAD@{2}: pull: Merge made by the 'ort' strategy.
0ad5deb HEAD@{3}: commit: fix(env): stop tracking .env
798c1f9 HEAD@{4}: commit: chore(env): add local settings
e584633 HEAD@{5}: pull: Merge made by the 'ort' strategy.

```

## E5 (c)
```
$ git reflog -6
78c64ff HEAD@{0}: reset: moving to HEAD@{1}
c4fd867 HEAD@{1}: reset: moving to HEAD~1
78c64ff HEAD@{2}: commit: chore(notes): add demo note
c4fd867 HEAD@{3}: pull: Fast-forward
256e707 HEAD@{4}: pull: Merge made by the 'ort' strategy.
cba584a HEAD@{5}: commit (amend): chore(notes): add ship note

```

## E7
```
$ git push origin main
remote: error: GH006: Protected branch update failed for refs/heads/main.        
remote: 
remote: - Changes must be made through a pull request.        
To https://github.com/kareem25092000/lantern.git
 ! [remote rejected] main -> main (protected branch hook declined)
error: failed to push some refs to 'https://github.com/kareem25092000/lantern.git'

```
