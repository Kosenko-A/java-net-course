# Домашняя работа

---

### Задание:

1. Подписаться на репозиторий https://github.com/azarnovdaniil/java-net-course
2. Поставить звездочку 
3. Сделать fork репозитория
4. Прислать pull-request в репозиторий курса с заполненным блоком ответы.
5. Прислать ссылку на pull-request через платформу.

---

### Вопросы:

1. Как организовать клиент-серверное взаимодействие?
2. Как и в каком виде передавать файлы?
3. Как пересылать большие файлы?
4. Как пересылать служебные команды?
5. Как передавать структуру каталогов/файлов?
6. Какую библиотеку использовать для сетевого взаимодействия: java.io, java.nio, Netty?

---

### Ответы:

1. Взаимодействие между сервером и клиентом происходит через Socket. 
Каналы ввода и вывод класса Socket как раз будут обеспечивать связь эту связь. 
Объявляется этот класс на стороне клиента, а сервер воссоздаёт его, получая сигнал на подключение. 
На стороне сервера будет находиться ServerSocket, он нужен только на этапе установки соединения. 
После создания объекта типа ServerSocket, метод accept() ждет пока к серверу кто-то подсоединиться и после 
этого возвращает объект типа Socket, то есть воссозданный клиентский Socket. Также необходимо знать адрес 
сервера и порт клиента. Методы getInputStream и getOutputStream дают доступ к потокам объектов типа Socket. 
2. Файлы передаются в виде потока байтов
3. Установить максимальный объем файла в байтах для прохождения целиком. Если файл превышает этот объем, то поделить его на части, а потом склеить.
4. Можно на стороне сервера сделать так, что при приходе определенных команд будут вызываться соответствующие методы
5. С помощью Path
6. java.io

---

### Материалы:

1. [Howe make a fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo)
2. [How make a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)
