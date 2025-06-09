Ansible Webserver Setup Project

This project demonstrates infrastructure automation using Ansible. It sets up an Apache2 web server on an Ubuntu client VM, deploys a webpage, configures permissions, and verifies the service, showcasing real-world DevOps skills for configuration management.

Features





Ansible playbook to automate Apache2 setup.



Custom webpage served by Apache2.



Organized with Ansible roles for modularity.



Tested on Ubuntu VMs using VMware Player.



Professional GitHub documentation.

Prerequisites





Two Ubuntu 24.04 LTS VMs (control node and client)



Ansible installed on the control node



Git



GitHub account



VMware Workstation Player for Windows users

Setup Instructions





Clone the repository:

git clone https://github.com/your-username/ansible-webserver.git
cd ansible-webserver



Copy the ansible-webserver folder to the control node VM.



Update inventory.ini with the client VM’s IP:

[webservers]
<client-IP> ansible_user=user ansible_ssh_private_key_file=/home/user/.ssh/id_rsa



On the control node, test connectivity:

ansible -i inventory.ini webservers -m ping



Run the playbook:

ansible-playbook -i inventory.ini playbook.yml



Verify the webpage:





On the client VM, open a browser and visit http://localhost.



From the host, use the client VM’s IP (e.g., http://<client-IP>).

Project Structure





playbook.yml: Main Ansible playbook.



inventory.ini: Defines target hosts.



roles/webserver/: Role for Apache2 setup.





tasks/main.yml: Installs Apache2, deploys webpage, ensures service is running.



templates/index.html.j2: Webpage template.



.gitignore: Excludes logs and Python files.

Challenges Faced





Set up Ansible on Ubuntu control node.



Configured SSH key-based authentication between VMs.



Learned Ansible playbook and role structure.



Debugged Apache2 service issues on the client VM.

Future Improvements





Add variables for dynamic webpage content.



Expand to multi-node setups (e.g., load balancer).



Integrate with cloud providers like AWS.

Author





Your Name (GitHub)



Connect on LinkedIn