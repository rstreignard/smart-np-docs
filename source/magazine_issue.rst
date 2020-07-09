Выпуск издания
==============

..  code-block:: none

    GET http://sjournal.milestns.beget.tech/api/v1/magazine-issues/{magazin_issue_id}

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
            "magazine_issue": {
                "id": 14,
                "magazine_id": 4,
                "title": "Forbes Украина. Июль",
                "body": "Lorem ipsum dolor sit amet",
                "issue_date": "01 июля 2020",
                "cover_image": "/storage/covers/4/JeOd8yoYhc6bdVPFnHXGOP1GkxMutzE0qq9PVx54.jpeg",
                "pdf_content_url": "http://sjournal.milestns.beget.tech/api/v1/magazine-issues/14/pdf-content",
                "pdf_encoded_content_url": "http://sjournal.milestns.beget.tech/api/v1/magazine-issues/14/encoded-pdf-content",
                "pdf_preview_url": "http://sjournal.milestns.beget.tech/api/v1/magazine-issues/14/pdf-preview",
                "pdf_download_url": "http://sjournal.milestns.beget.tech/api/v1/magazine-issues/14/pdf-download"
            },
            "magazine_issues": [
                {
                    "id": 13,
                    "title": "Forbes Украина. Июнь",
                    "issue_date": "01 июня 2020",
                    "cover_image": "/storage/covers/4/9nuvcGZyZIzyZ3bAN6q7VkKjWs9foH7LqmUUD6EI.jpeg"
                }
            ]
        }
    }