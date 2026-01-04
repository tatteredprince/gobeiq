# Go Backend Frequently Asked Interview Questions

[Вопросы Go](Go.md)

## Что выведет программа?

<details>

<summary>
Что выведется если `a1` проинициализировать слайсом нулевого размера?
</summary>

```go
a1 := make([]int, 0, 10)
a1 = append(a1, []int{1, 2, 3, 4, 5}...)
a2 = append(a1, 6)
a3 = append(a1, 7)
fmt.Println(a1, a2, a3)
```

</details>

<details>

<summary>Почему модификация второго слайса не изменяет содержимое первого?</summary>

```go
func main() {
	first := []int{10, 20, 30, 40, 50}
	second := make([]*int, len(first))
	for i, v := range first {
		second[i] = &v
		*second[i] *= 10
	}
	fmt.Println(first)
	fmt.Println(*second[0], *second[1], *second[2], *second[3], *second[4])
}
```

</details>

<details>

<summary>Как в `handle()` вернуть ошибку не используя дополнительных пакетов? Возможно используя интерфейс `error`?</summary>
  
```go
func main() {
  println(handle())
}

func handle() error {
  ...
}
```

</details>

## Сети

* Отличия между `TCP` и `UDP`: гарантия доставки, нумерация пакетов, поддержка дуплексного режима, предустановка соединения, скорость передачи данных, восстановление данных.

* Чем отличаются адреса `MAC` и `IP`?

* Как используется маска подсети? Сколько адресов в сети с масков `/24`? А сколько с маской `/32`?

* Опишите процесс `TLS handshake`, как он поменялся в `TLS 1.3`?

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

## Git

* Чем отличается ветка от тега?

* Какие типы и стратегии слияний знаете?

* Отличия `rebase` от `merge`.

* Какие состояния локального репозитория существуют?

## Linux

* Что означают поля `VSZ`, `RSS` и `SHM` в выводе `top`/`ps`?

* Почему в выводе `top` один или несколько процессов могут занимать более 100% нагрузки процессора?

* Как операционная система переключается между процессами? Что такое аппаратные и программные прерывания?

* Может ли на компьютере с одним логическим процессором выполнятся одновременно много процессов?

* В чем отличия процесса от потоков исполнения?

* Как формируются и именовыываются сетевые интерфейсы? Что за интерфейс `loopback`?

* Для чего нужен `Predictable network interface naming convention`?

[Вопросы PostgeSQL](PostgreSQL.md)

[Вопросы Kafka](Kafka.md)

## Общее

* Методологии разработки: `Waterfall` `Cascade` `Iterative` `Agile` `Scrum` `Kanban`.

* Обработки ошибок и отказов: `Circuit Breaker` `Retry` `Timeout` `Fallback` `Bulkhead`.

* Распределение нагрузки: `Round Robin` `Least Connections` `Weighted Round Robin` `Weighted Least Connections` `IP Hash` `Sticky Sessions` `Random` `Least Response Time` `Chaos Monkey`.
