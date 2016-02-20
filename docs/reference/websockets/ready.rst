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
            "user_settings": {
                "theme": "light",
                "show_current_game": true,
                "render_embeds": true,
                "muted_channels": [],
                "message_display_compact": false,
                "locale": "en-US",
                "inline_embed_media": true,
                "inline_attachment_media": true,
                "enable_tts_command": true,
                "convert_emoticons": true
            },
            "user_guild_settings": [
                {
                    "suppress_everyone": false,
                    "muted": false,
                    "mobile_push": true,
                    "message_notifications": 1,
                    "guild_id": "11122233344455566",
                    "channel_overrides": []
                }
            ],
            "user": {
                "verified": true,
                "username": "Test Account",
                "id": "11122233344455566",
                "email": "discordbot@ironboots.net",
                "discriminator": "1234",
                "avatar": "a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1"
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
                        "avatar": "a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1"
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
                            "suppress": true,
                            "session_id": "aaaabbbbccccddddeeeeffffgggghhhh",
                            "self_mute": false,
                            "self_deaf": false,
                            "mute": false,
                            "deaf": false,
                            "channel_id": "11122233344455566"
                        }
                    ],
                    "splash": null,
                    "roles": [
                        {
                            "position": 1,
                            "permissions": 36953089,
                            "name": "@everyone",
                            "managed": false,
                            "id": "11122233344455566",
                            "hoist": false,
                            "color": 0
                        }
                    ],
                    "region": "us-east",
                    "presences": [
                        {
                            "user": {
                                "id": "11122233344455566"
                            },
                            "status": "online",
                            "game": null
                        }
                    ],
                    "owner_id": "11122233344455566",
                    "name": "Example Server",
                    "member_count": 1,
                    "members": [
                        {
                            "user": {
                                "username": "Test Account",
                                "id": "11122233344455566",
                                "discriminator": "1234",
                                "avatar": "a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1a1"
                            },
                            "roles": ["11122233344455566"],
                            "mute": false,
                            "joined_at": "2015-12-25T19: 30: 47.982000+00: 00",
                            "deaf": false
                        }
                    ],
                    "large": false,
                    "joined_at": "2015-12-25T19: 30: 47.982000+00: 00",
                    "id": "11122233344455566",
                    "icon": null,
                    "features": [],
                    "emojis": [],
                    "channels": [
                        {
                            "type": "text",
                            "topic": "Test Text Channel",
                            "position": 0,
                            "permission_overwrites": [
                                {
                                    "type": "role",
                                    "id": "11122233344455566",
                                    "deny": 36864,
                                    "allow": 0
                                }
                            ],
                            "name": "general",
                            "last_message_id": "111222333444555666",
                            "id": "11122233344455566"
                        },
                        {
                            "type": "voice",
                            "topic": "",
                            "position": 0,
                            "permission_overwrites": [],
                            "name": "Test Voice Channel",
                            "last_message_id": null,
                            "id": "111222333444555667"
                        },
                        {
                            "type": "voice",
                            "topic": "",
                            "position": 0,
                            "permission_overwrites": [
                                {
                                    "type": "role",
                                    "id": "111222333444555666",
                                    "deny": 65011737,
                                    "allow": 0
                                }
                            ],
                            "name": "Test AFK channel",
                            "last_message_id": null,
                            "id": "111222333444555670"
                        },
                    ],
                    "afk_timeout": 300,
                    "afk_channel_id": "111222333444555670"
                }
            ]
        }
    }

Keys
^^^^^^^^^^

    - **user_settings**: Values of some Discord Settings.
    - **user_guild_settings**: Array of guilds Notification Settings.
    - **user**: Information about the current user.
    - **session_id**: Current session id.
    - **read_state**: Array of channels read states in format:
        - **mention_count**: Count of mentions for the current user.
        - **last_message_id**: ID of the last message.
        - **id**: Channel ID.
    - **private_channels**: Array of private channels.
    - **heartbeat_interval**: Interval for `keepalive <https://github.com/DiscordAPI/docs/blob/master/docs/reference/websockets/general.rst#keepalive>`_.
    - **guilds**: Array of current guilds in `Guild Format <https://github.com/DiscordAPI/docs/blob/master/docs/reference/guilds/general.rst#guild-format>`_ with additional keys:
        - **voice_states**: Array of members voice states.
        - **presences**: Array of memebers statuses.
        - **members**: Array of guild members.
        - **channels**: Array of guild channels in `Channel Format <https://github.com/DiscordAPI/docs/blob/master/docs/reference/channels/general.rst#channel-format>`_.
