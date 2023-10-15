# mts_less
Ansible:
За основу взят https://github.com/vitabaks/postgresql_cluster
Отредактирован inventory под наши хосты, прописываем ssh-ключи и проверяем доступность inventory
В vars/main включаем установку HAProxy - haproxy_load_balancing: true, и выключаем PG_Bouncer - pgbouncer_install: false 
После этих настроек деплоим.

Helm:
Namespace - sre-cource-student-38
name: sre-api-mts

В values.yaml в connection string задать ip: server=91.185.84.192  (для git-a убрал ip)
