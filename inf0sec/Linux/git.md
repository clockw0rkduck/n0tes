multiple credential methods

echo "# c0de" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/clockw0rkduck/n0tes.git
git push -u origin main



git status    [-s for short mode]
git add README.md (add file to staging area)
git restore --staged FILENAME  (remove from staging area)
git restore README.md (undo local changes to README.md)
git clean -fd (undo all local changes)

git log --oneline (see list of commits)
git restore --source=HEAD~1 README.md  (insert README.md from "commit head-1" into local)



now use git add to add files, and git commit to submit changes, then git push -u origin main to update files. 

### Installation: Credential storage with libsecrets (encrypted)
sudo apt-get install libsecret-1-dev
cd /usr/share/doc/git/contrib/credential/libsecret
sudo make
git config --global credential.helper /usr/share/doc/git/contrib/credential/libsecret/git-credential-libsecret


Create Personal Access token at: (https://github.com/settings/tokens/new)[This link]


to configure git settings use: 
```
git config --global --edit
```

```
# This is Git's per-user configuration file.
[user]
# Please adapt and uncomment the following lines:
	name = NAME
	email = EMAIL
username = USERNAME
[credential]
	helper = /usr/share/doc/git/contrib/credential/libsecret/git-credential-libsecret
#	helper = /usr/local/bin/git-credential-manager
[credential "https://dev.azure.com"]
[core]
	editor = codium --wait
	autocrlf = input
[diff]
	tool = codium
[difftool "codium"]
	cmd = "codium --wait --diff $LOCAL $REMOTE"

```

Learning git too! 