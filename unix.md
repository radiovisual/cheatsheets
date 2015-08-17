#UNIX cheatsheet

###Learning Unix

- [The Art of the Command Line](https://github.com/jlevy/the-art-of-command-line)
- [Cyberwizard Institute Unix](https://github.com/cyberwizardinstitute/workshops/blob/master/unix.markdown)
- [Become a Unix Wizard](https://github.com/substack/unix-adventure)

###The Unix Philosophy

- [Unix Philosophy](https://en.wikipedia.org/wiki/Unix_philosophy)

### Undoing / Fixing / Removing Commits

- [On undoing, fixing, or removing commits in git](http://sethrobertson.github.io/GitFixUm/fixup.html#discard_all_unpushed)

### Get the current user

To see the name of the current user:

`whoami`

### Change the Current User

Use the `chown` (change owner) command

`sudo chown <name_of_user>`

### Processes

#### List all processes
`ps aux`

#### Search for a specific process
`ps aux | grep node`

#### Kill all specific processes
`killall -9 node`
`kill -9 PID`

### View all spaces or tabs in a file

Useful for checking your Makefiles for problematic spaces (only tabs are allowed)

```
cat -e -t -v  makefile_name
```