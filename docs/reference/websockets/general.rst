|stub| General
==============

Get Gateway Server
------------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/gateway
	
Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    	"url":"wss://gateway-cerberus.discord.gg"
    }
    
    The URL shown here is a common example of one. It's best to always use the URL you receive from your GET request instead of statically connecting to the URL here.
