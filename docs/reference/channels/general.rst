|stub| General
==============

Create Channel
--------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/guilds/:guild_id/channels

.. code-block:: json

    {
        "name":"channel name",
        "type":"text"
    }

Parameters
^^^^^^^^^^

    - **name** (Required): The name of the channel to create. Name must be 2-100 characters long
    - **type** (Required): Should be `text` for text channels, or `voice` for voice channels

Response
~~~~~~~~

See `Channel Format`_.


Edit Channel
------------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/channels/:id

.. code-block:: json

    {
        "name": "channel name"
    }

Parameters
^^^^^^^^^^

    - **name** (Required): The new name of the channel. Name must be 2-100 characters long.

Response
~~~~~~~~

See `Channel Format`_.


Delete Channel
--------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/channels/:id

Response
~~~~~~~~

See `Channel Format`_.

Broadcast Typing
----------------

Broadcasts to all members of a channel that you are currently typing. Each request will maintain the typing state for the next 5 seconds.

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/channels/:id/typing


Events
------



Channel Format
--------------

.. code-block:: json

    {
        "guild_id": "111222333444555666",
        "name": "some name",
        "permission_overwrites": [],
        "topic": null,
        "position": 2,
        "last_message_id": null,
        "type": "text",
        "id": "111222333444555666",
        "is_private": false
    }