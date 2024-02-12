# dotfiles

This repository is powered with [gnu stow](https://www.gnu.org/software/stow/).

> "GNU Stow is a symlink farm manager which takes distinct packages of software and/or data located in separate directories on the filesystem, and makes them appear to be installed in the same place."
>
> \- The project page

Basically stow will create symlinks on the parent repository that wil target the files in this directory so we will be able to use distributed version control to manage them.

## Setup

First install stow on your system

**Opensuse** 🦎
```
sudo zypper ref
sudo zypper in stow
```

**Arch** 🟦
```
sudo pacman -Syu stow
```


**Debian/Ubuntu** 🟠🔴
```
sudo pacman -Syu stow
```

Then run these commands 

```
cd
git clone git@github.com:WoodenMaiden/dotfiles.git
cd dotenv
stow .
```

And tadaaaaa 🎉 you are good to go!