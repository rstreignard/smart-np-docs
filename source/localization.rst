Локализация
===========

Локализация контента и возвращаемых ошибок осуществляется путем передачи в заголовке параметра ``Accept-Language``:

..  code-block:: none

    Accept-Language: ru / uk

..  note::

    В случае отсутствия в запросе данного заголовка, сервер возвращает данные по умолчанию на русском языке

Примеры ответов
---------------

..  code-block:: none

    Accept-Language: ru

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": [
            {
                "title": "Семейный",
                "subscription_end_date": "22 июля 2020"
            },
            {
                "title": "Мужской",
                "subscription_end_date": "21 сентября 2020"
            },
            {
                "title": "Детский",
                "subscription_end_date": "06 июля 2020"
            }
        ]
    }

----

..  code-block:: none

    Accept-Language: uk

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": [
            {
                "title": "Сімейний",
                "subscription_end_date": "22 липня 2020"
            },
            {
                "title": "Мужской",
                "subscription_end_date": "21 вересня 2020"
            },
            {
                "title": "Дитячий",
                "subscription_end_date": "06 липня 2020"
            }
        ]
    }