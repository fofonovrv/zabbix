# Zabbix
Файл docker-compose.yml разворачивает сервисы:
- zabbix-db (image mysql:5.7)
- zabbix-java-gateway (image zabbix-java-gateway)
- zabbix-web (image zabbix/zabbix-web-nginx-mysql:latest)
- grafana-zabbix (image grafana/grafana)
- zabbix-agent (image zabbix/zabbix-agent2:alpine-5.0.1)

# Порты
Для корректной работы необходимо открыть порты на фаерволе:
- 80 (веб-интерфейс)
- 10051 (подключение агентов к серверу)
- 10052 (мониторинг java приложений)
- 3000 (grafana)
- 10050 (доступ к агенту)

# Требования
Тестировалось на Ubuntu 20.04 и CentOS 7 (adm64). 
На сервере с 1Гб ОЗУ не хватает памяти для запуска даже пустой конфигурации...
