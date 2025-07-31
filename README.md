# A Subissue Extension for `gh`

This `gh` extension lets you assign one Github issue as a sub-issue of another:

```sh
gh subissue 123 245
```

Will make the issue 245 of the current Github repository a sub-issue of issue 123.

# Install

```sh
gh extension install jacobo-doist/gh-subissue
```

# Passing issues

Issues can be passed as URLs or as issue numbers. When both the parent and the child issue are passed as numbers, the repository will be inferred from the current working directory, but it can also be explicitly givven with the `--repo` flag.

## Replaing an existing parent issue

If a child issue is already a sub-issue of another parent, you can use the `--force` flag to move it to a new parent:

```sh
gh subissue --force 456 245
```

This will remove issue 245 from its current parent and make it a sub-issue of issue 456.
