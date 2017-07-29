# Сервер SMPP

## Конфигурация

Конфигурация представлена в файле `config.py`.
Каждое поле сопровождено комментарием.

## Тесты

Файлы `test.py`, `smpp/parse_tests.py`, `smpp/functests.py` и папка `smpp/vendor`
для запуска не обязательны. Они содержат тесты проекта и зависимости тестов.

## Запуск

### Через Docker (предпочтительно)

1. Собрать образ с помощью команды `docker build -t smppserver`.
2. Запустить контейнер командой
  `docker run -p 2775:2775 --restart always --name smppserver smppserver`.
3. Остановить командой `docker stop smppserver`.

### Вручную

1. Требует Python версии 3.5 или выше.
2. Требуется установить в систему библиотеку zeromq. На ubuntu она ставится
  пакетом `libzmq-dev`.
3. Установить зависимости приложения: `pip install -r requirements.txt`.
4. Запустить файл `main.py`.
5. Остановить послав сигнал завершения через Ctrl+C.