# Ansible Role: User Management

## Требования
- Ubuntu 22.04 Server
- Ansible 2.14+

## Установка зависимостей
```bash
sudo apt update && sudo apt install -y ansible-core
```

## Как запустить
```bash
ansible-playbook -i inventory/hosts.yml playbooks/site.yml --ask-vault-pass
```

## Тестирование
```bash
ansible-playbook tests/test_users.yml --check
```

## Теги для запуска отдельных фич
```bash
ansible-playbook -i inventory/hosts.yml playbooks/site.yml --tags "create_users"
```

## Vault ключ
```bash
ansible-vault view secret.yml --vault-password-file .vault_pass.txt
```
