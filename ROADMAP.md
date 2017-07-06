# ROADMAP.md for ansible-role-git

## multiversion support

### ~/.profile or ~/.bashrc or source able script

* turn this into a script?

```shell
export PATH="$HOME/bin/git/bin:$PATH"
```

### ~/bin link to preferred git version

Ensure for common root dir and move into it.

```shell
 cd ~/bin
 pwd
 ~/bin
```

Path to the directory you 

#### Create symklinks

Create base directory for the application and move into it.

```shell
mkdir -p ~/bin/git
cd ~/bin/git
```
collect the names of all subdirectories

```shell
# get all subdirectory names and print them out
cd ~/bin/git-2.9.2
ls -d */ | awk '{print $NF}' | xargs -n1 sh -c 'echo "${0%?}"'
```

our desired desired output is something like this:

```shell
#!/bin/bash
#
# file: common_root_dir/git/activate-git-2.9.2.sh
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
make it executable
