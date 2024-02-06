# `git-writer` Component

The `git-writer` component writes Carvel package configuration to a Git repository.
This component will create a commit on the specified branch. If you want to create a
Pull/Merge Request, use the [git-writer-pr](./git-writer-pr.hbs.md) component.

## Inputs

### [package[package]](./idioms.hbs.md#package)
The package to commit to the Git Repository. The component is agnostic of the packaging format and commits all files in the package input. 

## Outputs

### [gitops[gitops]](./idioms.hbs.md#gitops)

## Secrets

Ensure an appropriate secret is added to the service account to allow for Git authentication. ???

## Configuration

```console
spec:
  # required
  gitOps:
    # https URL of the git repository 
    # required 
    url: <gitops repository url> 
    
    # branch to commit to
    # required ??     
    branch: <branch to commit to>
    
    # subpath within the repository to write to
    # required ??
    subPath:
```
