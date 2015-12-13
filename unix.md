#UNIX cheatsheet

###Learning Unix

- [The Art of the Command Line](https://github.com/jlevy/the-art-of-command-line)
- [Cyberwizard Institute Unix](https://github.com/cyberwizardinstitute/workshops/blob/master/unix.markdown)
- [Become a Unix Wizard](https://github.com/substack/unix-adventure)
- [Eight Terminal Utilities Every OS X Command Line User Should Know - Part 1](http://www.mitchchn.me/2014/os-x-terminal/?x)
- [Eight Terminal Utilities Every OS X Command Line User Should Know - Part 2](http://www.mitchchn.me/2014/and-eight-hundred-more/)

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

### Change the permissions on a directory to the current user

`sudo chown -R $USER /usr/local`

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

### Find all occurrences of a string

```
grep -i stringToSearchFor * -R
```

### See what programs are open on a specific port:

#### lsof (LiSt Open Files)
```
$ lsof -i :8000
Python    9130 michael    4u  IPv4 0x0000000000000000      0t0  TCP localhost:irdmi (LISTEN)
```

### Get detailed information about a process

```
$ echo "get in on PID 9130"
$ ps -fp 9130
```