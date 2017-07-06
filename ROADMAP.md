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

## Create symklinks

Create base directory for symlinks and move into it.

```shell
mkdir -p ~/bin/git
cd ~/bin/git
```

```shell
# get all subdirectory names and print them out
cd ~/bin/git-2.9.2
ls -d */ | awk '{print $NF}' | xargs -n1 sh -c 'echo "${0%?}"'
```

# desired output

```shell
#!/bin/bash
#
# file: activate-git-2.9.2.sh
#

rm bin
ln -s ../git-2.9.2/bin bin

rm lib
ln -sf ../git-2.9.2/lib lib

rm libexec
ln -sf ../git-2.9.2/libexec libexec


rm share
ln -sf ../git-2.9.2/share share
```

