- To change the default branch name:
```bash
$ git config --global init.defaultBranch main
```
- To initialize the repo:
```bash
$ git init
```
- To see it's status:
```bash
$ git status
```
- To delete the repo, you need to delete `.git`.
```bash
$ rm -rf .git
```

- View the log with:
```bash
$ git log
```
# Workflow
1. Initialize the repo
2. Create the files
3. Add them to version control:
```bash
$ git add --all
```
  - If the files are modified, it will be shown when you run `git status`.
4. To remember the modifications you've made, run `git add` again.

5. __The next step is committing__ (`-m` flag is used to add a message):
```bash
$ git commit -m 'Мой первый коммит!'
```

# Remote repos

To connect to a remote repository, run:
```bash
$ git remote add [name] [URL]
```
For github, copy SSH link on the repository page. For example:
```bash
$ git remote add origin git@github.com:shekelashvili-st/git-first.git
```
See if the connection was successful (`-v` is for verbose):
```bash
$ git remote -v
```

Send the changes to remote repo (`-u` flag is used to link the current local branch to the remote one):
```bash
$ git push -u origin main
```
Next `push` commands won't need the `-u` flag.

To clone a repo:
```shell
$ git clone [adress] # укажите адрес репозитория
```
>[!important] 
>If you cloned the repo, the branches are linked by default