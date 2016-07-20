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

## Exercises

1. [Repository structure](/exercises/1.md)
1. [Changes everywhere](/exercises/2.md)

## Aliases

View [Aliases.md](/Aliases.md) for my aliases descriptions.

## Links

1. [A Visual Git Reference](http://marklodato.github.io/visual-git-guide/index-en.html)
2. [git — the simple guide](http://rogerdudler.github.io/git-guide/)

