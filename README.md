# CI-CD_PIPELINE_SETUP

**COMPANY**: CODTECH IT SOLUTIONS

**NAME**: DEEPAK PRASAD

**INTERN ID**: 

**DOMAIN**: DEVOPS

**BATCH DURATION**: DECEMBER 25th, 2024 to FEBRUARY 10th, 2025

**MENTOR NAME**: NEELA SANTHOSH

# ENTER DESCRIPTION OF TASK PERFORMED NOT LESS THAN 500 WORDS

# OUTPUT OF THE TASK
![Image](https://github.com/user-attachments/assets/c9712335-d090-4a4c-a707-d06d2aa01758)

here i am set up the pipeline of ci/cd 
first i will create or launch ec2 machine and named jenkins and take ami image ubuntu, instance type t2 micro, 
keypair selected or create keypair, in network settings we select existing group or create security group 
here i will set ssh,http and custom tcp 8080 so that jenkins will run on 8080 port only. after setting this.
configure storage of 20 gb and magnetic standard and
Launch the instance
now connect this ec2 machine to ec2 instance so that we will work on ci/cd jenkins.
first make this root user like sudo su - and it will become root user
update the machine apt-get update 
jenkins works on java language so i will install java version 17
apt-get install openjdk-17-jre it will install and after this i will install jenkins here.
here i am pasting jenkins installing websites.
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
now i will take public ip address of this ec2 machine and paste to google so that jenkins will work.
http://3.82.227.154:8080 here when i put this site jenkins page will appear here and one code is there
that code will put on ec2 instance connect page and you will get password of jenkins page. 
here you have to put your details like Name, email, password, and login to it.
install tools on jenkins like maven, java
if anything you want to change in jenkins you have to go to manage jenkins option.
now first we will go to managed jenkins here i will 
