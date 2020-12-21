# ansible-ffnef
Ansible based server configuration based on https://github.com/FreiFunkMuenster/ansible-ffms

## how to clone
```bash
git clone git@github.com:Neanderfunk/ansible-ffnef.git
cd ansible-ffnef
git submodule update --init roles
```


## Beispiel-Aufruf:

```bash
ansible-playbook -i hosts nextcloud.yml -e 'ansible_python_interpreter=/usr/bin/python3' --tags="nextcloud_nginx_mariadb" --limit="cloud"
```

**nextcloud.yml** ist das Playbook, es kann auch monitoring.yml, gateways.yml usw. sein.

**--tags="nextcloud_nginx_mariadb"** Begrenzt das Playbook auf die roles, welche diese Tags nutzen.

**--limit="cloud"** Begrenzt die Ausführung des Playbooks auf den angegebenen Host.
