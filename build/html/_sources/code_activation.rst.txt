Активация кода
==============

..  code-block:: none

    POST http://sjournal.milestns.beget.tech/api/v1/user/code-activate

Пример запроса
--------------

..  code-block:: none

    {
        "code": "LEdTu9YkId"
    }

Примеры ответов
---------------

Успешная активация
~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": {
            "message": "Введенный код успешно активирован"
        }
    }

Попытка активации неверного кода
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": false,
        "errorMessage": [
            "Введен неверный или недействительный код"
        ],
        "data": null
    }

Попытка активации использованного кода
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": false,
        "errorMessage": [
            "Введеный код уже был активирован раннее"
        ],
        "data": null
    }

Попытка активации просроченного кода
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": false,
        "errorMessage": [
            "Срок действия введенного кода истек"
        ],
        "data": null
    }
    
Попытка активации при наличии активной подписки
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": false,
        "errorMessage": [
            "Введенный код не был активирован. У пользователя имеется активная подписка на данный пакет"
        ],
        "data": null
    }


