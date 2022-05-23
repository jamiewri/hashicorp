![Screenshot](img/splash.jpg)
> Photo by [Gabriel Menchaca](https://unsplash.com/gabrielmenchaca) on [Unsplash](https://unsplash.com)

# HashiCorp workflows and demos
A collection of links to my HashiCorp demos, resources, and other scripts I use.

# Table of contents
1. [Packer](#packer)
2. [Terraform](#terraform)
3. [Terraform Cloud](#terraform-cloud)
4. [Vault](#vault)
5. [Consul](#consul)
6. [Golang](#golang)
7. [Scripts](#scripts)

## Packer <a name="packer"></a>
#### [Library of Packer examples](https://github.com/jamiewri/packer-by-example)
Working examples of Packer configurations including, Ansible, Windows and CentOS

## Terraform <a name="terraform"></a>

### Examples

#### [Common Terraform patterns](https://github.com/jamiewri/tf-common-patterns)
Referenceable code snippets for common Terraform logic. Include reading and merging JSON from a file.

### Modules

#### [Terraform Cloud/Enterprise Workspace](https://github.com/jamiewri/terraform-tfe-workspace)
This module uses a custom data structure called workspaces to manage terraform cloud workspaces and the team access model. See [Terraform Cloud Workspace](https://github.com/jamiewri/tfc-management) automation for usage.

## Terraform Cloud <a name="terraform-cloud"></a>

#### [Workspaces and teams automation](https://github.com/jamiewri/tfc-management)
The automated deployment of Terraform Cloud workspaces, including tags, and teams.

#### [API driven workflow from your CICD pipeline](https://github.com/jamiewri/terraform-cloud-connect)
Create, run and destroy infrastructure in Terraform Cloud from a CICD pipeline. Including GitLab CI example.

#### [tfctl - a CLI tool for tag based orchestration of Terraform Cloud](https://github.com/jamiewri/tfctl)
A CLI tool for interacting with mutliple Terraform Cloud workspace at the same time based on tags. For example, 'Start a destory plan on all workspaces that match the tags `demo` and `azure`. Built using the official [Golang SDK](https://github.com/hashicorp/go-tfe) for Terraform Cloud/Enterprise.

## Vault <a name="vault"></a>

### Workflows

#### [KMS Secrets Engine](https://github.com/jamiewri/snapshot-vault-kms)
Example KMS secrets engine workflows for AWS, Azure, and Google Cloud. Configure the Vault KMS secrets engine to generate key material locally then push it to any one of the available public cloud providers.

#### [Transit Secrets Engine](https://github.com/jamiewri/vault-transit-workflows)
Example Transit secret engine workflows. Including generating key material outside of Vault and then importing it into Vault.

#### [Vault auto-init sidecar](https://github.com/jamiewri/vault-auto-init)
A sidecar for working with Vault in a environment. Useful for deploying demos quickly.

### Testing
#### [Non-functional testing of the Transit secrets engine](https://github.com/jamiewri/vault-loadtester)
Use Python to run a mutli-threaded non-functional test of Vaults Transit secret engine and output performance statistics.

#### [Functional testing of KMIP secrets engine](https://github.com/jamiewri/vault-kmip-secrets-engine-client-test)
Use Python to functionally test operations in Vault KMIP secret engine. Including a parsable JSON output.

## Consul <a name="consul"></a>

#### [Service discovery on Google Cloud](https://github.com/jamiewri/consul-service-discovery)
Use Packer and Ansible to build immutable Consul, Web, and Bastion server images. Deploy them into Google Cloud and show Consul auto discovering and health checking the web servers.

#### [Dynamically configure Nginx for Blue/Green Deployments](https://github.com/jamiewri/consul-snapshot-blue-green-deployments)
Use Docker and Python to build 2 containerised web applications. Then deploy Consul and programmatically render an Nginx configuration based on Consul service discovery.

## Golang <a name="golang">
#### [Searching Terraform Cloud from the CLI](https://github.com/jamiewri/terraform-cloud-tag-orchestration)
Example usage of the  Create a CLI tool that searches Terraform Cloud workspaces based on provided tags. Built using the official [Golang SDK](https://github.com/hashicorp/go-tfe) for Terraform Cloud/Enterprise.

## Scripts <a name="scripts"></a>
#### [Doormat-cli automation](https://github.com/jamiewri/doormat-cli-automation)
Bash wrapper i used around doormat and tecli for starting demos quickly.
