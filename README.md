## What is Dev env & benefits
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
  -  Now run 'll' command to check the file permission
  -  It doesn't have executable permission  (the file name will appear in white color)
  -  run 'sudo chmod +x filename' to change the file permission (Here it would be 'sudo chmod +x provision.sh')
  -  After running the command you'll see file name in green color which means it's executable
  -  To run the file run command './filename' (Here './provision.sh' if there's permission issue then use 'sudo ./  permission.sh)
  -  Enter 'exit' to come out of VM and back to the localhost