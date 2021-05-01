# GW-Cybersecurity
*Repository for GW Cyber file
​
## Automated ELK Stack Deployment
​
The files in this repository were used to configure the network depicted below.
​
​
https://github.com/cse230/GW-Cybersecurity/blob/main/Ansible/RedTeam-Net-Diagram.png
​
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.
​
https://github.com/cse230/GW-Cybersecurity/blob/main/Ansible/filebeat-playbook.yml
​
This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build
​
​
### Description of the Topology
​
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.
​
Load balancing ensures that the application will be highly versitile, in addition to restricting connections to the network.
Load balancer will help to balance the network traffice as 
​
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _____.
- _TODO: What does Filebeat watch for?_
- _TODO: What does Metricbeat record?_
​
The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.
​
| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| Load Bal | Gateway  | 10.1.0.4   | Linux            |
| ELK      | Server   | 10.0.0.5   | Linux            |
| Web2     | DVWA     | 10.0.0.6   | Linux            |
​
### Access Policies
​
The machines on the internal network are not exposed to the public Internet. 
​
Only the Jumpbox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- The creator ip address
​
Machines within the network can only be accessed by internal IP address from jumpbox.
Only jumpbox machine can enters ELKmachine via SSH
​
A summary of the access policies in place can be found in the table below.
​
| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | Owner's IP           |
| Web1     |  NO                 | 10.0.0.4/10.1.0.4    |
| Web2     |  NO                 | 10.0.0.4/10.1.0.4    |
| Load Bal |  YES                | ANY from public      |   
| ELK      |  NO                 | 10.0.0.4             |                
​
### Elk Configuration
​
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
-automating configuration can assist with setting up multiple machine at once thus reduce the time to set-up each individual machine. 
​
The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- install dokcer
- install python3
- install docker module
- use more memory
- download and launch dokcer elk container
- enable service docker on boot
​
The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.
​  
​
​
![image](https://user-images.githubusercontent.com/77525758/116796080-c8335600-aaa7-11eb-8ac7-e3d7f1b73f22.png)
​
### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- 10.0.0.5
- 10.0.0.6
​
We have installed the following Beats on these machines:
- webservers using metricbeat-7.4.0-amd64.deb***
​
### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 
​
SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.
​
_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?
​
