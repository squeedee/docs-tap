# Tanzu Catalog of Supply Chain Components

* [Aggregator](#aggregator)


## Aggregator

- Name: `aggregator`
- Purpose: Constructs configuration from a series of inputs
- 



| Type                                          | Description                                                                  | Inputs                                                           | Outputs                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|
| [aggregator](aggregator)                      | Constructs configuration from a series of inputs.                            | oci-yaml-files[oci-yaml-files]<br/> oci-ytt-files[oci-ytt-files] | config[config]                                                   |
| [app-config-server](app-config-server.hbs.md) | Generates a server workload template from a config bundle.                   | conventions[conventions]                                         | oci-yaml-files[oci-yaml-files]<br/> oci-ytt-files[oci-ytt-files] |
| [app-config-web](app-config-web.hbs.md)       | Generates a web workload template from a config bundle.                      | conventions[conventions]                                         | oci-yaml-files[oci-yaml-files]<br/> oci-ytt-files[oci-ytt-files] |
| [app-config-worker](app-config-worker.hbs.md) | Generates a worker workload template from a config bundle.                   | conventions[conventions]                                         | oci-yaml-files[oci-yaml-files]<br/> oci-ytt-files[oci-ytt-files] |
| [carvel-package](carvel-package.hbs.md)      |                                                                              |                                                                  |                                                                  |
| [conventions](conventions.hbs.md)             |                                                                              | image[image]                                                     | gitops[gitops]                                                   |
| [git-writer](git-writer.hbs.md)               | Write a package as a commit to a branch.                                     |                                                                  |                                                                  |
| [git-writer-pr](git-writer-pr.hbs.md)         | Write a package as a commit to a new branch and create a Pull/Merge request. |                                                                  |                                                                  |
|                                               |                                                                              |                                                                  |                                                                  |
|                                               |                                                                              |                                                                  |                                                                  |

carvel-package-1.0.0             alm-catalog                 Generates a carvel package from a config bundle                                   False        oci-yaml-files[oci-yaml-files], oci-ytt-files[oci-ytt-files]  package[package]                                              11h
deployer-1.0.0                   alm-catalog                 Generates a carvel package from a config bundle                                   False        package[package]                                              <none>                                                        11h
source-package-translator-1.0.0  alm-catalog                 Takes the type source and immediately outputs it as type package. In the          False        source[source]                                                package[package]                                              11h
future, will be replaced by input type mapping or some similar feature.
conventions-1.0.0                conventions-component       Use the Cartographer Conventions service to generate decorated pod template       False        image[image]                                                  conventions[conventions]                                      11h
specs
git-writer-1.0.0                 git-writer-catalog          Writes carvel package config directly to a gitops repository                      False        package[package]                                              gitops[gitops]                                                11h
git-writer-pr-1.0.0              git-writer-catalog          Writes carvel package config to a gitops repository and opens a PR                False        package[package]                                              gitops[gitops]                                                11h
source-git-provider-1.0.0        source-provider             Monitors a git repository                                                         True         <none>                                                        source[source], git[git]                                      11h
buildpack-build-1.0.0            tbs-catalog                 Builds an app with buildpacks using kpack                                         True         source[source], git[git]                                      image[image]                                                  11h
trivy-image-scan-1.0.0           trivy-app-scanning-catalog  Performs a trivy image scan using the scan 2.0 components                         False        image[image], git[git]                                        <none>                                                        11h


Notes:

* Inputs and Outputs are formatted `name[type]` where name is the default name.
* Inputs and outputs comply with [Idioms](idioms.hbs.md)
