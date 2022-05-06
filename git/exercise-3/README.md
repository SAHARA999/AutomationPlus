## Exercise - 3: Create a new branch

1. Check your local branches:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git branch
* master
```
2. Create a new branch based on the master:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git checkout -b development
```
3. Check if the branch exits:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git branch
* development
 master
```

4. Push the code to the remote repo:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git push origin development
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 761 bytes | 761.00 KiB/s, done.
Total 8 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To github.com:sebastianeidner1980/testrepo.git
   f193396..73cb995  development -> development
```