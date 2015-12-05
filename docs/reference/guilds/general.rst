General
==============

Create Guild
------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/guilds

.. code-block:: json

    {
        "name": "guild name"
    }

Parameters
^^^^^^^^^^

    - **name** (Required): The name of the guild to create. Name must be 2-100 characters long

Response
~~~~~~~~

See `Guild Format`_.



Edit Guild
----------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/guilds/:id

.. code-block:: json

    {
        "name": "guild name"
    }

Parameters
^^^^^^^^^^

    - **name** (Required): The new name of the guild. Name must be 2-100 characters long.

Response
~~~~~~~~

See `Guild Format`_.



Delete/Leave Guild
------------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/guilds/:id

Response
~~~~~~~~

See `Guild Format`_.



Get Guild Channels
------------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/guilds/:id/channels

Response
~~~~~~~~

An array of channel objects. See `Channel format <../channels/general.html#channel-format>`_.



Guild Format
--------------

.. code-block:: json

    {
        "afk_timeout": 300,
        "joined_at": "2012-12-21T12:34:56.789012+00:00",
        "afk_channel_id": null,
        "id": "111222333444555666",
        "icon": null,
        "name": "Name",
        "roles": [
            {
                "managed": false,
                "name": "@everyone",
                "color": 0,
                "hoist": false,
                "position": -1,
                "id": "111222333444555666",
                "permissions": 12345678
            }
        ],
        "region": "us-west",
        "embed_channel_id": null,
        "embed_enabled": false,
        "owner_id": "111222333444555666"
    }