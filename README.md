# Use terraform 0.13 version for this code

# Change the following lines
ami_id                   = "ami-0be2609ba883822ec" 
subnet_id                = "subnet-00f80855f5d558926"
vpc_id                   = "vpc-0bbb668bb87fc7009"

# Terraform 0.13 version installation
wget https://releases.hashicorp.com/terraform/0.13.0/terraform_0.13.0_linux_amd64.zip

unzip

sudo mv terraform /bin/terraform_0.13.0

# Terraform apply process
terraform init

terraform plan -var-file configurations/regions/us-east-1.tfvars

terraform apply -var-file configurations/regions/us-east-1.tfvars

terraform destroy -var-file configurations/regions/us-east-1.tfvars
