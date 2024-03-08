# Use

To active one of the installed Terraform versions, run the `use` command in any of the following ways.

## Specific version

You can activate a specific version by calling the `use` command with a version number.

```sh
tfversion use 1.7.4
```

## Latest stable

If you want to activate the latest stable version, you can use the `--latest` flag.

```sh
tfversion use --latest
```

!!! tip
    The latest version might not be installed yet, as this is a dynamic value.
    Add the `--install` flag to automatically install it for you.

## Latest pre-release

You can activate the latest pre-release version to experiment by adding the `--pre-release` flag.

```sh
tfversion use --latest --pre-release
```

!!! warning
    When using `--pre-release`, you must always add `--latest` as well.

## Required version

You can activate the required version for your current working directory by adding the `--required` flag.

```sh
terraform use --required
```

Read more details about how `--required` works at the [install instructions](install.md#required-version).

## Automatically install

To automatically install a missing version when activating, add the `--install` flag.

```sh
tfversion use 1.7.4 --install
```

```sh
tfversion use --latest --install
```

This is especially handy for options that result in an unknown version number, like `--latest`, `--pre-release` and `--required`.
