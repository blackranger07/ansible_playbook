# ansible_playbook
Ansible Practice Playbook

This repo is meant for myself while I learn how to use ansible.

* The "inventory" file is used to have all of your targets that you want ansible to be able to reach for your automations.

This command will look at all the hosts inside of "inventory" file and will login to server(s) using the specified key file. Then it will check to make sure ansible can connect to the remote server.
* ansible all --key-file ~/.ssh/ansible-key -i inventory -m ping

The shorthand command to the one above. Here, the "--key-file" and "inventory" file were not specified because the needed information was created in "ansible.cfg"
* ansible all -m ping

Lists the hosts inside of the "inventory" file.
* ansible all --list-hosts

This gathers all of the important data about the remote hosts.
* ansible all -m gather_facts
