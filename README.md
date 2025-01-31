# [`git-goprivate`](https://github.com/hakadoriya/git-goprivate)

`git-goprivate` is a git subcommand for setting up a .git/config file for `GOPRIVATE` environment variable.

## Installation

```sh
# install
curl -sSfL https://raw.githubusercontent.com/hakadoriya/git-goprivate/main/git-goprivate -o /usr/local/bin/git-goprivate

# now you can use `git-goprivate`
git-goprivate
```

## Features

### `setup`

Set up a .git/config file for `GOPRIVATE` environment variable.

```console
$ GITHUB_TOKEN=$(gh auth token) GOPRIVATE=github.com/hakadoriya git-goprivate setup

$ tail -n 2 .git/config
[url "https://gho_GITHUBACCESSTOKEN:x-oauth-basic@github.com/hakadoriya"]
        insteadOf = https://github.com/hakadoriya
```

## Usage

```console
$ git-goprivate
git-goprivate - a git subcommand for setting up a .git/config file for `GOPRIVATE` environment variable.

Usage:
  git-goprivate <SUBCOMMAND>

SUBCOMMAND:
    setup
        Set up a .git/config file for `GOPRIVATE` environment variable.
        Usage:
          git-goprivate setup [--global|--local]
    help, usage
        Show this help message.
        Usage:
          git-goprivate help
```
