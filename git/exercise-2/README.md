## Exercise - 2: Get the code to Github

1. Go to your Github and get your repo:
```
git@github.com:sebastianeidner1980/testrepo.git
```

2. Add your Github as a remote repo:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git remote add origin git@github.com:sebastianeidner1980/testrepo.git
```

3. Check if the remote branch is setuped:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git remote -v
origin	git@github.com:sebastianeidner1980/testrepo.git (fetch)
origin	git@github.com:sebastianeidner1980/testrepo.git (push)
```

4. Push the Code to your remote repo:

Cause we are using ssh for the authenification, we will be asked if we trust the remote host. This will always happen when you do the first push. 
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git push -u origin master
The authenticity of host 'github.com (140.82.121.4)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com,140.82.121.4' (RSA) to the list of known hosts.
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 222 bytes | 222.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/sebastianeidner1980/testrepo/pull/new/master
remote:
To github.com:sebastianeidner1980/testrepo.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

5. Check on Github if the code is online.
