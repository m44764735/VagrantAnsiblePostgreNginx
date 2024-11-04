# Deploy PostgreSQL, Nginx and Semaphore

### This playbook deploy PostgreSQL, Nginx and Semaphore (Dockered) to Vagrant VM use Ansible

1. System requirements to use this playbooks: Linux (like Ubuntu), Vagrant VM and Ansible
2. Download this repo
```
git clone https://github.com/m44764735/VagrantAnsiblePostgreNginx.git
```
3. Enter folder
```
cd VagrantAnsiblePostgreNginx/
```
4. Look and check
   
| File | Description |
| --- | --- |
| Vagrantfile | Main playbook to run Vagrant VM |
| install_ansible.yml | Main playbook to install PostgreSQL, Nginx and Semaphore |
| file/proxy.conf | File contains proxy server settings for nginx |
| requirements.yml | File with link to ansible role geerlingguy.postgresql |
| vars.yml | File with variable for postgresql |
| README.md | "Readme" file |

 5. Change in **Vagrantfile** network interface name, from "enp8s0" to your
 6. Change in **vars.yml** and **Vagrantfile** passwords to DB and admin access to Semaphore
7. Run VM
```
vagrant up
```
8. Wait ~3 min, after deploy in the last step playbook you see IPv4 address to connect Semaphore

   ![image](https://github.com/user-attachments/assets/e7b2a712-4075-4a9a-8de6-1fdd1ce9a267)
9. Open browser and go. Enter password from step 6. Default username "admin" password "12345678"
   ![image](https://github.com/user-attachments/assets/555b0fae-a691-4531-a8f2-bd9c0441f0aa)

