In developing `tfversion`, our 2 focus points are simplicity and ensuring a smooth user experience, enabling you to effortlessly use Terraform on any platform.

## Installation

Installing a Terraform version can be done in a few ways:

### Install the latest stable release

```sh
tfversion install --latest
```

### Install a specific version

```sh
tfversion install 1.7.4
```

### Install the latest pre-release

```sh
tfversion install --latest --pre-release
```

### Install the required version for your current directory

```sh
tfversion install --required
```

## Use

Once you have installed a Terraform version, you can activate it with the `use` command.

### Use the latest stable release

```sh
tfversion use --latest
```

### Use a specific version

```sh
tfversion use 1.7.4
```

### Use the latest pre-release

```sh
tfversion use --latest --pre-release
```

### Use the required version for your current directory

```sh
tfversion use --required
```

## List

If you're curious which Terraform versions are available or installed, you can use the `list` command.

### List all available versions

```sh
tfversion list
```

### List all installed versions

```sh
tfversion list --installed
```

## Uninstall

If you want to remove a Terraform version, you can use the `uninstall` command.

### Uninstall a specific version

```sh
tfversion uninstall 1.7.4
```
