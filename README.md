**Тестовое задание.**
_______________________________________________________________________
Подготовить docker-compose проект в котором должны быть развернуты контейнеры
   1. Jbpm
   2. Nginx
   3. Postgres
   4. Prometheus
   5. Grafana
   6. Node-exporter
Проверка правильности выполнения задания:
    Для выполненного задания все запросы поступают на 80 порт через Nginx контейнер (запросы проксируются в Jbpm и Grafana на разные endpoint-ы, считается выполненной если при запросах /jbpm /grafana выведет на разные сервисы). Остальные порты должны быть закрыты.
Jbpm настроен на работу с СУБД postgres
Grafana настроена на работу с Prometheus.
Внутри Grafana настроен dashboard для отображения метрик из Prometheus
Prometheus забирает метрики с host машины (node-exporter)
Приложить скриншот дашборда.

Для запуска проекта:
1. Установить [docer](https://docs.docker.com/engine/install/ubuntu/) и [docker-compose](https://docs.docker.com/compose/install/)
2. Склонировать репозиторий `git clone git@github.com:Shchegolkov-vg/test_it.git`
3. Запустить docker-compose файл `docker-compose up`
<<<<<<< HEAD
4. Доступ к grfafna -  http://localhost/grafana login/pasw: admin (dasboard и datasource уже добавлены)
5. Доступ к jbpm - http://localhost/jbpm login:pasw: wbadmin

![image](https://github.com/Shchegolkov-vg/test_it/assets/154276083/f96923f5-d48b-48b1-bd0b-9f46cf676715)

![image](https://github.com/Shchegolkov-vg/test_it/assets/154276083/baa11ba0-8d98-4079-8ea2-707d6d8190a3)

=======
4. Доступ к grfafna -  http://ip-address/grafana/ login/pasw: admin (dasboard и datasource уже добавлены)
5. Доступ к jbpm - http://ip-address/jbpm/ login:pasw: wbadmin
>>>>>>> caea495 (add & fixed files)
