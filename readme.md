# Инструкция по работе с Git

## Что такое Git

Git - одна из реализаций распределенных систем контроля версий, имеющая как локальную версионность так и версионность на сервере. 
Git является самом полурярной системой контроля версий на сегодняшний день

## Подготовка репозитория

Для того что бы создать репозиторий в указанной папке, используется команда *git init*. Для этого достаточно написать команду "git init" в папке с будующим репозиторием

## Создание фиксаций

### Просмотр информации о изменениях

Для того, что бы посмотреть информацию об изменениях, сделанных в текущей ветке, необходимо использовать команду "git status". Для этого достаточно использовать *git status* в папке с репозиторием 

### Добавление файла к коммиту
для того чтобы добавить файл к новому коммиту("сохранению") необходимо использовать команду "git add".
Используется она следующим образим:
в папке с репозиторием пишем команлу *git add <имя файла>*

### Создание коммитов

Для создания новой фиксации необходимо использовать команду *git commit*. 
Используется она следующим образом:
В папке с репозиторием пишется команда *git commit -m "<сообщение к коммиту>".
Все файлы коммита должны быть предварительно добавлены с помощью команды *git add*.
Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***

## Перемещение между сохранениями

Для того что бы перемещаться между коммитами необходимо использовать команду *git log*, что бы выбрать необходимый коммит, скопировать его имя, затем использовать команду в папке с репозиторием : *git checkout <имя коммита>*.

## Журнал изменений

Для того, что бы вызвать журнал изменений необходимо использовать команду *git log*.
Данная команда показывает все сохраненные изменения в файле.

## Ветки в Git

* Для того что бы посмотреть ветки, которые созданы на данный момент, необходимо ввести команду *git branch*.
* для того что бы создать новую ветку необходимо ввести команду *git branch <имя ветки>*.
* Для перемещения между ветками необходимо ввести команду *git checkout <имя ветки>*.

## Слияние веток и разрешение конфликтов

### Слияние веток:

Для того что бы слить ветки необходимо ввести команду *git merge <имя ветки>*.
**ВАЖНО** 
Для этого необходимо находится на ветке мастер, что бы изменения были внесены в основной файл.

### Решение конфликтов:

При возникновении конфликтов при слиянии веток необходимо выбрать на конфликте путь решения.
Для решения представлены 4 варианта:
1. Принять текущие изменения
2. Принять входящие изменения
3. Применить оба изменения
4. Сравнить изменения  

## Удаление веток

Для того что бы удалить ветку, для начала необходимо произвести слияние с веткой мастер.
Затем для удаления ненужной ветки необходимо ввести команду *git branch -d <имя ненужной ветки>*.
Если *git* не удаляет ненужную ветку необходимо ввести команлу *git branch -D <имя ненужной ветки>*.
