# New dotfiles repo

All files are .gitignored by default, use `git add -f <file>` to add to repo

## Setup on new computer

```shell
cd ~
git init
git remote add origin git@github.com:lisadean/newdotfiles.gitdotfiles
git fetch
git checkout -f main
```

## Reference

Heavily inspired by [Drew Devault's dotfiles](https://drewdevault.com/2019/12/30/dotfiles.html)

Shell profile loading order: https://medium.com/@rajsek/zsh-bash-startup-files-loading-order-bashrc-zshrc-etc-e30045652f2e
