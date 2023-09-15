# New dotfiles repo

git files for the repo are stored in `~/.dotfiles` instead of `~/.git` like they would normally be

## Setup on new computer

```shell
cd ~
git clone --bare git@github.com:lisadean/newdotfiles.git $HOME/.dotfiles.git
git --git-dir=$HOME/.dotfiles.git/ --work-tree=$HOME checkout
```

Backup snippet in case there are files that would be overwritten

```shell
mkdir -p .config-backup && \
config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | \
xargs -I{} mv {} .config-backup/{}
```

## Reference

Heavily inspired by:

- [https://www.atlassian.com/git/tutorials/dotfiles](https://www.atlassian.com/git/tutorials/dotfiles)
- [Drew Devault's dotfiles](https://drewdevault.com/2019/12/30/dotfiles.html)

Shell profile loading order: https://medium.com/@rajsek/zsh-bash-startup-files-loading-order-bashrc-zshrc-etc-e30045652f2e
