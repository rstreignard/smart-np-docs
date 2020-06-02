.. _login-label:

Login
=====

..  code-block:: none

    POST http://sjournal.milestns.beget.tech/api/v1/login

Пример запроса
--------------

..  code-block:: none

    {
        "email": "api9@example.com",
        "password": "password",
        "device_name": "Iphone 11",
        "device_os": "iOS",
        "device_code": "72f316e6-b353-11ea-cc37-0242ac130002"
    }

Правила валидации
-----------------

..  code-block:: none

    'email' => 'required|string|email|max:191',
    'password' => 'required|string|min:8',
    'device_name' => 'required|string|max:191',
    'device_os' => 'required|string|max:191|in:Android,iOS',
    'device_code' => 'required|string|max:191',

Примеры ответов
---------------

Успешная авторизация
~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    { 
        "status": true, 
        "errorMessage": null, 
        "data": { 
            "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9sb2NhbGhvc3RcL3Nqb3VybmFsXC9wdWJsaWNcL2FwaVwvdjFcL3JlZ2lzdGVyIiwiaWF0IjoxNTkxMDA4NTAxLCJleHAiOjE1OTEwMTIxMDEsIm5iZiI6MTU5MTAwODUwMSwianRpIjoiV3llMnFJU2dNb004WUV5MCIsInN1YiI6MzEsInBydiI6ImIzYzUwMmZlOGU1OThmYmIyNDUxNDNkM2RmYzQwMmY3NTEyZTdjYmUifQ.WU1qaLk42rsB7tQfven_xoysVZrHB_GJkQRkzf6dVK8", 
            "token_type": "bearer",
            "expires_in": 3600 
        } 
    }

Ошибки валидации
~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    { 
        "status": false, 
        "errorMessage": [ 
            "Поле E-Mail адрес должно быть действительным электронным адресом.", 
            "Поле Пароль обязательно для заполнения." 
        ], 
        "data": null 
    }

Неверный логин/пароль
~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    { 
        "status": false, 
        "errorMessage": [ 
            "Неверный логин или пароль.", 
        ], 
        "data": null 
    }

Вход с другого устройства
~~~~~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    { 
        "status": false, 
        "errorMessage": [ 
            "Для доступа к контенту, авторизуйтесь на устройстве с которого проходили регистрацию или обратитесь в Поддержку.", 
        ], 
        "data": null 
    }
    

