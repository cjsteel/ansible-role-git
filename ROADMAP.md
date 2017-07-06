# ROADMAP.md for ansible-role-git

## multiversion support

### ~/.profile or ~/.bashrc or source able script

* turn this into a script?

```shell
export PATH="/home/users/csteel/bin/git/bin:$PATH"
```

### ~/bin link to preferred git version

https://askubuntu.com/questions/524606/creating-a-symbolic-link-to-a-directory

Ensure for and move into common root

```shell
 cd ~/bin
 pwd
 ~/bin
```

Path to the directory you 

Create base directory for symlink to the source directory

```shell
mkdir ~/bin/git
cd ~/bin/git
```

Create relative links to all subdirs

* iterate subdirs to list
* create links

```
ln -s ../git-2.9.2/bin bin
ln -s ../git-2.9.2/lib lib
ln -s ../git-2.9.2/libexec libexec
ln -s ../git-2.9.2/share share
```

