# ansible-gentoo

I'm using [Ansible's Gentoo modules](https://docs.ansible.com/ansible/latest/collections/community/general/portage_module.html) to deploy some of my Gentoo servers.


## software

The `software.yml` file contains a list of default packages, to add more just use `--extra-vars`.

**Example**:

    ansible-playbook software.yml --extra-vars "packages=['app-containers/docker', 'app-misc/neofetch']"


## emerge

To update the [@world](https://wiki.gentoo.org/wiki/World_set_%28Portage%29) set just run `emerge.yml`. It has some defaults but you can overwrite them via `--extra-vars`.

**Example**:

    ansible-playbook update_world.yml --extra-vars "sync=no deep=no"

