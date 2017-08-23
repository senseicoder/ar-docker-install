# Usage

Lancement avec proxy : 
> ansible-playbook -i ~/bin/list_new_servers.txt -e 'setproxy=1' --limit "restore1.admin2" --ask-become-pass main.yml

Lancement sans proxy
> ansible-playbook -i ~/bin/list_new_servers.txt --limit "restore1.admin2" --ask-become-pass main.yml

# Todo

* erreur si joué sans proxy :  [WARNING]: could not parse environment value, skipping: [u'proxy_environment']
*  [WARNING]: when statements should not include jinja2 templating delimiters such as {{ }} or {% %}. Found: {{ setproxy }}