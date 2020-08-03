Сгруппированные подписки
========================

..  code-block:: none

    GET http://sjournal.milestns.beget.tech/api/v1/user/grouped-subscriptions

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
                "id": 2,
                "title": "Мужской"
            },
            {
                "id": 4,
                "title": "Детский"
            }
        ]
    }
