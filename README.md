# Using Terraform to build-Infrastructure-on-Aws-
Using Terraform to provision an EC2 instance on Amazon Web Services (AWS)

# Prerequisites
```Terraform CLI (1.2.0+)``` ```Gitbash``` ```Chocolatey``` ```VSCode``` ```The AWS CLI```


1. Initially download and install ```Gitbash``` ```Chocolatey``` ```VSCode``` ```The AWS CLI```
   
2. Install terraform using Chocolately
   
 ``` $ choco install terraform ```

3. Use your IAM credentials to authenticate the Terraform AWS provider by setting up the AWS_ACCESS_KEY_ID environment variable.

```$ export AWS_ACCESS_KEY_ID=```

```$ export AWS_SECRET_ACCESS_KEY=```

4. Create the test folder
   
```$ mkdir terraform-folder```

```$ cd terraform-folder```

5. Create the main.tf
   
   ```touch main.tf```
