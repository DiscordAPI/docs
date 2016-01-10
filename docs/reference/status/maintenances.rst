|stub| Maintenances
===================

Active Maintenances?
--------------------

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
----------------------

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


Maintenance Format
------------------

.. code-block:: json

    {
        "name": "Call the Moving Van!",
        "status": "scheduled",
        "created_at": "2016-01-09T13:24:35.249-08:00",
        "updated_at": "2016-01-09T13:25:05.482-08:00",
        "monitoring_at": null,
        "resolved_at": null,
        "shortlink": "http://stspg.io/1q1G",
        "scheduled_for": "2016-01-12T02:00:00.000-08:00",
        "scheduled_until": "2016-01-12T03:00:00.000-08:00",
        "id": "bclbdmdnhmdn",
        "page_id": "srhpyqt94yxb",
        "incident_updates": [
            {
                "status": "scheduled",
                "body": "Beginning over the holidays our Data Center provider has been targeted by repeated DDoS attacks of epic proportions. We’re talking Vanish Doom level stuff. Unfortunately, that’s meant Discord has been… fizzy every now and then.\r\n\r\nSo we're moving! We’ve scoped out the neighborhood and found a more resilient Data Center provider just around the corner. After much deliberation we decided the most straightforward maneuver is to take Discord down for an hour-ish. In the middle of the night. While most of you are sleeping.",
                "created_at": "2016-01-09T13:24:35.508-08:00",
                "updated_at": "2016-01-09T13:24:35.508-08:00",
                "display_at": "2016-01-09T13:24:35.508-08:00",
                "id": "ccdjfjmkpjhl",
                "incident_id": "bclbdmdnhmdn"
            }
        ],
        "impact": "none"
    }
