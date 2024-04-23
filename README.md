# distributed calculator 2.0
## Суть проекта:
Калькулятор, который способен считать математические выражения конкуренто.
Также можно посмотреть решение каждого введённого тобой выражения.
Для того, чтобы посчитать пример, нужно авторизоваться.
## Используемые технологии
* SQlite
* JWT
* proto
* grps
## Требования
Go >= 1.20 </br>
C++ (для SQlite)
## Запуск проекта
1)
Для начала необходимо скачать Zip файл или клонировать проект.
```shell
git clone https://github.com/tantoni228/distributed_calculator2
```
2) 
Скачиваем C++ (если его нет).
Устанавливаем необходимые пакеты. Пишем команду в каталоге проекта:
```shell
go mod download 
```
3) Необходимо запустить два сервера. 1 - *авторизации*, 2 - *калькулятор*
1. Запуск сервера калькулятора
```shell
go run cmd/client/client_authorization.go
```
2. 
```shell
go run cmd/client/client_calculator.go
```
## Функционал проекта
Необходимо зайти на [ссылку](http://127.0.0.1:5001/register) (http://127.0.0.1:5001/register). Придумать логин и пароль. Потом перейти на [ссылку](http://127.0.0.1:5001/login) (http://127.0.0.1:5001/login). Здесь вы получите JWT токен, при помощи которого можно будет решить пример. Токен работает 5 мин, потом необходимо генерировать новый. Копируем его и идём [сюда](http://127.0.0.1:8080/calculate) (http://127.0.0.1:8080/calculate). Здесь вводим пример с токеном и получаем id(запоминаем). Чтобы получить решение переходим [сюда](http://127.0.0.1:8080/get_solution) 
(http://127.0.0.1:8080/get_solution).
Вводим токен с id и получаем решение примера. Также отображаются ошибки, если имеются.

## Недоработки
* Ни в коем случаи не делим на ноль. Программа не обрабатывает эту ошибку. Программа не будет вычислять дальше.
* Реализован на одном порту, но при доработке сможет выполняться несколькими( попробую доделать).
* Любой пользователь может получить решение примера
* Калькулятор целочисленный


## Обратная связь
[почта](leshyovantoha@yandex.ru) </br>
[телеграм](https://t.me/sadlarfox)
