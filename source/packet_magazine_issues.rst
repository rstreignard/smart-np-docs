Выпуски издания по подписке
===========================

..  code-block:: none

    GET http://sjournal.milestns.beget.tech/api/v1/packets/{packet_id}/magazine-issues

Примеры ответов
---------------

Перечень выпусков
~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": {
            "packet_id": 2,
            "magazine_issues": [
                {
                    "id": 13,
                    "title": "Forbes Украина. Июнь",
                    "issue_date": "01 июня 2020",
                    "cover_image": "/storage/covers/4/9nuvcGZyZIzyZ3bAN6q7VkKjWs9foH7LqmUUD6EI.jpeg"
                },
                {
                    "id": 14,
                    "title": "Forbes Украина. Июль",
                    "issue_date": "01 июля 2020",
                    "cover_image": "/storage/covers/4/JeOd8yoYhc6bdVPFnHXGOP1GkxMutzE0qq9PVx54.jpeg"
                }
            ]
        }
    }

Отсутствие выпусков по данной подписке
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": {
            "packet_id": 3,
            "magazine_issues": []
        }
    }