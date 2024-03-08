# Alias

When having multiple projects and versions installed, you don't want to remember which version you are using for which purpose (for example a client).
For this we created the `alias` command, which allows naming versions in a way that you can remember.

## Create alias

You can create an alias by using the `alias` command and passing a name and target Terraform version.

```sh
tfversion alias default 1.7.4`
```

```sh
tfversion alias my-client 1.2.3
```

## Use alias

You can activate the Terraform version behind an alias by calling `use` with an alias instead of a version number.

```sh
tfversion use my-client
```

## Remove alias

Once you're done with a project and no longer need the alias you can remove it using the `unalias` command.

```sh
tfversion unalias my-client
```

!!! warning
    `tfversion` does not check if an alias to a version exists when uninstalling.
    Uninstalling a version with active aliases will cause that alias to break as well.
