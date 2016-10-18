# git 101

## Setup

Install [`git`](https://git-scm.com/download/linux), [`gitsh`](https://github.com/thoughtbot/gitsh/blob/master/CONTRIBUTING.md#contributing-a-feature), [`git-standup`](https://github.com/kamranahmedse/git-standup), [`meld`](http://meldmerge.org/).

Save [`.gitconfig`](https://github.com/wieczorek1990/dotfiles/blob/master/.gitconfig) as `~/.gitconfig`.

Create `~/.gituser` with contents:

```sh
[user]
  name = $first-name $last-name
  email = '$username@$domain'
```

Optionally create `~/.gitlocal` with custom local configuration.

Create SSH keys and add them to your Git server provider if not done already.

```sh
ssh-keygen
cat ~/.ssh/id_rsa.pub
```

### Setting default editor in git config

Atom:

```sh
git config --global core.editor 'atom --wait'
```

Sublime Text:

```sh
git config --global core.editor subl
```

VIM:

```sh
git config --global core.editor vim
```

### Setting default editor in Bash

You might want to specify a different default editor for Git actions.

I recommed you to learn VIM, but if you wish to use Atom do as follows.

Make sure that you have a `.bash_profile` file in home directory (`~/.bash_profile`) with simillar contents:

```sh
if [ -f "$HOME/.bashrc" ]
then
  . "$HOME/.bashrc"
fi
```

You might have `.profile` file (`~/.profile`) with simmilar content instead.

You also need to add the following line to `.bashrc` file (`~/.bashrc`).

```sh
export EDITOR='atom --wait'
```

For Sublime Text:

```sh
export EDITOR=subl
```

In case you want VIM instead type:

```sh
export EDITOR=vim
```

### GUI text editors on Mac OS

Create `/usr/local/bin/` if it does not exist. We will place symlinks in there as it is in `PATH` variable by default.

```sh
sudo mkdir -p /usr/local/bin/
```

#### Atom

After unziping the archive downloaded from official Atom site move it to
Applications folder and create a symlink to `atom.sh`:

```sh
sudo ln -s /Applications/Atom.app/Contents/Resources/app/atom.sh /usr/local/bin/atom
```

#### Sublime Text

After installing create a symlink to `subl`:

```sh
sudo ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

## Nomenclature

> Correct me if I am wrong. I am no expert. I just use it for work.

* add - adds the files you want to commit
* commit — save changes locally with a message about what was changed
* push — send changes to some Git server
* pull — receive changes from some Git server
* merge — merge changes from different branche
* rebase — rewrite changes history, usually to:
  * put your changes on top of others changes to maintain clear commit history and avoid merges
  * squash, fixup changes
  * reword commit messages
* stash — save local changes without commiting them in stash
* cherry pick — apply chosen commit to the current branch
* branch — name pointing at commit
* staged files — files to add, remove or modify in commit

## Tutorials

1. [Moving around](/tutorials/1.md)
2. [Changes everywhere](/tutorials/2.md) [In progress]

## Exercises

1. [Repository structure](/exercises/1.md)
2. [Changes everywhere part 1](/exercises/2-1.md)
3. [Changes everywhere part 2](/exercises/2-2.md)

## Aliases

View [Aliases.md](/Aliases.md) for my aliases descriptions.

## Links

1. [A Visual Git Reference](http://marklodato.github.io/visual-git-guide/index-en.html)
2. [git — the simple guide](http://rogerdudler.github.io/git-guide/)

