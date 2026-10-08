# 2prac_3sem — Сетевой сервер БД на C++ (многопоточный)

Практическая №2, 3 семестр. Многопоточный TCP-сервер мини-СУБД на сокетах: парсинг команд, хеш-таблицы, файловое хранение.

## Что внутри
- `main.cpp` — многопоточный сервер (`std::thread`, `mutex`, POSIX sockets)
- `CommandParser.cpp/.h` — парсер `SELECT (...) FROM ...`
- `FileHandler.cpp/.h` — файловое хранение (~21К строк кода обработки)
- `HashTable.cpp/.h`, `Table.cpp/.h`, `CustVector.h`
- `schema.json`, `com.txt`, `CommandHelp.txt`, `nlohmann/`

## Стек
C++17, POSIX sockets, multithreading, CMake/build

## Запуск
```bash
g++ main.cpp FileHandler.cpp HashTable.cpp Table.cpp CommandParser.cpp -o db_server -pthread
./db_server
```

## Что изучено
Сокеты, потоки и мьютексы, собственные структуры данных, протокол клиент-сервер.
См. также `1prac_3sem` — однопоточная версия.

---
**Автор:** Assweg · Telegram: [@assweg](https://t.me/assweg) · Учебное портфолио, все работы — студенческие.
