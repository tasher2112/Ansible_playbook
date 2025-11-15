# Ansible_playbook
___
## Цель и характеристики плейбука
Стандартизация, автоматизация и обеспечение согласованности в выполнении задач, например, автоматизация развёртывания приложений, управления обновлениями и конфигурирования кластеров. Ключевые характеристики плейбука включают: он должен быть пошаговым руководством, содержать конкретные действия (задачи) и наборы правил для их выполнения
___
## Блок кода
{lineno-start=1 emphasize-lines="10,14"}
```yaml
server: port: 8080
liquibase: base: &base user: <admin>
    password: <admin_password>
  test:
    <<: *base
    default-schema: ds
    url: ${database.test.url}
  access-control:
    <<: *base
    default-schema: test_access_control
    url: ${database.access-control.url}
```
