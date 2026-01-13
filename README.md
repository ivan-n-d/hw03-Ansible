## Структура
- `playbook.yml` - основной плейбук
- `inventory.ini` - файл инвентаризации с хостами

## Группы хостов
- **app**: vm2, vm3 - установка Docker
- **database**: vm1 - установка PostgreSQL
- **web**: vm1

## Использование
```bash
# Проверка соединения
ansible all -i inventory.ini -m ping

# Запуск плейбука
ansible-playbook -i inventory.ini playbook.yml