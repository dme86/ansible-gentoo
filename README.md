# gentoo-ansible

I'm using [Ansible's Gentoo modules](https://docs.ansible.com/ansible/latest/collections/community/general/portage_module.html) to deploy some of my machines.


## software

The `software.yml` file contains a list of default packages, to add more just use `--extra-vars`.


**Example**:

    ansible-playbook software.yml --extra-vars "packages=['app-containers/docker', 'app-misc/neofetch']"

