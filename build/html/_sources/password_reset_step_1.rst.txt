Сброс пароля. Шаг 1
===================

..  code-block:: none

    POST http://sjournal.milestns.beget.tech/api/v1/password/email

Пример запроса
--------------

..  code-block:: none

    {
        "email": "api9@example.com",
    }

Правила валидации
-----------------

..  code-block:: none

    'email' => 'required|email',

Примеры ответов
---------------

Успешная отправка
~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": {
            "message": "Код для сброса пароля был выслан на почту",
            "email": "ramis.streignard@gmail.com"
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
            "Поле E-Mail адрес обязательно для заполнения."
        ],
        "data": null
    }

Пользователь не найден
~~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": false,
        "errorMessage": [
            "Не удалось найти пользователя с указанным электронным адресом"
        ],
        "data": null
    }

API Throttling
~~~~~~~~~~~~~~

При большом количестве запросов с неверными данными, есть возможность получить кратковременный "бан". В данном случае будет отправлен следующий ответ

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": false,
        "errorMessage": [
            "Пожалуйста, подождите перед повторной попыткой"
        ],
        "data": null
    }

