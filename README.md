
# Repository for completely isolated ephemeral environment creation solution

This repository contains resources to demonstrate the Pull Request Generator Pattern for creating ephemeral test environments.
For the sake of simplicity, instead of having multiple repositories for Application code, Infrastructure Helm Charts, and implementation bootstraping scripts, these are represented as separate folders under this repository.

## Index 

Folder  | Description  |
---|---|
[sample-app-source-repo](./sample-app-source-repo/)  | This folder represents Application Code repository, which contains the application source code, the docker file, and application manifests. PRs against this repository result in creation of the completely isolated ephemeral environment|
[environment-infra-helm-repo](./environment-infra-helm-repo/)  |This folder represents the Infrastructure repository which contains the Helm Chart to generate PR specific ephemeral environment resources, including those which will result in creation of cloud services|
[e2e-solution-setup](./e2e-solution-setup/) | This folder contains scripts to bootstrap and setup the two solution implementations of the pull request generation pattern|
[flux-pull-request-generator](./flux-pull-request-generator/)  | This folder contains source code for the **sample** PR ephemeral environment controller source code repository. **This is a sample custom controller, and is needed only for the flux based implementation.** |adding line to  markdown for testing 4
