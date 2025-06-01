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

## Linux

* Что означают поля VSZ, RSS и SHM в выводе top/ps?

## Общее

* Методологии разработки: `Waterfall` `Cascade` `Iterative` `Agile` `Scrum` `Kanban`.

* Обработки ошибок и отказов: `Circuit Breaker` `Retry` `Timeout` `Fallback` `Bulkhead`.

* Распределение нагрузки: `Round Robin` `Least Connections` `Weighted Round Robin` `Weighted Least Connections` `IP Hash` `Sticky Sessions` `Random` `Least Response Time` `Chaos Monkey`.
