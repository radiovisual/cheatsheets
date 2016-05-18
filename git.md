### Set your user info

To set your username for a specific repo (run command in your repo's root dir):
```
git config user.name "Michael Scott"
```

Confirm the username you set with:
```
git config user.name`
```

To set your username for every repository on your computer:
```
git config --global user.name "Michael Scott"
```

Now confirm the global name:
```
git config --global user.name`
```

See: [Setting your username in Git](https://help.github.com/articles/setting-your-username-in-git/)

#### Track changes to a file

```sh
git log --follow -p -- file
```

#### Removing Files & Directories From a Repo

To remove a file from a commit (and delete it from the filesystem):
```
git rm file1.txt
```

To remove a file from a git repo (but leave it on the filesystem):
```
git rm --cached file.txt
```

To remove a directory from git:
```
git rm -r -f directory/*
```

Notes: update your .gitignore if you don't want these files to be added back in.


#### Make Your Fork Track the Original Upstream Repo ([source](https://gun.io/blog/how-to-github-fork-branch-and-pull-request/))

This step isn't absolutely necessary, but I find it **very useful** if you plan on working on this project for anything more than a very quick fix. Use the following commands to add the 'upsteam' (original project location) as a remote branch so that you can get their updates into your branch. Replace the 'upstreamname' and 'projectname' values with that actual user/project name that you're trying to track.
```
git remote add --track master upstream git://github.com/upstreamname/projectname.git
```
This will add the original project as a remote named 'upstream'. To get the code, type:
```
git fetch upstream
```
Then, to merge it into your own project, type:
```
git merge upstream/master
```
Tada! Now you'll have an up-to-date version of the upstream code in your current branch.


#### Comparing the difference between files across commits

Use the `diff` command to compare the difference between commits.

For example, to see the differences across commits for file.txt

 ```
 git diff file.txt
 ```

This command can do a [lot more](http://git-scm.com/docs/git-diff).

#### Sync Your Local Fork

```
git fetch upstream
git checkout master
git merge upstream/master
```

If you get an error: `fatal: 'upstream' does not appear to be a git repository` then you first need to add the upstream repo before running the commands above:

```
git remote add upstream https://github.com/original-project/repo-name.git
```

#### Check your Remotes

```
$ git remote -v
origin	https://github.com/my-project/repo-name.git (fetch)
origin	https://github.com/my-project/repo-name.git (push)
upstream	https://github.com/original-project/repo-name.git (fetch)
upstream	https://github.com/original-project/repo-name.git (push)
```

#### Change a remote url

```
$ git remote set-url origin git://new.url.here
$ git push -u origin master (use -u on your first new push to specify new upstream)
```

#### Change git's default text editor

Update your `PATH` variable to point to the application if the command to launch it is not already available to the command line:
```
# Add TextEdit to your PATH so it can be launched by git
export PATH=/Applications/TextEdit.app/Contents/MacOS/TextEdit:$PATH
```

Now add the command to git's config file:

```
$ git config --global core.editor TextEdit
```

#### Changing the Latest Commit Message (BEFORE pushed to GitHub)

```
$ git commit --amend -m "New commit message"
```

#### Revert to an old commit

```
$ git reset --hard <SHA CHECKSUM of your commit>
```

#### Delete a Local Branch

```
$ git branch -d the_local_branch
```

#### Rollback to a Previous Commit

**Note:** Using this is dangerous in a collaborative environment: you're rewriting history!

If just local:
```
$ git reset --hard <old-commit-id>
```

Local and remote:

```
git push -f <remote-name> <branch-name>
```

#### Rename a file in git

```
$ git mv <oldfilename> <newfilename>
```

#### Remove Uncommitted Changes

Remove any uncommitted changes and revert back to the state of your last commit:

```
$ git reset --hard HEAD
```

#### Global Ignore

Create (or edit) a .gitignore_global file.

```
touch ~/.gitignore_global
```

with the following sample contents (for MAC OS X): 

<pre>
# OS generated files #
######################
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db
</pre>

Now register the `.gitignore_global` file with git:

```
git config --global core.excludesfile ~/.gitignore_global
```


### Nice Resources

- [Pro Git](http://git-scm.com/book/en/v2)
- [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)
- [HOW TO GITHUB: FORK, BRANCH, TRACK, SQUASH AND PULL REQUEST](https://gun.io/blog/how-to-github-fork-branch-and-pull-request/)
- [Git Fake Submodules](http://debuggable.com/posts/git-fake-submodules:4b563ee4-f3cc-4061-967e-0e48cbdd56cb)
- [Learn Git Branching](http://learngitbranching.js.org/)
- [How To Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
- [quick tip - syncing your local git fork](http://harlankellaway.com/blog/2014/11/19/git-syncing-local-fork/)
- [My pull request was merged, now what?](http://stackoverflow.com/a/12772000/3960969)

### Remove Sensitive Data

- [Remove Sensitive Data from Git](https://help.github.com/articles/remove-sensitive-data/)
