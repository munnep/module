# Example: Module with Terraform

Modules [See documentation](https://www.terraform.io/docs/language/modules/sources.html) 


# Prerequisites

## Install terraform  
See the following documentation [How to install Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli)

# How to

1. Create terraform file that uses this repo as module
```
module "mymodule" {
  source = "github.com/munnep/module"
}
```
2. Terraform initialize
```
terraform init
```
3. Terraform plan
```
terraform plan
```
4. Terraform apply
```
terraform apply
```
5. Sample output
```
...
...
...
  # module.mymodule.random_pet.pet will be created
  + resource "random_pet" "pet" {
      + id        = (known after apply)
      + length    = 2
      + separator = "-"
    }

  # module.mymodule.random_string.string will be created
  + resource "random_string" "string" {
      + id          = (known after apply)
      + length      = 16
      + lower       = true
      + min_lower   = 0
      + min_numeric = 0
      + min_special = 0
      + min_upper   = 0
      + number      = true
      + result      = (known after apply)
      + special     = true
      + upper       = true
    }

Plan: 2 to add, 0 to change, 0 to destroy.
```

