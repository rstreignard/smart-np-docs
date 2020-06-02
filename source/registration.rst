Регистрация
===========

..  code-block:: none

    POST http://sjournal.milestns.beget.tech/api/v1/register

Пример запроса
--------------

..  code-block:: none

    {
        "email": "api@test.com",
        "password": "password",
        "password_confirmation": "password",
        "device_name": "Iphone 11",
        "device_os": "iOS",
        "device_code": "72f316e6-a353-11ea-bb37-0242ac130002"
    }

Правила валидации
-----------------

..  code-block:: none

    'email' => 'required|string|email|max:191|unique:app_users', 
    'password' => 'required|string|min:8|confirmed', 
    'device_name' => 'required|string|max:191', 
    'device_os' => 'required|string|max:191|in:Android,iOS', 
    'device_code' => 'required|string|max:191'

Примеры ответов
---------------

Успешная регистрация
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
            "Такое значение поля E-Mail адрес уже существует.", 
            "Поле Пароль не совпадает с подтверждением." 
        ], 
        "data": null 
    }
    