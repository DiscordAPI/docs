|stub| The Ready Event
======================

READY Event
-----------

.. code-block:: json

    {
        "t": "READY",
        "s": 1,
        "op": 0,
        "d": {
            "v": 3,
            "user": {
                "verified": true,
                "username": "Test Account",
                "id": "11122233344455566",
                "email": "discordbot@ironboots.net",
                "discriminator": "1234",
                "avatar": null
            },
            "session_id": "aaaabbbbccccddddeeeeffffgggghhhh",
            "read_state": [
                {
                    "mention_count": 0,
                    "last_message_id": "11122233344455566",
                    "id": "11122233344455566"
                }
            ],
            "private_channels": [
                {
                    "recipient": {
                        "username": "Other Test Account",
                        "id": "11122233344455566",
                        "discriminator": "1234",
                        "avatar": "23e8fc19b243a62cc9cc3ea40fe1c2e0"
                    },
                    "last_message_id": "11122233344455566",
                    "is_private": true,
                    "id": "11122233344455566"
                }
            ],
            "heartbeat_interval": 41250,
            "guilds": [
                {
                    "voice_states": [
                        {
                            "user_id": "11122233344455566",
                            "token": "aaaabbbbccccdddd",
                            "suppress": true,
                            "session_id": "aaaabbbbccccddddeeeeffffgggghhhh",
                            "self_mute": false,
                            "self_deaf": false,
                            "mute": false,
                            "deaf": false,
                            "channel_id": "11122233344455566"
                        }                
                    ],
                    "roles": [
                        {
                            "permissions": 36953089,
                            "name": "@everyone",
                            "id": "11122233344455566"
                        }
                    ],
                    "region": "us-east",
                    "presences": [
                        {
                            "user": {
                                "id": "11122233344455566"
                            },
                            "status": "online",
                            "game_id": null
                        }
                    ],
                    "owner_id": "11122233344455566",
                    "name": "Example Server",
                    "members": [
                        {
                            "user": {
                                "username": "Voltana",
                                "id": "53905483156684800",
                                "discriminator": "3721",
                                "avatar": "23e8fc19b243a62cc9cc3ea40fe1c2e0"
                            },
                            "roles": [],
                            "mute": false,
                            "joined_at": "2015-09-26T23:29:51.680000+00:00",
                            "deaf": false
                        }
                    ],
                    "joined_at": "2015-10-06T23:47:08.465452+00:00",
                    "id": "97474751190011904",
                    "icon": null,
                    "channels": [
                        {
                            "type": "text",
                            "topic": null,
                            "position": 0,
                            "permission_overwrites": [],
                            "name": "general",
                            "last_message_id": "101127292343812096",
                            "id": "97474751190011904"
                        }
                    ],
                    "afk_timeout": 300,
                    "afk_channel_id": null
                }
            ]
        }
    }