Messages
========

Get Messages
------------

Gets a block of messages from the provided channel.

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/channels/:channel_id/messages?before=111222333444555666&after=111222333444555666&limit=50

Parameters
^^^^^^^^^^

    - **before** (Optional): Gets messages before a given message ID.
    - **after** (Optional): Gets messages after a given message ID.
    - **limit** (Optional): Max number of messages to return. Default: 50

Response
~~~~~~~~

See `Message Format`_.



Send Message
------------

Sends a message to the provided channel.

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/channels/:channel_id/messages

.. code-block:: json

    {
        "content": "I'm a test message~",
        "mentions": ["111222333444555666"],
        "nonce": "1453949470692605952",
        "tts": false
    }

Parameters
^^^^^^^^^^

    - **content**: The text of the message. Supports basic markdown formatting.
    - **mentions** (Optional): An array of the ids of all users this message is mentioning.
    - **nonce** (Optional): A unique ID assigned to this message. Has no purpose other than being sent back to you in the MESSAGE_CREATE event.
    - **tts** (Optional): Should this message be broadcast using Text-To-Speech? (default: false)

Response
~~~~~~~~

See `Message Format`_.



Edit Message
------------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/channels/:channel_id/messages/:id

.. code-block:: json

    {
        "content": "I'm a test message~",
        "mentions": ["111222333444555666"]
    }

Parameters
^^^^^^^^^^

    - **content**: The text of the message. Supports basic markdown formatting.
    - **mentions** (Optional): An array of the ids of all users this message is mentioning.

Response
~~~~~~~~

See `Message Format`_.



Delete Message
--------------

Deletes the provided message.

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/channels/:channel_id/messages/:id

Acknowledge Message
-------------------

Marks the provided message ID as read.

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/channels/:channel_id/messages/:id/ack



Events
------

MESSAGE_CREATE
~~~~~~~~~~~~~~

A message was sent in one of the channels you have read access to.
Note: d is in `Message Format`_.

.. code-block:: json

    {
        "t": "MESSAGE_CREATE",
        "s": 1,
        "op": 0,
        "d": {...}
    }

MESSAGE_UPDATE
~~~~~~~~~~~~~~

A message was updated in one of the channels you have read access to.
Note: d is in `Message Format`_.

.. code-block:: json

    {
        "t": "MESSAGE_UPDATE",
        "s": 1,
        "op": 0,
        "d": {...}
    }

MESSAGE_DELETE
~~~~~~~~~~~~~~

A message was deleted in one of the channels you have read access to.

.. code-block:: json

    {
        "t": "MESSAGE_UPDATE",
        "s": 1,
        "op": 0,
        "d": {
            "id": "111222333444555666",
            "channel_id": "111222333444555666"
        }
    }

MESSAGE_ACK
~~~~~~~~~~~

You acknowledged a message on another machine.

.. code-block:: json

    {
        "t": "MESSAGE_ACK",
        "s": 1,
        "op": 0,
        "d": {
            "message_id": "101739512769544192",
            "channel_id": "81385020756865024"
        }
    }



Message Format
--------------

.. code-block:: json

    {
        "nonce": "1453949470692605952",
        "attachments": [],
        "tts": false,
        "embeds": [],
        "timestamp": "2015-10-07T20:12:45.743000+00:00",
        "mention_everyone": false,
        "id": "111222333444555666",
        "edited_timestamp": null,
        "author": {
            "username": "Test Account",
            "discriminator": "1234",
            "id": "111222333444555666",
            "avatar": "31171c07640015bbc5aed21b28ea2408"
        },
        "content": "I'm a test message~",
        "channel_id": "81384788765712384",
        "mentions": []
    }