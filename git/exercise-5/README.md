## Exercise - 5: Update the local repository from remote

1. Go to your remote repository and change the branch on master.

2. Edit with your online Github editor the file first.yaml and write some text in this file.

3. Switch on you local system to the master branch and check the content of the file first.yaml:

```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
``` 

As you will see there is no content in this file currently.
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % cat first.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo %
```

4. Now pull your updated code from Github and overwrite your local repository:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git pull origin master
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From github.com:sebastianeidner1980/testrepo
 * branch            master     -> FETCH_HEAD
   76147a9..3c52eea  master     -> origin/master
Updating 76147a9..3c52eea
Fast-forward
 first.yaml | 1 +
 1 file changed, 1 insertion(+)
```

5. Check the content of the file first.yaml:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % cat first.yaml
I have added a line with the editor
```

6. Follow step 1 and 2 to add a new line in to your code.

7. Fetch the code from Github:

```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git fetch origin
```

8. Check the changes that have been made and what will happen when you now do the checkout:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git diff master origin/master
diff --git a/first.yaml b/first.yaml
index b392fd0..cb14c73 100644
--- a/first.yaml
+++ b/first.yaml
@@ -1 +1,2 @@
 I have added a line with the editor
+I have added a line with the editor
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git checkout master
Already on 'master'
Your branch is behind 'origin/master' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)
```

9. Pull the code from the remote repository: 
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git pull origin master
From github.com:sebastianeidner1980/testrepo
 * branch            master     -> FETCH_HEAD
Updating 3c52eea..17a3b4f
Fast-forward
 first.yaml | 1 +
 1 file changed, 1 insertion(+)
 ```

10. Check the code:

```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % cat first.yaml
I have added a line with the editor
I have added a line with the editor
```