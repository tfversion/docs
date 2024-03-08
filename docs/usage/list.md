# List

Use the `list` command to show lists of available and installed versions.

## Available

By default, the `list` command shows all versions of Terraform available on HashiCorp servers.

```sh
tfversion list
```

## Installed

By passing the `--installed` flag, you can see all the Terraform versions that you have currently installed.

```sh
tfversion list --installed
```

## Aliases

By passing the `--aliases` flag, you can see all aliases that you created.

```sh
tfversion list --aliases
```

## Pre-releases

By default, the `list` command hides pre-release versions because they are not interesting for must use cases.
If you want to see those anyways, add the `--pre-release` flag.

```sh
tfversion list --pre-release
```

## Limiting

List can get quite long.
To show only the top items, add the `--max-results` flag.
This flag works for all options of the `list` command.

```sh
tfversion list --max-results=10
```

```sh
tfversion list --installed  --max-results=10
```
