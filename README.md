# Example: Module with Terraform

Modules are containers for multiple resources that are used together. [See documentation](https://www.terraform.io/docs/language/modules/sources.html) 

In this example will call one module to create 2 different resources. 

# Prerequisites

## Install terraform  
See the following documentation [How to install Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli)

# How to

1. Clone the repository to your local machine
```
git clone https://github.com/munnep/module
```
2. Change your directory
```
cd module
```
3. Terraform initialize
```
terraform init
```
5. Terraform plan
```
terraform plan
```
6. Terraform apply
```
terraform apply
```
7. Sample output
```
...
...
...
  # module.random.random_pet.pet will be created
  + resource "random_pet" "pet" {
      + id        = (known after apply)
      + length    = 2
      + separator = "-"
    }

  # module.random.random_string.string will be created
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

