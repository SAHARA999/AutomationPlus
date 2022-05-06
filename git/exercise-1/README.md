## Exercise - 1: First steps with Git on your machine

1. Create a project folder and execute git init.
You need to create a project folder structure:
```shell
sebastian.eidner@AMAC02DV2DCMD6R % cd ~
student-1$ mkdir firstgitrepo
student-1$ cd firstgitrepo/
```

2. Initialize the directory with git:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git init
Initialized empty Git repository in /Users/sebastian.eidner/Documents/all_in_one/firstgitrepo/.git/
```

3. Add a file to the folder:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % touch first.yaml
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % ls
first.yaml
```
4. Check the status of your local repo:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git status
```
You will see that the first.yaml is currently in the project folder, but not yet observed by git.
```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	first.yaml

nothing added to commit but untracked files present (use "git add" to track)
```

5. Add a file to the staging area:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git add first.yaml
```

Then check what happens with the status.
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git status
```
You will see that a new file is added to the staging area and is ready to be commited to the local repo.
```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   first.yaml
```

Commit the first version and give a meaningful description.
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git commit -m "first init"
[master (root-commit) 76147a9] first init
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 first.yaml
```
