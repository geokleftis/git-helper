This is a test file

Intiate git in a dir

```
git init
```

See the files added/edited since last commit

```
git status
git log

```


add files under a path to git list

```
git add .
```

commit changes

```
git commit -m "This is the commit's message"
```

```
git push
```
At this point it does not know where to upload. So we have to connect our local git project with a github repository


```
fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>

PS C:\Users\ukleftis\Desktop\python-project> git remote add origin https://github.com/geokleftis/git-helper.git
PS C:\Users\ukleftis\Desktop\python-project> git branch -M main
PS C:\Users\ukleftis\Desktop\python-project> git push -u origin main
info: please complete authentication in your browser...
PS C:\Users\ukleftis\Desktop\python-project> git remote add origin https://github.com/geokleftis/git-helper.git
error: remote origin already exists.
PS C:\Users\ukleftis\Desktop\python-project> git branch -M main
PS C:\Users\ukleftis\Desktop\python-project> git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 1.29 KiB | 331.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/geokleftis/git-helper.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```