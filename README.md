# ansible_skeleton
basic layout to start testing

## ad-hoc commands examples
ansible {server/group} -a "hostname" -i hosts
ansible {server/group} -a "df -h" -i hosts
ansible {server/group} -a "date" -i hosts

ansible {server/group} -s -m yum -a "name=ntp state=installed" -i hosts

The -s option (alias for --sudo) tells Ansible to run the command with sudo. This will work fine with our Vagrant VMs, but if youâ€™re running commands against a server where your user account requires a sudo password, you should also pass in -K (alias for --ask-sudo-pass), so you can enter your sudo password when Ansible needs it.
