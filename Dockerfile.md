# Dockerfile Cheat Sheet

## Основы
- `FROM` - задает базовый (родительский) образ.
- `RUN` - выполняет команду и создает новый слой образа.
- `CMD` - задает команду, которая будет выполнена при запуске контейнера.
- `LABEL` - добавляет метаданные к образу в виде ключ-значение.
- `EXPOSE` - указывает на необходимость открыть порт.
- `ENV` - устанавливает переменные среды.
- `ADD` - копирует новые файлы, директории или удаленные URL-файлы и добавляет их в файловую систему контейнера.
- `COPY` - копирует новые файлы или директории в файловую систему контейнера.
- `ENTRYPOINT` - задает исполняемый файл, который будет запущен при старте контейнера.
- `VOLUME` - создает точку монтирования для работы с постоянным хранилищем.
- `USER` - устанавливает имя пользователя (UID) или UID/GID, который будет использоваться.
- `WORKDIR` - задает рабочую директорию для инструкций `RUN`, `CMD`, `ENTRYPOINT`, `COPY` и `ADD`.
- `ARG` - задает переменные, которые могут быть переданы во время сборки образа.
- `ONBUILD` - добавляет инструкцию, которая будет выполнена позже, при использовании образа в качестве базы для другого образа.

## Пример Dockerfile

```dockerfile
# Использование официального образа Python 3.8 как базового
FROM python:3.8-slim

# Установка рабочей директории в контейнере
WORKDIR /app

# Копирование файлов из текущей директории в рабочую директорию контейнера
COPY . /app

# Установка зависимостей из файла requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Определение переменной среды
ENV NAME World

# Открытие порта 80 для доступа к приложению
EXPOSE 80

# Запуск приложения при старте контейнера
CMD ["python", "app.py"]
