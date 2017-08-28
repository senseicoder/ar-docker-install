# Usage

Lancement avec proxy : 
> ansible-playbook -i ~/bin/list_new_servers.txt -e 'setproxy=1' --limit "restore1.admin2" --ask-become-pass main.yml

Lancement sans proxy
> ansible-playbook -i ~/bin/list_new_servers.txt --limit "restore1.admin2" --ask-become-pass main.yml

# Todo

* erreur si joué sans proxy :  [WARNING]: could not parse environment value, skipping: [u'proxy_environment']
*  [WARNING]: when statements should not include jinja2 templating delimiters such as {{ }} or {% %}. Found: {{ setproxy }}
* fatal: [test_infra_plays_cedric]: FAILED! => {"changed": true, "cmd": "mount -o remount /space", "delta": "0:00:00.038863", "end": "2017-08-23 13:46:31.228903", "failed": true, "rc": 32, "start": "2017-08-23 13:46:31.190040", "stderr": "mount: cannot remount /space read-write, is write-protected", "stderr_lines": ["mount: cannot remount /space read-write, is write-protected"], "stdout": "", "stdout_lines": []}