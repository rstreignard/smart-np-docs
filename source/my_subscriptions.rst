Мои подписки
============

..  code-block:: none

    GET http://sjournal.milestns.beget.tech/api/v1/user/subscriptions

Примеры ответов
---------------

..  code-block:: none

    Status: 200

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
