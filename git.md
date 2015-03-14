###Set your user info

To set your username for a specific repo (run command in your repo's root dir):
`git config user.name "Billy Everyteen"`

Confirm the username you set with:
`git config user.name`

You can do the same thing for the following properties on the user object:

`email`

To set your username for every repository on your computer:
`git config --global user.name "Billy Everyteen"`

Now confirm the global name:
`git config --global user.name`

See: [Setting your username in Git](https://help.github.com/articles/setting-your-username-in-git/)

###Removing Files & Directories From a Repo

To Remove a file from a commit (and delete it from the filesystem):
`git rm file1.txt`

To remove a file from a git repo (but leave it on the filesystem):
`git rm --cached file.txt`

To remove a directory from git:
`git rm -r -f directory/*`

Notes: update your .gitignore if you don't want these files to be added back in.

## Nice Resources

-[A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)