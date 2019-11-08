# sprint15
## Backend deployment

Public IP: 84.201.138.101   http://sprint15app.ml https://sprint15app.ml

* все ошибки обрабатываются централизованно;
* тела запросов и, где необходимо, заголовки и параметры, валидируются по определённым схемам. Если запрос не соответствует схеме, обработка не передаётся контроллеру и клиент получает ошибку валидации;
* все запросы и ответы записываются в файл request.log;
* все ошибки записываются в файл error.log;
* файлы логов не добавляются в репозиторий;
* к серверу можно обратиться по публичному IP-адресу, указанному в README.md;
* к серверу можно обратиться по http и по https, используя домен, указанный в README.md;
* секретный ключ для создания и верификации JWT хранится на сервере в .env файле. Этот файл не добавляется в git;
* в режиме разработки (когда process.env.NODE_ENV !== 'production') код запускается и работает без наличия .env файла;
* сервер самостоятельно восстанавливается после GET-запроса на URL /crash-test.
