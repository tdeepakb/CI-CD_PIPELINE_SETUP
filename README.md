# CI-CD_PIPELINE_SETUP

**COMPANY**: CODTECH IT SOLUTIONS

**NAME**: DEEPAK PRASAD

**INTERN ID**: CT6WGAP

**DOMAIN**: DEVOPS

**DURATION**: 6 WEEKS

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
i want to built a ci pipeline using jenkins. jenkins will interact with github because git hub code is uploaded
at github. my code is in java so java must be installed here. it is written in maven.
so build automation tool maven must installed here.
if anything you want to change in jenkins you have to go to manage jenkins option.
now first we will go to managed jenkins here i will click on 'tool' option.
here java, git i have already installed so i will click maven add maven option
latest version i will select and apply & save.
now i will create job.
go to dashboard click on new item and enter name my compilejob select freestyle project.
here another tab will open and in description you can write anything related.
in source code you have to paste github repository link.
branch specifier master
build Trigger option you select github hook trigger for gitscm polling. 
set github setting you paste public ip address to here so that if you changed anything in your file
it will run.
in build steps select invoke top level maven Targets maven version mymvn in goals compile.
now apply and save. if i run compile job click on build now option. it automatically run.
now we configure for Test job
go to jenkins dashboard
click on new item
enter an item name mytestjob
in description write this is mytest job.
source code management we have git repository address link paste here.
build Trigger option you select build after other project build option.
build steps select invoke top level maven targets
maven version mymvn
goal i have to write here test
now apply and save
at last we configure for package job.
go to jenkins dashboard
click on new item
enter an item name mypackagejob
in description write this is mypackage job.
source code management we have git repository address link paste here.
build Trigger option you select build after other project build option.
build steps select invoke top level maven targets
maven version mymvn
goal i have to write here package
now apply and save
here you can see in compile job it is showing downstream job is mytest job means first compile job will run 
and then mytest job will run.
if you see mytestjob tab you will see upstream and downstream job is written there. means mycompile job is upstream job and downstream mytest job
my compile job will run first and then mytest job will run.
if you go mypackage job option you will see only upstream job is mytest job. so here first mytest job will run 
and then mypackage job will run.
here all things managed now if i will show to someone this ci/cd then i have to create all job in one page
to show all jobs running in one frame.
go to dashboard and click manage jenkins
here i will select available plugins it is like a market place.
search build pipeline its come automatically.
select and install it. plugins give you some extra features.
now go to dashboard and select build pipelin view and configure here like first job is mycompilejob
and after this all jobs run.
you can see all jobs will show in one frame.
