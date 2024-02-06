# Idioms

## API Fields And Labels

## Output Types

### `source`

`URL` points to a GET endpoint for a tarball of the complete source.

**Note**: You cannot assume it comes with metadata such as a `.git` folder.

### `git`

The git metadata of a repository. What you would commonly find in the `.git` folder

### `conventions`

A Pod Spec Template including the reference image input and decorated by any Convention servers configured on the
cluster.

### `gitops`

- `url`: to the pull request (`git-writer-pr`), or the repository (`git-writer`)
- `digest`: SHA of the git commit.

Todo: this "or" feels problematic. I think it should be

```
### `git-pr`

- `url` URL to the pull request
- `digest` SHA of the HEAD commit.
```

and

```
### `git-commit`

- `url` URL to the commit
- `digest` SHA of the commit.
```

This might be trouble downstream without other features

### `package`

?? Tarball? Tgz? OCI??