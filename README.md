
_______________________________________________________________________
Задача (оформить в GIT-системе):
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
2. Склонировать репозиторий  
`git clone git@github.com:Shchegolkov-vg/test_it.git`
3. Запустить docker-compose файл `docker-compose up`
4. Доступ к grfafna -  http://localhost/grafana login/pasw: admin (dasboard и datasource уже добавлены)
5. Доступ к jbpm - http://localhost/jbpm login:pasw: wbadmin
