# Sample Application to test ephemreal environments


## Initial Sample Application Code
This sample app is initially taken from [quickstart-spring-data-jdbc-postgresql](https://github.com/Azure-Samples/quickstart-spring-data-jdbc-postgresql) Azure Samples, and then modified for purpose of creating ephemeral test environments.

## Purpose of the Sample Application

Once setup a PR agains this repository will result in creation of a new ephemeral environment for this PR, with a new Azure Resource group which contains an AKS cluster and Postgres SQL database. A version of this application corresponding to the PR commit SHA is then deployed to this ephemeral environment. The creation of Infrastructure and application release are all done using the GitOps way.
