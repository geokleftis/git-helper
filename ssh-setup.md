1. Created ~/.ssh dir
2. Create an ssh key for the gihub connection
```
ssh-keygen -t ed25519 -C "geokleftis@gmail.com"
```
3. Write key to file in Desktop
4. Open admin elevated console by right clicking powershell, open as admin
```
Get-Service ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
```
5. Copy the public key:

```
cat ~/.ssh/id_ed25519.pub
```

6. Go to GitHub → Settings → SSH and GPG Keys
Click New SSH key
Paste the key, give it a name, and save.

7. Test the ssh connection
```
ssh -T git@github.com
```

response is 
```
PS C:\Users\ukleftis\Desktop\python-project> ssh -T git@github.com
>> 
The authenticity of host 'github.com (111.11.111.1)' can't be established. 
ECDSA key fingerprint is SHA256:asdfasdfasdfasdfasdf.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes   
Warning: Permanently added 'github.com,111.11.11.1' (ECDSA) to the list of known hosts.
Hi geokleftis! You've successfully authenticated, but GitHub does not provide shell access.
```

8. We now have to login. if we were to commit we would get
```
PS C:\Users\ukleftis\Desktop\python-project> git commit -m "Intial commit"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'ukleftis@DESKTOP-CEUVNR7.(none)')
PS C:\Users\ukleftis\Desktop\python-project> 
```

9. Login
```
PS C:\Users\ukleftis\Desktop\python-project> git config --global user.email "geokleftis@gmail.com"
PS C:\Users\ukleftis\Desktop\python-project> git config --global user.name "geokleftis"
```

10. Commit!

```
git commit -m "Initial commit"
```

Sample change