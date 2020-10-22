## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.
 

(https://github.com/CyberZ33k/Silo/blob/main/Diagrams/Diagram_layout_West_East%20VN.jpg)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _ my-playbook.yml file may be used to install only certain pieces of it, such as Filebeat.

  the _ my-playbook2.yml

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly efficient, in addition to restricting downtime to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system metrics.
- _TODO: What does Filebeat watch for?_
- _TODO: What does Metricbeat record?_

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.




| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   |  Linux (ubuntu 18.04)             |
| Web-1     |    ssh      |  10.0.0.5          |  Linux (ubuntu 18.04)               |
| Web-2     |  ssh       |   10.0.0.6         |      Linux (ubuntu 18.04)             |
| Web-3     |    ssh     |     10.0.0.8       |    Linux (ubuntu 18.04)              |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the JumpBox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_
My Jumpbox Ip address and my laptop.

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 52.160.121.111    |
|    Web-1        |           No          |     10.0.0.5            |
|      Web-2     |         No            |        10.0.0.6              |
|      Web-3     |         No            |        10.0.0.8              |
|      Web-1.1 (elk)     |        yes           |      53.188.11.30      |





### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_
The main advantage is that you can set the command so when it starts up its the same so It saves time to focus on other things. 

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
It Installs Apache
Second it increases the memory
Third it installs the docker .io
Fourth it runs the python  pip file in th edocker
Fifth Installs docker pip file
Sixth it installs Elk docker container
Then starts docker service

- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

**Note**: The following image link needs to be updated. Replace `docker_ps_output.png` with the name of your screenshot image file.  https://github.com/CyberZ33k/Silo/blob/main/Examples/docker_ps_output.png


![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_
10.0.0.5, 10.0.06, 10.0.08

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_
Metricbeat and Filebeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook?  ansible-playbook metricbeat-playbook.yml Where do you copy it?_ in the Ansible folder
- _Which file do you update to make Ansible run the playbook on a specific machine? You tell it in the .yml file the command you want to send. How do I specify which machine to install the ELK server on versus which to install Filebeat on?_ you choose the container you want and start and attach
- _Which URL do you navigate to in order to check that the ELK server is running?
http://52.188.10.25:5601/app/kibana#/home

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._



