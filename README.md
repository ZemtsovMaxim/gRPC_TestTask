# gRPC_TestTask

Этот проект представляет собой gRPC сервис обертку над nmap с использованием скрипта для сканирования уязвимостей сети.

## Установка

Для установки проекта на вашем компьютере выполните следующие шаги:

1. Клонируйте репозиторий на локальную машину:

    ```git clone https://github.com/ZemtsovMaxim/gRPC_TestTask.git```

2. Перейдите в каталог проекта:

    ```cd gRPC_TestTask```

3. Установите зависимости:

    ```go mod tidy```

4. Установите nmap (если еще не установлен):

    Linux:

    ```sudo apt-get update && sudo apt-get install -y nmap```

    Windows:

    Скачайте и установите с [официального сайта] (https://nmap.org)

    MacOS:

    ```brew install nmap```

## Использование

Для запуска сервера выполните следующие шаги:

1. Отредактируйте конфигурационный файл config.yaml в каталоге config в соответствии с вашими требованиями.

2. Запустите сервер:

    ```go run cmd/main.go --config=./config/config.yaml```

3. После запуска сервера он будет готов к принятию запросов gRPC.

4. Для проверки результата можно использовать Postman 

## Описание Makefile

### Тестирование

    ```make test```

### Запуск линтера

    ```make lint```

### Генерация кода из proto файла

    ```make generate```
