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
        "name": "guild name",
        "region": "region name",
        "icon": "icon"
    }

Parameters
^^^^^^^^^^

    - **name** (Required): The name of the guild to create. Name must be 2-100 characters long
    - **region** (Required): Region name received by `voice/regions <https://github.com/DiscordAPI/docs/blob/master/docs/reference/voice/general.rst#get-server-regions>`_ (Example: us-west)
    - **icon** (Optional): Icon image 128x128px in format like: data:image/jpg;base64,dGVzdDEy ... (Set null if don't needed)
    
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
        "name": "guild name",
        "region": "region name",
        "icon": "icon",
        "afk_channel_id": "channel id",
        "afk_timeout": "timeout"
    }

Parameters
^^^^^^^^^^

    - **name** (Required): The new name of the guild. Name must be 2-100 characters long.
    - **region** (Optional): Region name received by `voice/regions <https://github.com/DiscordAPI/docs/blob/master/docs/reference/voice/general.rst#get-server-regions>`_
    - **icon** (Optional): Icon image 128x128px in format like: data:image/jpg;base64,dGVzdDEy ... (Set null if don't needed)
    - **afk_channel_id** (Optional): Channel id for AFK channel (Set null if don't needed)
    - **afk_timeout** (Optional): AFK timeout for the guild (valid values are: 60,300,900,1800,3600)

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



Get Guilds
----------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/users/@me/guilds

Response
~~~~~~~~

An array of guild objects. See `Guild Format`_.



Get Guild Channels
------------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/guilds/:id/channels

Response
~~~~~~~~

An array of channel objects. See `Channel format <../channels/general.rst#channel-format>`_.



Events
------
    
GUILD_CREATE
~~~~~~~~~~~~~~

A guild has been created.
Note: d is in `Guild Format`_.

.. code-block:: json

    {
        "t": "GUILD_CREATE",
        "s": 1,
        "op": 0,
        "d": {...}
    }


GUILD_UPDATE
~~~~~~~~~~~~~~

A guild has been edited by owner.
Note: d is in `Guild Format`_.

.. code-block:: json

    {
        "t": "GUILD_UPDATE",
        "s": 1,
        "op": 0,
        "d": {...}
    }
    

GUILD_DELETE
~~~~~~~~~~~~~~

Guild has been deleted by owner or you have leaved the guild.
Note: d is in `Guild Format`_.

.. code-block:: json

    {
        "t": "GUILD_DELETE",
        "s": 1,
        "op": 0,
        "d": {...}
    }
    

Guild Format
--------------

.. code-block:: json

    {
        "features": [],
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
        "splash": null,
        "emojis": [],
        "owner_id": "111222333444555666"
    }
