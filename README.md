# [`git-goprivate`](https://github.com/hakadoriya/git-goprivate)

`git-goprivate` is a git subcommand for configuring `.git/config` to work with the `GOPRIVATE` environment variable.

## Installation

```sh
curl -sSfL https://raw.githubusercontent.com/hakadoriya/git-goprivate/main/git-goprivate -o ./git-goprivate && chmod +x ./git-goprivate
```

To use `git-goprivate` as a git subcommand, move it to a directory in your PATH:

```sh
# Example: Move to a directory in PATH
mv ./git-goprivate /usr/local/bin/git-goprivate

# Now you can use it as a git subcommand
git goprivate
```

## Features

### `add`

Configures `.git/config` for use with the `GOPRIVATE` environment variable.

```console
$ GITHUB_TOKEN=$(gh auth token) GOPRIVATE=github.com/hakadoriya git-goprivate add

$ tail -n 2 .git/config
[url "https://gho_GITHUBACCESSTOKEN:x-oauth-basic@github.com/hakadoriya"]
        insteadOf = https://github.com/hakadoriya
```

## Usage

```console
$ git-goprivate
git-goprivate - a git subcommand for configuring .git/config to work with the GOPRIVATE environment variable.

Usage:
  git-goprivate <SUBCOMMAND>

SUBCOMMAND:
    add
        Configure .git/config for use with the GOPRIVATE environment variable.
        Usage:
          git-goprivate add [--global|--local]
    help, usage
        Show this help message.
        Usage:
          git-goprivate help
```
