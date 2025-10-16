# Роль: danted-socks5

Эта роль устанавливает и настраивает Dante SOCKS5 сервер с авторизацией по PAM (локальные пользователи).

## Использование

1. Положи роль в папку `roles/danted-socks5/`.
2. Создай файл `users.yml` рядом с плейбуком.
3. Создай playbook:

```yaml
- hosts: vpnservers
  become: true
  vars:
    danted_external_ip: 103.74.92.94
    users_file: users.yml
  roles:
    - danted-socks5
