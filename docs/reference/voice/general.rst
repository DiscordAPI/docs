|stub| General
==============

Get Server Regions
------------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/voice/regions

Parameters
^^^^^^^^^^

Response
~~~~~~~~

An array of objects. Below is an example of a response with one location. There should be six objects, one for each server location: Amsterdam, London, Singapore, Sydney, US East, US West.

.. code-block:: json

    [
        {
            "sample_hostname": "us-west3.discord.gg",
            "sample_port": 80,
            "id": "us-west",
            "name": "US West"
        }
    ]



Move Member
-----------

Request
~~~~~~~

.. code-block:: http

	PATCH https://discordapp.com/api/guilds/:guild_id/members/:member_id

.. code-block:: json

	{
		"channel_id": "111222333444555666"
	}

Parameters
^^^^^^^^^^

	- **channel_id** (Required): ID of the channel to move the member to.

Response
~~~~~~~~

.. code-block:: json

    {
    }



???
---

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/voice/ice

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }
