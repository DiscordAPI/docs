|stub| Profile
==============

Edit Profile
------------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/users/@me

.. code-block:: json

    {
        "avatar": "a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1",
        "email": "email@example.com",
        "new_password": "newpassword",
        "password": "password",
        "username": "Something"
    }

Parameters
^^^^^^^^^^

    - **avatar** (Required): The user's avatar ID to keep the current image, a base64 encoded image to set a new image, or null to remove
    - **email** (Required): The user's email (overwrites existing)
    - **password** (Required): The user's current password
    - **new_password** (Optional): The user's desired password
    - **username** (Required): The user's userame (overwrites existing)

Response
~~~~~~~~

.. code-block:: json

    {
        "avatar": "a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1",
        "discriminator": "1234",
        "email": "email@example.com",
        "id": "111222333444555666",
        "token": "your new login token",
        "username": "Something",
        "verified": true
    }

Example: changing the avatar image
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: json

    {
        "avatar": "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAMCAgICAgMCAgIDAwMDBAYEBAQ...",
        "email": "email@example.com",
        "new_password": "newpassword",
        "password": "password",
        "username": "Something"
    }
    
    
    
Events
------
    
USER_UPDATE
~~~~~~~~~~~~~~

.. code-block:: json

    {
        "t": "USER_UPDATE",
        "s": 1,
        "op": 0,
        "d": {
            "verified":true,
            "username":"Something",
            "id":"11122233344455566",
            "email":"email@example.com",
            "discriminator":"1234",
            "avatar":"a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1"
        }
    }

