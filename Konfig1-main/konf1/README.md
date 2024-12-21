# Конфигурационное управление

## Домашнее задание №1

**Вариант №10**

Разработать эмулятор для языка оболочки ОС. Необходимо сделать работу
эмулятора как можно более похожей на сеанс shell в UNIX-подобной ОС.
Эмулятор должен запускаться из реальной командной строки, а файл с
виртуальной файловой системой не нужно распаковывать у пользователя.
Эмулятор принимает образ виртуальной файловой системы в виде файла формата
zip. Эмулятор должен работать в режиме CLI.

Конфигурационный файл имеет формат xml и содержит:
1. Имя пользователя для показа в приглашении к вводу.
2. Имя компьютера для показа в приглашении к вводу.
3. Путь к архиву виртуальной файловой системы.
4. Путь к лог-файлу.


Необходимо поддержать в эмуляторе команды ls, cd и exit, а также следующие команды:
1. cp
2. chmod
3. whoami

Все функции эмулятора должны быть покрыты тестами.

## Описание всех функций и настроек

* ls - Команда вывода содержимого данного каталога;
* cd - Команда перехода к определённому каталогу;
* chmod - команда для изменения прав доступа к файлам и каталогам;
* exit - Команда для завершения процесса командной оболочки с кодом успешного завершения или кодом ошибки;
* whoami - выводит имя пользователя, ассоциированное с текущим эффективным идентификатором пользователя;
* cp -  копирует файл или каталог, указанный в параметре;

## Команда для запуска проекта

Для запуска программы необходимо перейти из корневого каталога проекта в каталог ``Konf1`` посредством команды:

```
cd Konf1
```

После перехода в каталог ``Konf1`` запускаем программу:

```
python emulator.py
```

## Команда для запуска юнит-тестов

Для запуска юнит-тестов необходимо перейти из корневого каталога проекта в каталог ``Konf1`` посредством команды:

```
cd Konf1
```

Для запуска пишем команду:

```
python -m unittest tests.py
```

## Описание работы программы

Программа запускается в каталоге ``Konf1``. Первоначально создана эмуляция образа Linux в VirtualDevice.zip архиве. Программа работает только с командами, указанными в условии задачи и разделе **``Описание всех функций и настроек``**. Результат работы команд выводится в консоль образа Linux. 

## Результат работы юнит-тестов

![image](https://github.com/user-attachments/assets/2fa6589d-a785-4f7c-9b1c-fb1dea70963e)


## Результат работы программы

![image](https://github.com/user-attachments/assets/4371fc40-7502-44e0-af9a-e15689e3ec4e)