# dotfiles

This repository contains all my dotfiles and config files.

## Prerequisites

The following tools need to be installed:

### Git

```bash
brew install git
```

### Stow

```bash
brew install stow
```

## Installation

Firstly, checkout the `dotfiles` repository to your `$HOME` directory using `git`.

```bash
$ git clone git@github.com/pablobastidasv/dotfiles
$ cd dotfiles
```

Then, use `GNU stow` to create symlinks of the files in the `dotfiles` folder.

```bash
$ stow .
```

Finally, install all the `brew` packages.

```bash
$ xargs brew install < brew_leaves
```

## Leaving machine

When leaving the machine, or when new homebrew installations have been added that is needed
for future setups, then generate the leaves again.

```bash
$ brew leaves --installed-on-request > brew_leaves
```
