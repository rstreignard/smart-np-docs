Партнеры
========

..  code-block:: none

    GET http://sjournal.milestns.beget.tech/api/v1/partners

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
        "data": [
            {
                "id": 2,
                "title": "АЛЛО",
                "responsible_manager": "John Doe",
                "phone_number": "+01234567789",
                "email": "partner1@example.com",
                "website": "http://allo.com.ua",
                "logo": "/storage/partners/NN62yZWyvVQjh38nk06skO0ATJYC8ZH26dBSTRFs.jpeg"
            },
            {
                "id": 3,
                "title": "COMFY",
                "responsible_manager": "Jane Doe",
                "phone_number": "+9876543210",
                "email": "partner2@example.com",
                "website": "http://comfy.com.ua",
                "logo": null
            }
        ]
    }