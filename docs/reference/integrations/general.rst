|stub| General
==============

Get Server Integrations
-----------------------

Request
~~~~~~~

.. code-block:: http

	GET https://discordapp.com/api/guilds/:guild_id/integrations

Response
~~~~~~~~

An array of integration objects. See `Twitch Format`_ or `YouTube Gaming Format`_.



Delete Integration
------------------

Request
~~~~~~~

.. code-block:: http

	DELETE https://discordapp.com/api/guilds/:guild_id/integrations/:integration_id



Edit Integration
----------------

Request
~~~~~~~

.. code-block:: http

	PATCH https://discordapp.com/api/guilds/:guild_id/integrations/:integration_id

Parameters
^^^^^^^^^^

	- **enable_emoticons** (Optional): Enable in-chat emoticons associated with the integration (boolean).
	- **expire_behaviour** (Optional): How the integration will expire (integer).
	- **expire_grace_period** (Optional): Amount of days to ignore subscription expiration (integer).
	- **enable** (Optional): Enable the integration (boolean).

Response
~~~~~~~~

See `Twitch Format`_ or `YouTube Gaming Format`_.


Twitch Format
-------------

.. code-block:: json

	{
		{
			"subscriber_count": 1,
			"syncing": false,
			"enable_emoticons": true,
			"expire_behavior": 0,
			"user": {
				"username": "Discord username",
				"discriminator": "1234",
				"id": "discord account ID",
				"avatar": "avatar ID"
			},
			"id": "integration ID",
			"expire_grace_period": 3,
			"account": {
				"id": "twitch ID",
				"name": "twitch username"
			},
			"name": "twitch username",
			"enabled": true,
			"role_id": "subscriber role ID",
			"synced_at": "2016-02-06T00:00:00.000000+00:00",
			"type": "twitch",
		}
	}

YouTube Gaming Format
---------------------

.. code-block:: json

	{

	}

Emoji Format
------------

.. code-block:: json

	{
		"roles": [ "111222333444555666" ],
		"require_colons": false,
		"name": "Kappa",
		"managed": true,
		"id": "123456789101112131"
	}