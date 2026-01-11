Веб-приложение в докере

backend/Dockerfile,wserv.py

nginx/nginx.conf 

docker-compose.yml

README.md


запуск:
перейти в корень проекта, запустить:
docker compose up --build


проверить:
curl http://localhost

вывод должен показать: Hello from Effective Mobile!



схема работает:
клиент -> Nginx(80) -> Backend(8080, docker net)
клиент стучится на 80 порт, nginx принимет и перенаправляет запрос на бэк по сети докера, на что получает ответ "Hello from Effective Mobile!", который отправляется в обратном порядке.

Использовал:
Pythone 3(http.server) - backend
Nginx - reverse proxy
Docker, compose - контейнеры и управление многоконтенеровость.
