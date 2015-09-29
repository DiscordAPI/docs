|stub| Messages
===============

Get Messages
------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/channels/:channel_id/messages
	
Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }



Create Message
--------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/channels/:channel_id/messages
	
Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }
  
    	
Edit Message
------------

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/channels/:channel_id/messages/:id

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }


Delete Message
--------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/channels/:channel_id/messages/:id

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }


Events
------