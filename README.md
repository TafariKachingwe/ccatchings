## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

https://github.com/TafariKachingwe/ccatchings/blob/master/Images/Diagram

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the Ansible playbook file may be used to install only certain pieces of it, such as Filebeat.


This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will have high availibilty, in addition to restricting access to the network.
- Load  What is the advantage of a jump box?_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the file system and logfiles.
- File beat monitors user access of your various directories 
- Metricbeat records the cpu data, performance, and processes. 

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address  | Operating System|
|----------|----------|-------------|-----------------|
| Jump Box | Gateway  |52.146.40.181|Linux            |
| Web-1    |Web Server|10.0.0.7     |Linux            |
| Web-2    |Web Server|10.0.0.8     |Linux            |
| Web-3    |Web Server|10.0.0.9     |Linux            |
| DVWA-VM3 |Monitoring|10.1.0.5     |Linux            |
| DVWA-VM4 |Monitoring|10.1.0.4     |Linux            |
| ELK      |Monitoring|10.1.0.6     |Linux            |
### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 100.11.68.16

Machines within the network can only be accessed by the jump box.
- _TODO: Which machine did you allow to access your ELK VM? The Jumpbox What was its IP address? ELK IP: 40.70.80.20

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible| Allowed IP Addresses              |
|----------|--------------------|-----------------------------------|
| Jump Box | No                 | 172.104.3.70                      |
| Web-1    | No                 | 10.0.0.6,100.11.68.16,10.1.0.8    |
| Web-2    | No                 | 10.0.0.6,100.11.68.16,10.1.0.8    |
| Web-3    | No                 | 100.11.68.16,172.104.3.70,10.1.0.4|
| DVWA-VM3 | No                 | 100.11.68.16,172.104.3.70,10.1.0.4|
| DVWA-VM4 | No                 | 100.11.68.16,172.104.3.70,10.1.0.4|
| ELK      | Yes                | 100.11.68.16,172.104.3.70,10.1.0.4|

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

!(https://github.com/TafariKachingwe/ccatchings/blob/master/Images/Screen%20Shot%202020-09-23%20at%205.31.33%20PM.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?
