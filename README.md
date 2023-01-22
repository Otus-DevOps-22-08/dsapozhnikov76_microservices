# dsapozhnikov76_microservices
dsapozhnikov76 microservices repository

## Monitoring-1
Выполнены все пунктиы основного задания. 
 
Ссылки на образы: https://hub.docker.com/u/dsapozhnikov76
## GitLab-ci-1

1. создана ВМ через cli yandex
2. настроен GitLab(получен пароль root; закрыта регистрация)
3. добавлен Reddit в проект 
4. поставлен раннер 
5. добавлена зависимость от тегов для production и stage 
6. добавлены динамические окружения


## Docker-4

1. Скачал оригинальный docker-compose.yml, запустил билд контейнеров
2. Изменил docker-compose.yml под использования 2-х сетей
3. Создал .env записав туда параметризованные параметры
4. При запуске docker-compose использует имя каталога как базовое имя проекта,
с помощью флага -p можно его изменить, например:

    ``docker-compose -p docker4 up -d``

## Docker-3

1. Скопировал исходники Dockerfile в целевые файлы
2. Добавил обновление pip для корректной установки зависимых пакетов (MarkupSafe)
3. Создали сеть, запустили контейнеры, проверили что можно сделать пост.
4. Переопределила сетевые алиасы, запустила контейнеры с передачей переменных окружения (--env)
5. Оптимизировала образы сервиса ui с использованием в качестве базового образа - ubuntu:16 и alpine 

````
REPOSITORY               TAG            IMAGE ID       CREATED          SIZE
dsapozhnikov76/ui        2.0            95d20a31993e   19 minutes ago   464MB
dsapozhnikov76/ui        1.0            6d8d0fc481df   7 hours ago      771MB

````
6. Создал том, подключил том к контейнеру с монгой, проверка работы приложения в целом (с остановкой контейнера с базой)

## Docker-2


  1.  Создан инстанс на YC
  2.  Инициирован докер хост система на инстансе
  3.  Создана структура репозитория Docker
  4.  Создан образ приложения reddit-monolith
  5.  Запущен контейнер с приложением на инстансе
  6.  Запшуен образ приложения в docker hub

## Docker-1 

Создал контейнер 

Сделал из него образ

Записал лог в docker-1.log

````
derek@dell5547 ~/otus/dsapozhnikov76_microservices $ docker system df
TYPE                TOTAL               ACTIVE              SIZE                RECLAIMABLE`
Images              3                   2                   63.16MB             63.15MB (99%)
Containers          2                   1                   18B                 0B (0%)
Local Volumes       6                   0                   268.9MB             268.9MB (100%)
Build Cache         0                   0                   0B                  0B`
````
