# Ansible Role: User Management

## Требования
- Ubuntu 22.04 Server
- Ansible 2.14+


## Установка зависимостей
```shell
sudo apt update && sudo apt install -y ansible-core
```

## Как запустить

Перед запуском лучше явно определить путь до ansible.cfg файла, из папки с проектом вызовите:
```shell
export ANSIBLE_CONFIG=$(pwd)/ansible.cfg
```

```shell
ansible-playbook -i inventory/hosts.yml playbooks/site.yml --ask-vault-pass
```


## Теги для запуска отдельных фич
```shell
ansible-playbook -i inventory/hosts.yml playbooks/site.yml --tags "create_users"
```

## Запуск для отдельной группы хостов
```shell
ansible-playbook -i inventory/hosts.yml playbooks/site.yml --tags "create_groups" --limit dev_servers
```
