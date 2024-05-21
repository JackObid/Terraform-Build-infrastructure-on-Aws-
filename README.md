# Using Terraform to build-Infrastructure-on-Aws
Using Terraform to provision an EC2 instance on Amazon Web Services (AWS)

## Prerequisites
```Terraform CLI (1.2.0+)``` ```Gitbash``` ```Chocolatey``` ```VSCode``` ```The AWS CLI```


### Actions
1. Initially download and install ```Gitbash``` ```Chocolatey``` ```VSCode``` ```The AWS CLI```
   
   
2. Install terraform using Chocolately
   
 ``` $ choco install terraform ```
 

3. Use your IAM credentials to authenticate the Terraform AWS provider by setting up the AWS_ACCESS_KEY_ID environment variable.

```$ export AWS_ACCESS_KEY_ID=```

```$ export AWS_SECRET_ACCESS_KEY=```


4. Create the test folder
   
```$ mkdir terraform-folder```

```$ cd terraform-folder```


5. Create the main.tf file for the terraform configuration 
   
```$ touch main.tf```


6. Open VSCode to Paste and update the terraform configuration
  ```
  terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "5.50.0"
    }
  }

  required_version = ">= 1.2.0"
}

provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "app_server" {
  ami           = "ami-08d70e59c07c61a3a"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
    }
  }

```


7. Save and Initialize the directory

```$ terraform init```


8. Format and validate the configuration

```$ terraform fmt```

```$ terraform validate```


9. Create the infrastructure on Aws with the terraform apply command
    
```$ terraform apply```

10. Type ```yes``` at the confirmation prompt to proceed


> [!NOTE]
> You can use VSCode or Gitbash to apply the terraform as long as your in the folder.
> 
