# tomcat-webapp-stack
This challenge for deploying tomcat web app on ec2 using terraform (IAAC). 

To deploy this application we are using below tools:
1. Ansible -:  Using to setup nginx and tomcat with deploy war file on running EC2.
2. Terraform -: Using to provision EC2 on AWS where tomcat web app will be deployed.


We are able to do below tasks:
1. Spin up a WebServer of your choice : Nginx
2. Deploy the WAR file located in the directory assets named devopschallenge.war : Tomcat 
3. Manage and Install a Reverse Proxy with SSL: Self Signed Certificate
4. Write Unit and Integration Tests : Using Molecule

## How to Deploy code:

To deploy tomcat Webapp on ec2 kindly clone the mentioned repo and run below commands to to init, plan and deploy.


Keeping the setup very basic. EC2 instance will launch in AWS AP-South(Mumbai) region in a Default VPC.
Using FreeTier Amazon EC2

### Run following commands in order
```
1) git clone https://github.com/manukoli1986/terraform-ec2-launch.git
2) terraform init  (Initialize a new or existing Terraform configuration)
3) terraform plan  (Generate and show an execution plan)
4) terraform apply (Builds or changes infrastructure)
```
You can access webapp using below URL.

URL:- "https://<Public IP>/hello"

i.e. - It will automatically download ansible playbook and deploy the tomcat stack on EC2.

Logging info can be found in the Debugging Terraform section of the documentation and I would encourage you to turn it on when running locally. The information is valuable and more helpful than what is written out during plan or apply. Below are the instructions for enabling the logging on both Windows and Linux. I will be setting mine to TRACE, but know that you can set it to DEBUG, INFO, WARN, or ERROR. I have chosen to use the most verbose setting as I don't want to have to rerun commands when I hit an issue just to debug.
```
$ export TF_LOG="DEBUG"
$ export TF_LOG_PATH="terraform.txt"
$ terraform apply
```


###Task Done By:
- Mayank Koli
