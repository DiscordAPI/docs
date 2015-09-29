|stub| General
==============

Create Channel
--------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/guilds/:guild_id/channels
	
Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }
  
    	
Edit Channel
------------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/channels/:id

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }


Delete Channel
--------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/channels/:id

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }
    
Broadcast Typing
----------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/channels/:id/typing

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }


Events
------