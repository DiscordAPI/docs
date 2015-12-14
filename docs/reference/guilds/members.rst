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
