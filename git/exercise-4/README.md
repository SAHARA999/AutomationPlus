# Exercise 4: Differences between versions and undo changes

1. Create a new file:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % echo "Welcome, automation students" >> playbook.yaml
```

2. Check the git status:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git status
On branch development
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   playbook.yaml

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   playbook.yaml
```

3. Add the playbook.yaml to staged:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git add playbook.yaml
```

4. Check the changes that will be applied to the local repo:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git diff --cached
diff --git a/playbook.yaml b/playbook.yaml
new file mode 100644
index 0000000..96da4cf
--- /dev/null
+++ b/playbook.yaml
@@ -0,0 +1 @@
+Welcome, automation students
```

5. Remove the playbook.yaml from the staged files:

```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git status
On branch development
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   playbook.yaml
```

```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git restore --staged playbook.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git status
On branch development
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	playbook.yaml

nothing added to commit but untracked files present (use "git add" to track)
```

6. Add the playbook.yaml to your local repo:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git add playbook.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git commit -m "playbook.yaml"
[development 0d25833] playbook.yaml
 1 file changed, 1 insertion(+)
 create mode 100644 playbook.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git status
On branch development
nothing to commit, working tree clean
```

7. Change your playbook.yaml and add it to staged:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % echo "to this to bootcamp" >> playbook.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git add playbook.yaml
```

8. Diff now the local repo with the stage:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git diff --cached
diff --git a/playbook.yaml b/playbook.yaml
index 96da4cf..58507b8 100644
--- a/playbook.yaml
+++ b/playbook.yaml
@@ -1 +1,2 @@
 Welcome, automation students
+ to this to bootcamp
```
