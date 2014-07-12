Install my dotfiles and common utilities on the different machines I work on.

Uses Ansible to make it all easy.

To run it do something like `ansible-playbook dev.yml -i ~/.ansible_hosts -Kv`

The `-K` is necessary for localhost. Otherwise don't use that flag.

A sample .ansible_hosts file might look like this:

````
localhost              ansible_connection=local

[vps]
104.131.132.128   ansible_ssh_user=root
````

## Macs
Install Homebrew manually and then run `brew install ansible` to get
Ansible working. Then clone this repo, create a ~/.ansible_hosts file, and run the above command.
