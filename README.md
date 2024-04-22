# distributed calculator 2.0
##Суть проекта:
Калькулятор, который способен считать математические выражения конкуренто.
Также можно посмотреть решение каждого введённого тобой выражения.
Для того, чтобы посчитать пример, нужно авторизоваться.
##Используемые технологии
* SQlite
* JWT
* proto
* grps
## Требования
Go 1.20 >=
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
От

