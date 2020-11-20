## Шаблон запуска и описания сервиса

За основу взят run book template - перед мною не стояло цели точности перевода, скорее наоборот, это очень не точная адаптация английской версии под своих нужды и цели, переведенная "как пониманию" на русский язык.

### Описание сервиса и системы в целом

> Краткое описание сервиса и его основных фишек

(пример: Микросервис для отправки email сообщений)

### Бизнес значение сервиса

> Какие проблемы закрывает продукт? Какую ценность он несет с точки зрения бизнеса? Какие ожидания с точки зрения доступности и гарантий ждет бизнес от этого сервиса?

_(пример: Делаем возможность отправлять email сообщения легко и просто, избегаем попадения в папку spam и обеспечиваем около 100%-ую достовляемость)_

### Краткое техническое описание

> Какой тип сервиса? Монолит или микросервис? API или background tasks processing? Многофуонционален или выполняет одну задачу?

_(пример: Микросервис для отправки email сообщений, принимает сообщения через SQS и общается с внешними email-гейтами, формат сообщений определен через protobuf)_

### SLA

> Какую доступность и работоспобность должен гарантировать сервис?

_(пример: Сервис должен работать 100% времени, при неуспешной отправке сообщения оно должно быть отправлено еще раз)_

### Приложение/Демоны/Сервисы/Middleware's/Базы данных

> Из каких приложений, демонов, middlerware'ов состоит ваш сервис?

_(пример: ruby приложение + sidekiq демон + rabbitmiq демон + postgresql + elasticsearch + statsd демон)_

## Характеристики системы