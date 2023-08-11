Развертывание окружения ansible:

python3.9 -m venv venv && source venv/bin/activate
pip3.9 install ansible==6.3.0


Непосредственно раскатка роли:

ansible-playbook -D all.yml -i inventory.yml

Реализовал таск через docker-compose с nginx, wordpress, grafana, prometheus. Сервисы проксируются через nginx по разным доменам. Айпишник хоста захардкожен в инвентаре, в качестве хост-ОС применялся Debian 12 с установленным sudo (настроенным в режиме NOPASSWD соответственно) и залитым ssh-ключом.
