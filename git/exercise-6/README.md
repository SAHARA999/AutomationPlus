## Exercise - 6: Resolve a merge conflict

1. Go to your Github and edit on the master branch the first.yaml. Add a new line: "remote repo".

2. Go to your local git repository and add a new line: "local repo":
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % echo "local repo" >> first.yaml
```

3. Add the local file to staged and commit it to your local repo:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git add first.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git commit -m "local repo added"
```

4. Push the code to your remote repo:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git push -u origin master
To github.com:sebastianeidner1980/testrepo.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'git@github.com:sebastianeidner1980/testrepo.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

5. Pull the remote repo:

```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git pull origin master
From github.com:sebastianeidner1980/testrepo
 * branch            master     -> FETCH_HEAD
Auto-merging first.yaml
CONFLICT (content): Merge conflict in first.yaml
Automatic merge failed; fix conflicts and then commit the result.
```

6. Show the content of the conflicted file:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % cat first.yaml
I have added a line with the editor
I have added a line with the editor
<<<<<<< HEAD
Local repo
=======
remote repo
>>>>>>> cd6ec699d369be8b1a2acc484b2cf460ea3697ae
```

7. Edit the file:
Delete the merge conflict marker <<<<<<< =======  >>>>>>>
```
<<<<<<< HEAD
Local repo
=======
remote repo
>>>>>>> cd6ec699d369be8b1a2acc484b2cf460ea3697ae
```

and leave only this part from the block:

```
Local repo
```

8. Now you add the file to stage, commit it and push it to the remote repository:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git add first.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git commit -m "fixed merge conflicts"
[WARN] Non-allowed remote URL in the repo: git@github.com:sebastianeidner1980/testrepo.git
[master 7eca35f] fixed merge conflicts
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git push origin master
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 425 bytes | 425.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To github.com:sebastianeidner1980/testrepo.git
   cd6ec69..7eca35f  master -> master
```

9. Verify the result on your Github. 
