|stub| Bans
===========

Get Bans
--------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/guilds/:guild_id/bans

Response
~~~~~~~~

An array of objects, each with a "user" property. Below is an example of a response with one banned user.

.. code-block:: json

    [
        {
            "user": {
                "username": "Some Username",
                "discriminator": "1234",
                "id": "111222333444555666",
                "avatar": "111222333444555666777888999aaabb"
            }
        }
    ]



Add Ban
-------

Request
~~~~~~~

.. code-block:: http

    PUT https://discordapp.com/api/guilds/:guild_id/bans/:user_id?delete-message-days=0

Parameters
^^^^^^^^^^

    - **delete-message-days** (Optional): Discord should delete messages by the banned user that are younger than # days



Remove Ban
----------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/guilds/:guild_id/bans/:user_id

Events
------

GUILD_BAN_ADD
~~~~~~~~~~~~~~

Ban has been added.

.. code-block:: json

    {
        "t": "GUILD_BAN_ADD",
        "s": 1,
        "op": 0,
        "d": {
            "user": {
                "username":"test user",
                "id":"111222333444555666",
                "discriminator":"1234",
                "avatar":null
            },
            "guild_id": "111222333444555666"
        }
    }
    
GUILD_BAN_REMOVE
~~~~~~~~~~~~~~

Ban has been removed.

.. code-block:: json

    {
        "t": "GUILD_BAN_REMOVE",
        "s": 1,
        "op": 0,
        "d": {
            "user": {
                "username":"test user",
                "id":"111222333444555666",
                "discriminator":"1234",
                "avatar":null
            },
            "guild_id": "111222333444555666"
        }
    }
    
