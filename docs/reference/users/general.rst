General
==============

Create Private Channel
----------------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/users/:id/channels

.. code-block:: json

    {
        "recipient_id": "111222333444555666"
    }

Parameters
^^^^^^^^^^

    - **recipient_id** (Required): User ID of the person to open a direct message with

Response
~~~~~~~~

.. code-block:: json

    {
        "id": "111222333444555666",
        "is_private": true,
        "last_message_id": null,
        "recipient": {
            "username": "Someone",
            "id": "111222333444555666",
            "discriminator": "1234",
            "avatar": "a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1"
        }
    }

Note: The first "id" is the DM channel ID



Get Avatar
----------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/users/:user_id/avatars/:avatar_id.jpg

Response
~~~~~~~~

A JPG of the user's avatar