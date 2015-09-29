|stub| Invites
==============
	    
Get Invite
----------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/invite/:id_or_xkcd

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }
    
    
Create Invite
-------------

Request
~~~~~~~

.. code-block:: http

    PUT https://discordapp.com/api/channels/:id/invites

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }

    
Accept Invite
-------------

Request
~~~~~~~

.. code-block:: http

    POSTs https://discordapp.com/api/invite/:id

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }
        
    
Delete Invite
-------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/invite/:id

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }