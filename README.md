# Ansible

### Installation

```
sudo apt update
suo apt install ansible
ansible --version
```

Output: 
```
ansible [core 2.16.3]
  config file = None
  configured module search path = ['/home/ubuntu/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  ansible collection location = /home/ubuntu/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/bin/ansible
  python version = 3.12.3 (main, Mar  3 2026, 12:15:18) [GCC 13.3.0] (/usr/bin/python3)
  jinja version = 3.1.2
  libyaml = True
```

As we can see config file is null, so we need to create cfg file manually

We need to create hosts file which will contains all the info like server public ip, user name etc.

We can check the hosts configuration working or not by below command 

```
ansible -i <path/hosts> group/worker -m ping
```

<img width="617" height="182" alt="image" src="https://github.com/user-attachments/assets/f34a9207-4621-4a3d-ba19-6b065c86e576" />

We can also run command to all the workers by using below command

```
ansible -i hosts servers -a "sudo apt update"
```

Here, we can pass single command at time which is not fesible, so we can create **PlayBooks**

Simply create file with task like install_docker.yml  # refer yml file
in which we can add multiple command






