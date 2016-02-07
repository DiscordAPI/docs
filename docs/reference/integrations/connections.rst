|stub| Connections
==================

Get All Connections
-------------------

Request
~~~~~~~

.. code-block:: http

    GET https://discordapp.com/api/users/@me/connections

Response
~~~~~~~~

An array of connections. See `Connection Format`_.


Connection Format
-----------------

.. code-block:: json

	{
		"type": "twitch",
		"name": "Twitch username",
		"id": "11223344",
		"integrations": [
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
			},
		],
	}