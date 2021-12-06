# ansible-demo
basic layout to start testing

## ad-hoc commands examples
ansible all -i inventory/all -m ping -k -e ansible_port=12345 -e ansible_ssh_user=ansible

## playbook example

Run docker build for apache2 image:

ansible-playbook tasks/docker-build-apache2.yml

Use ansible ad-hoc commands after setting up ssh:
ansible all -i inventory/all -m ping -k -e ansible_port=12345 -e ansible_ssh_user=root
