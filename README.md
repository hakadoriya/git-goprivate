# [`git-goprivate`](https://github.com/hakadoriya/git-goprivate)

`git-goprivate` is a git subcommand for setting up a .git/config file for `GOPRIVATE` environment variable.

## Installation

```sh
curl -sSfL https://raw.githubusercontent.com/hakadoriya/git-goprivate/main/git-goprivate -o ./git-goprivate && chmod +x ./git-goprivate
```

If you want to use `git-goprivate` as a git subcommand, you can move it to a directory in PATH.

```sh
# e.g. move to a directory in PATH
mv ./git-goprivate /usr/local/bin/git-goprivate

# now you can use `git-goprivate` as a git subcommand
git goprivate
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
