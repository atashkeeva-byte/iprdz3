## Команды для запуска:

Запустить приложение:

`docker compose up -d`

Проверить состояние:

`docker compose ps`

Остановка:

`docker compose down`

Приложение доступно по адресу: http://localhost:8080

## Настройки Docker Compose

В compose.yaml настроены два сервиса:

app — собирается из Dockerfile, использует настройки из .env и подключается к Redis

redis — запускается из образа redis:alpine, используется для хранения счётчика

Для приложения настроены переменные:

APP_PORT — порт внутри контейнера;

HOST_PORT — порт на компьютере;

GREETING — текст приветствия

Приложение подключается к Redis по адресу redis://redis:6379/0

Для Redis включено сохранение данных AOF. Данные хранятся в именованном томе redis-data, подключённом к /data

Для обоих сервисов настроены healthcheck. Приложение проверяет доступность HTTP-сервера через /healthz, Redis — командой redis-cli ping



## Report

## 4 балла — один контейнер

<img width="1039" height="197" alt="image" src="https://github.com/user-attachments/assets/2db3e4af-8ea9-43c1-861e-00d08745b8c6" />


## 6 баллов — Compose и данные

<img width="1050" height="210" alt="image" src="https://github.com/user-attachments/assets/b0ffa8ab-881b-4c69-a3ad-3c342522cfa1" />


## 8 баллов — отдельное хранилище

<img width="748" height="272" alt="image" src="https://github.com/user-attachments/assets/9e10d34e-732f-4469-b6f5-eb064d40e07e" />


<img width="650" height="315" alt="image" src="https://github.com/user-attachments/assets/ce3b4e3a-0f51-46ee-8d18-f586dd7e765c" />


<img width="701" height="107" alt="image" src="https://github.com/user-attachments/assets/8aeae6bc-0116-4ff1-9fd4-e1753b47c848" />
