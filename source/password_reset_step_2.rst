Сброс пароля. Шаг 2
===================

..  code-block:: none

    POST http://sjournal.milestns.beget.tech/api/v1/password/reset

Пример запроса
--------------

..  code-block:: none

    {
        "email": "ramis.streignard@gmail.com",
        "token": "52910e26f07f08bdeb4c5f46540beee3ed558f543043a1a359126e8608d1ef9e",
        "password": "newpassword",
        "password_confirmation": "newpassword"
    }

Правила валидации
-----------------

..  code-block:: none

    'token' => 'required',
    'email' => 'required|email',
    'password' => 'required|confirmed|min:8',

Примеры ответов
---------------

Успешный сброс
~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": {
            "message": "Ваш пароль был успешно сброшен"
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
            "Поле token обязательно для заполнения.",
            "Поле E-Mail адрес должно быть действительным электронным адресом.",
            "Поле Пароль не совпадает с подтверждением."
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

Неверный токен
~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": false,
        "errorMessage": [
            "Ошибочный код сброса пароля"
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

