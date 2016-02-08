Invites
=======

Get Invite
----------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/invite/:id_or_xkcd

Response
~~~~~~~~

See `Basic Invite Format`_.



Accept Invite
-------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/invite/:id_or_xkcd

Response
~~~~~~~~

See `Basic Invite Format`_.



Create Invite
-------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/channels/:id/invites

.. code-block:: json

    {
        "validate": "invite id"
    }

Parameters
^^^^^^^^^^

    - **validate** (Optional): Validate a cached invite ID

Response
~~~~~~~~

See `Rich Invite Format`_.



Delete Invite
-------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/invite/:id

Response
~~~~~~~~

See `Basic Invite Format`_.



Get Guild Invites
-----------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/guilds/:guild_id/invites

Response
~~~~~~~~

An array of invite objects. See `Rich Invite Format`_.



Get Channel Invites
-----------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/channels/:channel_id/invites

Response
~~~~~~~~

An array of invite objects. See `Rich Invite Format`_.



Basic Invite Format
-------------------

.. code-block:: json

    {
        "code": "0cFbBdvaQwODZPcF",
        "guild": {
            "id": "110451980584914944",
            "name": "Guild Name"
        },
        "xkcdpass": null,
        "channel": {
            "type": "text",
            "id": "110453227215937536",
            "name": "Channel Name"
        }
    }

Rich Invite Format
------------------

.. code-block:: json

    {
        "max_age": 86400,
        "code": "0cFbBdvaQwLBiyyI",
        "guild": {
            "id": "110451980584914944",
            "name": "Guild Name"
        },
        "revoked": false,
        "created_at": "2015-11-01T19:23:29.137000+00:00",
        "temporary": false,
        "uses": 0,
        "max_uses": 0,
        "inviter": {
            "username": "Person",
            "discriminator": "1849",
            "id": "112462135683509820",
            "avatar": null
        },
        "xkcdpass": null,
        "channel": {
            "type": "text",
            "id": "110453227215937536",
            "name": "Channel Name"
        }
    }
