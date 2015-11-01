|stub| Signing In
=================

Login
-----

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/auth/login

.. code-block:: json

    {
        "email":"client email",
        "password":"client password"
    }

Parameters
^^^^^^^^^^

    - **email** (Required): The email to login with.
    - **password** (Required): The password to login with.

Response
~~~~~~~~

.. code-block:: json

    {
        "token": "token here"
    }

It's important you keep track of this token, as most HTTP API requests will require an `Authorization` header containing this token.



Logout
------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/auth/logout

.. code-block:: json

    {
         "token": "token from login"
    }

Parameters
^^^^^^^^^^

    - **token** (Required): The token you logged in with.

Response
~~~~~~~~

.. code-block:: json

    {
    }
