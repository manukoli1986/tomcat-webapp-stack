# tomcat-webapp-stack
This challenge for deploying tomcat webapp using ansible playbook on ec2 using terraform(use https://github.com/manukoli1986/terraform-ec2-launch.git) but if you are only cloning ansible code then below steps need to be followed. 

### Run following commands in order
```
1) git clone https://github.com/manukoli1986/tomcat-webapp-stack.git
2) ansible-playbook tomcat-webapp-stack/site.yaml --connect=local &> ansible.log (Initialize a new or existing Terraform configuration)
```
You can access webapp using below URL.

URL:- "https://<Public IP>/hello"

i.e. - It will automatically install and setup Nginx with SSL and tomcat and deploy webapp in webapp folder.



To deploy this application we are using below tools:
1. Ansible -:  Using to setup nginx and tomcat with deploy war file on running EC2.
2. Terraform -: Using to provision EC2 on AWS where tomcat web app will be deployed.


We are able to do below tasks:
1. Spin up a WebServer of your choice : Nginx
2. Deploy the WAR file located in the directory assets named devopschallenge.war : Tomcat 
3. Manage and Install a Reverse Proxy with SSL: Self Signed Certificate
4. Write Unit and Integration Tests : Using Molecule



###Task Done By:
- Mayank Koli
