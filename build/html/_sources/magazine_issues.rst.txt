Выпуски издания
===============

..  code-block:: none

    GET http://sjournal.milestns.beget.tech/api/v1/magazine-issues

Примеры ответов
---------------

Успешный ответ
~~~~~~~~~~~~~~

..  code-block:: none

    Status: 200

..  code-block:: none

    {
        "status": true,
        "errorMessage": null,
        "data": {
            "magazine_issues": [
                {
                    "id": 13,
                    "title": "Forbes Украина. Июнь",
                    "issue_date": "01 июня 2020",
                    "cover_image": "/storage/covers/4/GbB1eug9MNy36xYAEYRKNotXebUCI7AIdYS7eJoc.jpeg"
                },
                {
                    "id": 14,
                    "title": "Forbes Украина. Июль",
                    "issue_date": "01 июля 2020",
                    "cover_image": "/storage/covers/4/uhqdTi6kC30GERUZ4Hvv3QjsD21QQxyX7nzpqif8.jpeg"
                },
                {
                    "id": 26,
                    "title": "Детский 1. Июнь",
                    "issue_date": "06 августа 2020",
                    "cover_image": null
                }
            ]
        }
    }