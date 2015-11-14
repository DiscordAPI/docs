|stub| Members
==============

Get Members
-----------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/guilds/:id/members

Response
~~~~~~~~

An array of objects. Below is an example of a response with one member.

.. code-block:: json

    [
        {
            "joined_at": "2015-10-10T10:10:10.100000+00:00",
            "deaf": false,
            "user": {
                "username": "Some User",
                "discriminator": "1234",
                "id": "111222333444555666",
                "avatar": null
            },
            "roles": [
                "111222333444555666"
            ],
            "mute": false
        }
    ]



Edit Member
-----------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/guilds/:guild_id/members/:user_id

.. code-block:: json

    {
        roles: ["111222333444555666"]
    }

Parameters
^^^^^^^^^^

    - **roles** (Required): A list of roles the user should be in (overwrites)



Kick Member
-----------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/guilds/:guild_id/members/:user_id



Events
------