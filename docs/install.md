# Installation

## Homebrew

Installing `tfversion` can be done in 2 ways. If you're using homebrew, you can install it with:

```sh
brew install tfversion/tap/tfversion
```

## Binaries

You can also download the latest binary from the [GitHub releases page](https://github.com/tfversion/tfversion/releases).

Supported platforms are:

* `darwin/amd64`
* `darwin/arm64`
* `linux/amd64`
* `linux/arm64`
* `linux/386`

## Configuring your shell

To ensure that `tfversion` is always available in your shell, append the following line to your shell profile (e.g., .bashrc, .zshrc or fish config):

```sh
export PATH="$HOME/.tfversion/bin:$PATH"
```

We prefer to not automagically modify your shell profile, and therefore leave this step to you.
