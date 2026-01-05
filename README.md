# Go Backend Frequently Asked Interview Questions

[Вопросы Go](Go.md)

[Что вывелет программа?](GoOutput.md)

[Вопросы Сети](Network.md)

## HTTP

* В чем отличия между версиями протокола `0.9` `1.0` `1.1` `2.0` `3.0`?

* Составные части запроса и ответа.

* Коды ответов `1xx` `2xx` `3xx` `4xx` `5xx`.

* Приведите примеры общих, клиентских и серверных заголовков.

* За что отвечают заголовки `Accept` `Accept-Charset` `Accept-Encoding` `Accept-Language` `Cache-Control` `Connection` `Content-Disposition` `Content-Encoding` `Content-Language` `Content-Length` `Content-Location` `Content-Type` `Cookie` `Date` `Host` `Location` `Referer` `Set-Cookie` `Transfer-Encoding` `User-Agent` ?

* Как работает `Basic Auth`?

* Кеширование ответов.

* Идемпотентность ответов.

* Коды ответов методов `POST` и `PUT`.

* Свойства `RESTful` приложений: единство интерфейса, независимость клиента от сервера, сохранность состояния, кэширование ответов сервера, многоуровневая архитектура, необязательный код в ответе сервера.

* Сравнение `REST` и `gRPC`: сетевые протоколы, форматы сообщений, кодогенерация, двунаправленность коммуникаций, скорость разработки.

## DNS

* Какой алгоритм вычесления адреса? Как используется файл `/etc/hosts`?

* Как настраивает локальный сервер? Как настраивается `resolv.conf`?

* Чем отличается рекурсивный сервер от нерекурсивного? Когда предпочтительнее использовать каждый?

* Формат и типы записей: `SOA` `A` `AAAA` `CNAME` `MX` `TXT` `NS` `PTR` `SRV` `SPF`.

* Уметь пользоваться утилитами `dig` и `nslookup`.

[Вопросы Git](Git.md)

[Вопросы Linux](Linux.md)

[Вопросы PostgreSQL](PostgreSQL.md)

[Вопросы Kafka](Kafka.md)

## Общее

* Методологии разработки: `Waterfall` `Cascade` `Iterative` `Agile` `Scrum` `Kanban`.

* Обработки ошибок и отказов: `Circuit Breaker` `Retry` `Timeout` `Fallback` `Bulkhead`.

* Распределение нагрузки: `Round Robin` `Least Connections` `Weighted Round Robin` `Weighted Least Connections` `IP Hash` `Sticky Sessions` `Random` `Least Response Time` `Chaos Monkey`.
