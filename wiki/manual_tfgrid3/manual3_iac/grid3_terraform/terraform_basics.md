## terraform basics

please make sure to read [What you need to know before getting started](grid3_developer_basics)

- make a directory for your project `mkdir myfirstproject`
- `cd myfirstproject`
- to initialize the repo `terraform init`

- create `main.tf`  <- creates the terraform main file 

```terraform
terraform {
  required_providers {
    grid = {
      source = "threefoldtech/grid"
    }
  }
}

provider "grid" {
    mnemonics = "FROM THE CREATE TWIN STEP"
    network = "dev" # or test to use testnet
}

... MORE TO BE ADDED
```
- all provider input variables and their description can be found [here](https://github.com/threefoldtech/terraform-provider-grid/blob/development/docs/index.md)
- capitalized environment variables can be used instead of writing them in the provider (e.g. MNEMONICS)

- to execute a terraform file `terraform apply -parallelism=1`
- to see the output `terraform output`
- to see the state `terraform showstate`
- to destroy `terraform destroy -parallelism=1`

