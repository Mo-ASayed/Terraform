# Terraform notes

Terraform is all about **infrastructure as code**. It helps you define your infrastructure with code so you can version, track, and deploy it easily. Here's a quick walk-through of the basics to advanced bits.

## 1. Getting Started

Start with the basic commands that you'll always use.

### `terraform init`
- **Purpose:** Prepares the working directory with the necessary plugins.
- **Run it:** First thing you do when you set up a new Terraform project.


### `terraform plan`
- **Purpose:** Checks what Terraform will do before actually doing it.
- Shows you what resources will be created, modified, or destroyed.
- **Pro Tip:** Run this often, especially before `apply`.


### `terraform apply`
- **Purpose:** Actually applies your changes to the infrastructure.
- Runs the plan and then does the work.


### Table of Basic Commands:
| Command               | Purpose                          |
|----------------------|----------------------------------|
| `terraform init`     | Sets up the environment with plugins |
| `terraform plan`     | Shows the execution plan         |
| `terraform apply`    | Executes the plan and applies changes |
| `terraform destroy`  | Tears down the infrastructure     |

## 2. Getting into Resource Blocks

Resource blocks are where you define *what* you want Terraform to manage.

`resource "aws_instance" "example" { ami = "ami-12345678" instance_type = "t2.micro" }`

- **Resource Type:** First part, `aws_instance`.
- **Name:** The second part, `"example"`, is your reference name.
- **Arguments:** Define the attributes like `ami` and `instance_type`.

The cool part? This block is declarative, so Terraform will always aim to make your infra match it.

### Variables
- You can use variables to make your configuration more flexible.
- Defined like this:
`variable "instance_type" { default = "t2.micro" }`

And used in your resource block like this: `instance_type = var.instance_type`


## 3. Moving on to Imports

Sometimes you want Terraform to manage something **already created**. Instead of recreating it, you can import it.

### `terraform import`
- **Purpose:** Bring existing resources under Terraform management.
- **Usage:** `terraform import aws_instance.example i-0123456789abcdef0`


This will import the `i-0123456789abcdef0` instance into your `aws_instance.example` resource block.

## 4. Replacing Resources

Every now and then, you might want to replace a resource entirely, for instance, when upgrading.

### `terraform taint` (old command)
Marks a resource for replacement on the next apply.


This will import the `i-0123456789abcdef0` instance into your `aws_instance.example` resource block.

## 4. Replacing Resources

Every now and then, you might want to replace a resource entirely, for instance, when upgrading.

### `terraform taint` (old command)
Marks a resource for replacement on the next apply.

`terraform taint aws_instance.example`


### `terraform apply -replace`
Modern, cleaner way to force a resource to be replaced without marking it tainted.

`terraform apply -replace="aws_instance.example"`


## 5. Modules: Keeping It DRY

As your infrastructure grows, you'll want to **reuse configurations**. That's where **modules** come in.

### Why Use Modules?
- Makes your Terraform code modular and easy to manage.
- Can reuse common patterns, like VPC creation, across multiple environments.

### Example:
Here’s how a basic module setup works: `module "vpc" { source = "./modules/vpc" cidr_block = "10.0.0.0/16" }`


- **source:** Path to the module (could be local or remote).
- **cidr_block:** A variable you're passing to the module.

Modules keep your infrastructure configuration neat and repeatable.

## 6. Advanced Command - Graph

For visual learners, Terraform has a **graph** command that shows the dependency graph of your infrastructure.

`terraform graph | dot -Tpng > graph.png`


This can give you an actual image of how your resources relate to each other.

## 7. Wrapping Up

Terraform is all about defining your infrastructure, but it’s also about making sure it’s reproducible and easy to manage. Whether you're just getting started with `plan` and `apply`, or using advanced tricks like `import`, **understanding the basics** will make your life easier.

- **Modules** help you stay DRY.
- **Plan often**, and always check what you’re about to apply.
- **Import** lets you bring in existing resources without hassle.
- Use **replace** and **taint** carefully when you want to recreate resources.
