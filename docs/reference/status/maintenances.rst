|stub| Maintenances
===================

Active Maintenances?
---

Request
~~~~~~~

.. code-block:: http

    GET https://status.discordapp.com/api/v2/scheduled-maintenances/active.json

Response
~~~~~~~~

.. code-block:: json

    {
        "page": {
            "id": "srhpyqt94yxb",
            "name": "Discord",
            "url": "http://status.discordapp.com",
            "updated_at": "2015-10-10T10:10:10.100-08:00"
        },
        "scheduled_maintenances": []
    }


Upcoming Maintenances?
---

Request
~~~~~~~

.. code-block:: http

    GET https://status.discordapp.com/api/v2/scheduled-maintenances/upcoming.json

Response
~~~~~~~~

.. code-block:: json

    {
        "page": {
            "id": "srhpyqt94yxb",
            "name": "Discord",
            "url": "http://status.discordapp.com",
            "updated_at": "2015-10-10T10:10:10.100-08:00"
        },
        "scheduled_maintenances": []
    }
