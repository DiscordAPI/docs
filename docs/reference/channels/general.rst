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
    - **type** (Required): Should be "text" for text channels, or "voice" for voice channels

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
        "name": "channel name",
        "position": 0,
        "topic": "a topic"
    }

Parameters
^^^^^^^^^^

    - **name** (Required): The new name of the channel. Name must be 2-100 characters long.
    - **position** (Required): The position of the channel to edit.
    - **topic** (Required): The new topic of the channel.

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

CHANNEL_CREATE (Public)
~~~~~~~~~~~~~~

A channel has been created in one of guilds.
Note: d is in `Channel Format`_.

.. code-block:: json

    {
        "t": "MESSAGE_CREATE",
        "s": 1,
        "op": 0,
        "d": {...}
    }
    
CHANNEL_CREATE (Private)
~~~~~~~~~~~~~~

You have got a first private message from person.

.. code-block:: json

    {
        "t": "MESSAGE_CREATE",
        "s": 1,
        "op": 0,
        "d": {
            "recipient": {
                "username": "test user",
                "id": "1111222233334444555666",
                "discriminator": "1234",
                "avatar": "..."
            },
            "last_message_id": null,
            "is_private": true,
            "id": "11112222333344445555666"
        }
    }
    
CHANNEL_UPDATE
~~~~~~~~~~~~~~

Channel details has been updated.
Note: d is in `Channel Format`_.

.. code-block:: json

    {
        "t": "CHANNEL_UPDATE",
        "s": 1,
        "op": 0,
        "d": {...}
    }
    
CHANNEL_DELETE (Public)
~~~~~~~~~~~~~~

Channel has been deleted.
Note: d is in `Channel Format`_.

.. code-block:: json

    {
        "t": "CHANNEL_DELETE",
        "s": 1,
        "op": 0,
        "d": {...}
    }
    
CHANNEL_DELETE (Private)
~~~~~~~~~~~~~~

Private channel has been deleted.

.. code-block:: json

    {
        "t": "CHANNEL_DELETE",
        "s": 1,
        "op": 0,
        "d": {
            "recipient": {
                "username": "test user",
                "id": "1111222233334444555666",
                "discriminator": "1234",
                "avatar": "..."
            },
            "last_message_id": null,
            "is_private": true,
            "id": "11112222333344445555666"
        }
    }

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
