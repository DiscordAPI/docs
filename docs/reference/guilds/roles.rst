|stub| Roles
============

Create Role
-----------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/guilds/:id/roles

Response
~~~~~~~~

See `Role Format`_.



Edit Role
---------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/guilds/:guild_id/roles/:role_id

.. code-block:: json

    {
        "color": 0,
        "hoist": true,
        "name": "New Name",
        "permissions": 33333333
    }

Parameters
^^^^^^^^^^

    - **color** (Required): The color the role should have (as a decimal, **not hex**)
    - **hoist** (Required): Whether to display the role's users separately
    - **name** (Required): The role's name (overwrites existing)
    - **permissions** (Required): The overall permissions number of the role (overwrites existing). See `Permissions Number <../channels/permissions.html#permissions-number>`_.

Response
~~~~~~~~

See `Role Format`_.



Reorder Roles
---------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/guilds/:guild_id/roles

.. code-block:: json

    [
        {
            "id": "111222333444555666",
            "position": 1
        },
        {
            "id": "111222333444555667",
            "position": 2
        }
    ]

Parameters
^^^^^^^^^^

Reorder Roles requires an array of objects. Above is an example on a server with two roles. After this request is executed, the order of the roles will be #111222333444555666, #111222333444555667, then @everyone (always last).

The following are required for each object in the array:
    - **id** (Required): The id of the role the object represents
    - **position** (Required): The desired position of this role (# >= 1)

Response
~~~~~~~~

An array of objects. Each object is a `Role Format`_.

Note: the response includes the @everyone role, which has position -1.



Delete Role
-----------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/guilds/:guild_id/roles/:role_id

Events
------



Role Format
-----------

.. code-block:: json

    {
        "color": 0,
        "hoist": false,
        "id": "111222333444555666",
        "managed": false,
        "name": "new role",
        "permissions": 36953089,
        "position": 2
    }