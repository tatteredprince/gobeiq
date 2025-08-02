# Go Backend Interview Questions

## Go

* Знать "на зубок" модули
[`bufio`](https://pkg.go.dev/bufio)
[`builtin`](https://pkg.go.dev/builtin)
[`cmp`](https://pkg.go.dev/cmp)
[`context`](https://pkg.go.dev/context)
[`errors`](https://pkg.go.dev/errors)
[`fmt`](https://pkg.go.dev/fmt)
[`io`](https://pkg.go.dev/io)
[`maps`](https://pkg.go.dev/maps)
[`math/rand`](https://pkg.go.dev/math/rand)
[`math`](https://pkg.go.dev/math)
[`net/http`](https://pkg.go.dev/net/http)
[`net/url`](https://pkg.go.dev/net/url)
[`net`](https://pkg.go.dev/net)
[`os`](https://pkg.go.dev/os)
[`reflect`](https://pkg.go.dev/reflect)
[`regexp`](https://pkg.go.dev/regexp)
[`runtime`](https://pkg.go.dev/runtime)
[`slices`](https://pkg.go.dev/slices)
[`strconv`](https://pkg.go.dev/strconv)
[`strings`](https://pkg.go.dev/strings)
[`sync/errgroup`](https://pkg.go.dev/golang.org/x/sync/errgroup)
[`sync`](https://pkg.go.dev/sync)
[`time`](https://pkg.go.dev/time)
[`unsafe`](https://pkg.go.dev/unsafe)

* Паттерны Fan-In и Fan-Out, уметь реализовать их в коде.

* Преимущества и недостатки SQL и ORM. Какие ORM библиотеки в Go знаешь?

* Как устроено управление памятью в Go? Каков размер стека функций и как он растет?

* Какой memory footprint у горутин?

* Как в Go реализована поддержка замыканий?
  
* Как Go использует heap?

* Зачем в Go заключают куски кода в фигурные скобки?

* За счет чего атомики такие быстрые?

* Как использование интерфейсов в Go влияет на coupling и code reuse?

* Использование интерфейсов реализует контрактное программирование?

* Почему `context.Context` принято передавать первым аргументов в функции?

* Почему `context.Context` не рекомендуется встраивать в структуры? Каков срок жизни `context.Context`?

* Почему не рекомендуется передавать `nil` для неизвестного контекста? Для чего используют `context.TODO()`?

* Почему для `context.WithCancel()`, `context.WithTimeout()` и `context.Deadline()` лучше использовать `defer cancel()`?

* Почему не рекомендуется использовать `context.WithValue()` для передачи больших объектов?

* Почему вместо `context.Background()` в обработчиках запросов рекомендуется использовать родительский контекст?

* Как необходимо обрабатывать `ctx.Done()` в `select`?

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

* Отличия между TCP и UDP: гарантия доставки, нумерация пакетов, поддержка дуплексного режима, предустановка соединения, скорость передачи данных, восстановление данных.

* Опишите процесс TLS handshake, как он поменялся в TLS 1.3?

## HTTP

* Составные части HTTP запроса и ответа.

* Коды ответов: 1xx, 2xx, 3xx, 4xx и 5xx.

* Приведите примеры общих, клиентских и серверных заголовков.

* За что отвечают заголовки `Accept` `Accept-Charset` `Accept-Encoding` `Accept-Language` `Cache-Control` `Connection` `Content-Disposition` `Content-Encoding` `Content-Language` `Content-Length` `Content-Location` `Content-Type` `Cookie` `Date` `Host` `Location` `Referer` `Set-Cookie` `Transfer-Encoding` `User-Agent` ?

* Как работает HTTP Basic Auth?

* Кеширование ответов.

* Идемпотентность ответов.

* Коды ответов методов POST и PUT.

* Свойства RESTful приложений: единство интерфейса, независимость клиента от сервера, сохранность состояния, кэширование ответов сервера, многоуровневая архитектура, необязательный код в ответе сервера.

* Сравнение REST и gRPC: сетевые протоколы, форматы сообщений, кодогенерация, двунаправленность коммуникаций, скорость разработки.

## Git

* Чем отличается ветка от тега?

* Какие типы и стратегии слияний знаете?

* Отличия `rebase` от `merge`.

* Какие состояния локального репозитория существуют?

## Linux

* Что означают поля `VSZ`, `RSS` и `SHM` в выводе `top`/`ps`?

## Общее

* Методологии разработки: `Waterfall` `Cascade` `Iterative` `Agile` `Scrum` `Kanban`.

* Обработки ошибок и отказов: `Circuit Breaker` `Retry` `Timeout` `Fallback` `Bulkhead`.

* Распределение нагрузки: `Round Robin` `Least Connections` `Weighted Round Robin` `Weighted Least Connections` `IP Hash` `Sticky Sessions` `Random` `Least Response Time` `Chaos Monkey`.
