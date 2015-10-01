|stub| Signing In
=================

Login
-----

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/auth/login
	
Parameters
^^^^^^^^^^


.. code-block:: json

    {
        "email":"client email",
        "password":"client password"
    }


Response
~~~~~~~~

.. code-block:: json

    {
        "token": "token here"
    }
  
It's important you keep track of this token, as you will need this later for most of the HTTP requests, especially when you want to send or delete messages.
    	
Logout
------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/auth/logout

Parameters
^^^^^^^^^^

.. code-block:: json

    {
         "token": "token from login"
    }

Response
~~~~~~~~

.. code-block:: json

    {
    }
