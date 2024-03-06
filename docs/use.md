# Usage guide

In developing `tfversion` our 2 focus points are simplicity and smooth user experience, enabling you to effortlessly use Terraform on any platform.

## Help

You can ask the CLI for help and examples for any command.

```sh
tfversion --help
tfversion list --help
```

## Installing

Installing a Terraform version can be done in a few ways:

### Install latest stable

This command checks with the HashiCorp servers what the most recent stable release is and then installs it.

```sh
tfversion install --latest
```

### Install specific version

If you need a specific version, you can install it by specifying the version number.

```sh
tfversion install 1.7.4
```

### Install latest pre-release

If you want to test pre-release features, you can install the latest pre-release.

```sh
tfversion install --latest --pre-release
```

### Install required for current directory

This command searches for `.tf` files in your current directory and sees if `required_version` is specified anywhere.
It then installes the latest matching version.

```sh
tfversion install --required
```

## Use

Once you have installed a Terraform version, you can activate it with the `use` command.

> Note: When using a version, it must always be installed first!

### Use latest stable

Use the latest stable version.

```sh
tfversion use --latest
```

### Use specific version

Use a specific version.

```sh
tfversion use 1.7.4
```

### Use the latest pre-release

Use the latest pre-release version.

```sh
tfversion use --latest --pre-release
```

### Use the required version for your current directory

Use the most recent version that matches with the required version in your current directory.

```sh
tfversion use --required
```

## Alias

If you don't want to remember which version you are using for a specific purpose (for example a client), you can use the alias feature.

### Create an alias

First create the alias by specifying the name and the target version.

```sh
tfversion alias default 1.7.4
tfversion alias my-client 1.2.3
```

### Use an alias

Then you can activate it by using the name.

```sh
tfversion use default
tfversion use my-client
```

## List

If you're curious which Terraform versions are available or installed, you can use the `list` command.

### List all available versions

Shows all available versions from the HashiCorp API sorted with the most recent one on top.

```sh
tfversion list
```

You can limit the amount of results.

```sh
tfversion list --max-results=10
```

### List all installed versions

Shows all installed versions.

```sh
tfversion list --installed
```

You can limit the amount of results.

```sh
tfversion list --installed --max-results=10
```

### List aliases

Shows all aliases and their target versions.

```sh
tfversion list --aliases
```

## Uninstalling

If you want to remove a Terraform version, you can use the `uninstall` command.

```sh
tfversion uninstall 1.7.4
```
