Lancement::

	ansible-playbook -i ~/bin/list_new_servers.txt --limit "restore1.admin2" --ask-become-pass main.yml

	éventuellement en ajoutant -e 'setproxy=1'
