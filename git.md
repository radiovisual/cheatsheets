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



### Removing Files & Directories From a Repo

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


### Make Your Fork Track the Original Upstream Repo ([source](https://gun.io/blog/how-to-github-fork-branch-and-pull-request/))

This step isn't absolutely necessary, but I find it **very useful** if you plan on working on this project for anything more than a very quick fix. Use the following commands to add the 'upsteam' (original project location) as a remote branch so that you can get their updates into your branch. Replace the 'upstreamname' and 'projectname' values with that actual user/project name that you're trying to track.
'''
git remote add --track master upstream git://github.com/upstreamname/projectname.git
'''
This will add the original project as a remote named 'upstream'. To get the code, type:
'''
git fetch upstream
'''
Then, to merge it into your own project, type:
'''
git merge upstream/master
'''
Tada! Now you'll have an up-to-date version of the upstream code in your current branch.

### Comparing the difference between files across commits

Use the `diff` command to compare the difference between commits.

For example, to see the differences across commits for file.txt

 ```
 git diff file.txt
 ```

This command can do a [lot more](http://git-scm.com/docs/git-diff).


## Nice Resources

- [Pro Git](http://git-scm.com/book/en/v2)
- [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)
- [HOW TO GITHUB: FORK, BRANCH, TRACK, SQUASH AND PULL REQUEST](https://gun.io/blog/how-to-github-fork-branch-and-pull-request/)