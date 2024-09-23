# AWS CloudSecurity Challenge Level 1
Hey, my name is David. I am excited to present to you a challenge to get familiar with AWS and its services.

In this github repo, I'll walk you through how to setup a 3 tier web architecture with nginx, wordpress and mysql as a standalone VM.

## How to setup a 3 tier web architecture with nginx, wordpress and mysql at AWS

## Prerequisite
1. # setup aliases
```ruby
alias k=kubectl; alias tf="terraform"; alias tfa="terraform apply --auto-approve"; alias tfd="terraform destroy --auto-approve"; alias tfm="terraform init; terraform fmt; terraform validate; terraform plan"
```
2. # https://developer.hashicorp.com/terraform/install
Install if running at cloudshell
```ruby
sudo yum install -y yum-utils shadow-utils; sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo; sudo yum -y install terraform
```
