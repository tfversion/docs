# Install

Installing a Terraform version can be done in a few ways.

## Specific version

You can install a specific version by calling the `install` command with a version number.

```sh
tfversion install 1.7.4
```

## Latest stable

If you just want the latest stable version, you can use the `--latest` flag.

```sh
tfversion install --latest
```

## Latest pre-release

If you want to experiment with the latest pre-release version, you can use the `--pre-release` flag.

```sh
tfversion install --latest --pre-release
```

!!! warning
    When using `--pre-release`, you must always add `--latest` as well.

## Required version

If you have specific a `required_version` in any Terraform (`.tf` or `.hcl`) file in the current working directory, you can install the latest matching version automatically by using the `--required` flag.

```sh
tfversion install --required
```

!!! note
    `tfversion` uses the first Terraform file with a `required_version` in it.
    If you have multiple, the others will be ignored.

## Uninstall

After upgrading all your codebases to a more recent version of Terraform, you might want to uninstall old versions.
For this you can use the `uninstall` command.

```sh
tfversion uninstall 1.7.4
```

!!! warning
    `tfversion` does not check if an alias to a version exists when uninstalling.
    Uninstalling a version with active aliases will cause that alias to break as well.
