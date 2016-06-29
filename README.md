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

* commit — save changes locally
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

## 101

Before issuing any commands run `gitsh`.

### Downloading repositories

```sh
cl git@github.com:wieczorek1990/git-101.git
```

### Viewing local branches

```sh
b
```

### Viewing remote branches

```sh
br
```

### Viewing all branches

```sh
ba
```

### Changing branches

```sh
co master
co develop
```

### Creating branches

```sh
bn develop
pt
```

### Renaming branches

```sh
co developp
bm develop
```

### Removing local branches

```sh
bd developp
```

```sh
bdf developp
```

### Removing remote branches

```sh
p :developp
```

### Viewing changes

```sh
s
```

### Viewing not staged differences

```sh
d
```

### Viewing staged differences

```sh
dc
```

### Viewing all differences

```sh
da
```

### Viewing differences with Meld

```sh
dt
```

### Viewing logs

```sh
l
```

```sh
ls
```

### Viewing your commits

```sh
lm
```

### Pushing changes

```sh
p
```

### Pushing changes after rebase

```sh
pf
```

### Ignoring files

```sh
vi .gitignore
vi tutorial/.gitignore
a .gitignore tutorial/.gitignore
```

### Merging

```
co develop
m feature/documentation/readme
```

### Cherry picking commits

```sh
cp 509d17a
```

### Commiting all files

```sh
aa
cm 'Initial commit'
```

### Commiting all versioned files

```sh
ca 'Refactoring'
```

### Resolving conflicts with Meld

```sh
mt
aa
c
```

### Stashing changes

```sh
st
```

### Viewing last stash differences

```sh
ds
```

### Poping stashed changes

```sh
stp
```

### Destroying last stashed changes

```sh
std
```

### Listing stash contents

```sh
stl
```

### Undoing last commit

```sh
undo
```

### Amending last commit message and author

```sh
amend
```

### Rebasing history

```sh
ri develop
```

```sh
ri @~3
```

### Pulling changes

```sh
pu
```

### Pulling changes using rebase

```sh
pur
```

### Creating features or fixes

```sh
co develop
pu
bn feature/documentation/readme
vi README.md
a README.md
cm 'Added README.md'
p
pur develop
pf
```

### Viewing work done by yourself before standup

```sh
standup
```

