|stub| Members
==============

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

GUILD_MEMBER_ADD
~~~~~~~~~~~~~~

Member has joined to the guild.

.. code-block:: json

    {
        "t": "GUILD_MEMBER_ADD",
        "s": 1,
        "op": 0,
        "d": {
            "user":{
                "username":"test user",
                "id":"111222333444555666",
                "discriminator":"1234",
                "avatar":null
            },
            "roles":[],
            "joined_at":"2016-01-02T16:14:21.451424+00:00",
            "guild_id":"111222333444555666"
        }
    }
    
GUILD_MEMBER_UPDATE
~~~~~~~~~~~~~~

Member get a new role, etc.

.. code-block:: json

    {
        "t": "GUILD_MEMBER_UPDATE",
        "s": 1,
        "op": 0,
        "d": {
            "user":{
                "username":"test user",
                "id":"111222333444555666",
                "discriminator":"1234",
                "avatar":null
            },
            "roles":[],
            "joined_at":"2016-01-02T16:14:21.451424+00:00",
            "guild_id":"111222333444555666"
        }
    }
    
GUILD_MEMBER_REMOVE
~~~~~~~~~~~~~~

Member has been kicked form the guild.

.. code-block:: json

    {
        "t": "GUILD_MEMBER_REMOVE",
        "s": 1,
        "op": 0,
        "d": {
            "user":{
                "username":"test user",
                "id":"111222333444555666",
                "discriminator":"1234",
                "avatar":null
            },
            "roles":[],
            "joined_at":"2016-01-02T16:14:21.451424+00:00",
            "guild_id":"111222333444555666"
        }
    }
