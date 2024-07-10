Graylog в docker-compose
Для запуска выполнить docker-compose up -d

Для отображения в веб-интерфейсе всех страниц логов, необходимо выполнить curl -XPUT -H 'Content-Type: application/json' -d '{"index": {"max_result_window": 500000 }}' 'http://127.0.0.1:9200/graylog_0/_settings'
Это увеличит число отображаемых записей до 500 000 для лога graylog_0

При необходимости выполнить команду для других логов, например для graylog_1
curl -XPUT -H 'Content-Type: application/json' -d '{"index": {"max_result_window": 500000 }}' 'http://127.0.0.1:9200/graylog_1/_settings'
