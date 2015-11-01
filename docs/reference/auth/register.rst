|stub| Registering
==================

Register
--------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/auth/register

.. code-block:: json

    {
        "email":"account email",
        "password":"account password",
        "username": "account username",
        "invite": "invite code or null",
        "fingerprint": null
    }

Parameters
^^^^^^^^^^

    - **email** (Optional with invite code): The email to register with. Emails must follow standard email formatting (username@example.com)
    - **username** (Required): The username to register with. Usernames must be 1-32 characters long.
    - **password** (Optional with invite code): The password to register with.
    - **invite** (Optional): The invite code to join with (bypasses email/password registration).
    - **fingerprint** (Optional): ?

Response
~~~~~~~~

.. code-block:: json

    {
    	"token": "token here"
    }

It's important you keep track of this token, as most HTTP API requests will require an `Authorization` header containing this token.



Get anonymous fingerprint
-------------------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/auth/fingerprint

Response
~~~~~~~~

.. code-block:: json

    {
    }