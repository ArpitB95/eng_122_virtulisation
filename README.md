### Virtualisation Dependencies:

- In order to setup a virtual machin in local system, we need to install following in our system

 1) Ruby
- https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-2.6.6-1/rubyinstaller-devkit-2.6.6-1-x64.exe  (For windows)

2) Vagrant
- https://www.vagrantup.com/downloads  (For windows)

3) Virtual Box
- https://www.virtualbox.org/wiki/Downloads 

- Check ruby vesrion

<img width="326" alt="Ruby version" src="https://user-images.githubusercontent.com/110182832/184233129-7533fffe-aa33-4d85-90b5-f862d7e06e79.png">


- Check vagrant version

<img width="205" alt="vagrant version" src="https://user-images.githubusercontent.com/110182832/184233171-854a2a14-bf67-4ec0-acd1-3318dc0f2673.png">



## What is Dev env & benefits
- A DevOps environment is the virtual environment where developers run their code and dependencies for their testing.
- A development environment is the collection of processes and tools that are used to develop the source code for a program or software product. This involves the entire environment that supports the process end to end, including development, staging and production servers.

### Benefits of DevOps
- Faster, better product delivery.
- Faster issue resolution and reduced complexity.
- Greater scalability and availability.
- More stable operating environments.
- Better resource utilization.
- Greater automation.
- Greater visibility into system outcomes.
- Greater innovation.
  
  
### vagrant and virtual box
- Vagrant is an open-source tool that allows you to create, configure, and manage boxes of virtual machines through an easy to use command interface. Essentially, it is a layer of software installed between a virtualization tool (such as VirtualBox, Docker, Hyper-V) and a VM
  
### virtualisation ?
- Virtualization relies on software to simulate hardware functionality and create a virtual computer system
- This enables IT organizations to run more than one virtual system – and multiple operating systems and applications – on a single server. The resulting benefits include economies of scale and greater efficiency.
  
### Creating a vagrant file / creating a virtual setup

<img width="481" alt="virtualisation-mkdir step" src="https://user-images.githubusercontent.com/110182832/184233736-2c58d16c-27bd-4182-bf06-acfd07ba5795.png">



### How to start VM ?
- Open terminal in VS code
- Run following commands
- vagrant up
- vagrant status
- vagrant ssh 
- Now you'll enter into the VM, you'll see 'vagrant@ubuntu -xenial:~$'




### Linux Basic Commands

- How can we find out name of os 'uname'  or 'uname -a'
- how to create a file in linux
-  'touch filename' or 'nano filename'
-  How to check existing file/folders 'ls' or 'ls -a'
-  How to create a folder
-  'mkdir foldername'

- How to navigate inside the folder
- 'cd foldername'


- How to come out of folder or 1 step back
- 'cd ..'

- How can we check our current location or where am I ?  'pwd'
- whoami

- How to copy file  'cp filename destination' or 'cp filename_with_absolute_path destination_with_absolute_path'


- How to remove file 'rm -rf file/folder_name'


- How to cut paste the file or move the test file inside linux_commandsfolder
- 'mv /path/from/file name /path/to/folder_name'

- How to check all processes 'top' and 'ps aux'
- Find out how to remove/delete/kill processs


- How to use root user 'sudo su' or 'sudo i'

- How to use '|'  pipe

- How to check file permission 'll'
- Change file permission 'chmod permission filename'
- 'r' or 'w' or 'rw' 'all' also numbers '400' or '600' for all'700'

- update our ubuntu OS  'apt-get update'
- upgrade our ubuntu os 'apt-get upgrade' or 'sudo apt-get upgrade -y'

- 'cat filename'
- to run provision.sh  './provision.sh'


- How to create automate tasks with provisioning scripts
- Automate update and upgrade 

- How to kill/terminate process in linux?
- First find the process id to kill that process by running 'ps -fu user'
- The process id will be displayed in the first column of the output
- Then run 'kill [signal-number pid]


### Task:
### Steps to create automate task with provisioning script
### which includes automate update and upgrade

- You'll be in your localhost 
- To turn on the VM run command 'vagrant up'
- Then to establish the contact with VM and localhost run command 'vagrant ssh'
- Now you'll be in your VM (vagrant@ubuntu-xenial:~$)
  
  - Now create a file name provision.sh using sudo command
  -  sudo nano provision.sh
  -  Now, write a script inside the file then ctrl+x to save and then Y and press enter to exit the file
  -  To check the content of file run 'cat filename' here it's 'cat provision.sh'
  
  
  - <img width="315" alt="script to automate upgrade and update" src="https://user-images.githubusercontent.com/110182832/184183414-9f4b654c-9323-468d-8529-c59674aea7e6.png">



  
  
  -  Now run 'll' command to check the file permission
  -  It doesn't have executable permission  (the file name will appear in white color)
  -  run 'sudo chmod +x filename' to change the file permission (Here it would be 'sudo chmod +x provision.sh')
  -  After running the command you'll see file name in green color which means it's executable
  -  To run the file run command './filename' (Here './provision.sh' if there's permission issue then use 'sudo ./  permission.sh)
  -  Enter 'exit' to come out of VM and back to the localhost



### Installation of NGINX
Install nginx 'sudo apt-get install nginx -y'
- How to check if it's installed/working 'sudo systemctl status nginx'

- How to restart a process  -in this case it's an nginx
- Restart or start 'sudo systemctl restart nginx'
- enable the process 'sudo systemctl enable nginx'
