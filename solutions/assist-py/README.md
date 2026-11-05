# Assistant
 
Персональный ассистент на FastAPI. Репозиторий ведётся в рамках дисциплины контейнеризация и оркестрация приложений.
 
Автор: Дарья Мануковская, ИСУ 466625
 
## Как запустить
 
```bash
docker build -t manuk-assistant:v1 .
docker run -d --name manuk-assistant -p 5455:5455 \
  -e APP_OWNER=manuk -e APP_SECRET=secret25manuk \
  manuk-assistant:v1
```
 
## Переменные окружения
 
| Переменная | Для чего | Пример |
| --- | --- | --- |
| APP_OWNER | фамилия, показывается на /me | manuk |
| APP_SECRET | ключ для /secret/ | secret25manuk |
| PORT | порт приложения | 5455 |
 
## Как проверить
 
```bash
curl http://localhost:5455/health
curl http://localhost:5455/me
```