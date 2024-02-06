# Tanzu Catalog of Supply Chain Components

Inputs and outputs comply with [Idioms](idioms.hbs.md)

Components:

Inputs and Outputs are formatted `name[type]` where name is the default name.

| Type                                  | Description                                                                  | Inputs       | Outputs        |
|---------------------------------------|------------------------------------------------------------------------------|--------------|----------------|
| [conventions](conventions.hbs.md)     |                                                                              | image[image] | gitops[gitops] |
| [git-writer](git-writer.hbs.md)       | Write a package as a commit to a branch.                                     |              |                |
| [git-writer-pr](git-writer-pr.hbs.md) | Write a package as a commit to a new branch and create a Pull/Merge request. |              |                |
