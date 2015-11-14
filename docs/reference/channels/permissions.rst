|stub| Permissions
==================

Create/Edit Permission
----------------------

Request
~~~~~~~

.. code-block:: http

    PUT https://discordapp.com/api/channels/:channel_id/permissions/:target_id

.. code-block:: json

    {
        "allow": 251905,
        "deny": 8216,
        "id": "111222333444555666",
        "type": "role"
    }

Parameters
^^^^^^^^^^

    - **allow** (Required): The allow permissions number of the role (overwrites existing). See `Permissions Number`_.
    - **deny** (Required): The deny permissions number of the role (overwrites existing). See `Permissions Number`_.
    - **id** (Required): The ID of the permission target (same as :target_id in URL)
    - **type** (Required): The type of the permission target (either member or role)



Delete Permission
--------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/channels/:channel_id/permissions/:target_id



Events
------



Permissions Number
------------------

Overall permission numbers are sums of the enabled individual permission numbers.

Individual permission numbers are bit-shifted. A list (borrowed from discord.js) is below:

General:
~~~~~~~~

+------------------------+---------+
|       Permission       |  Shift  |
+========================+=========+
| Create Instant Invite  | 1 <<  0 |
+------------------------+---------+
| Kick Members           | 1 <<  1 |
+------------------------+---------+
| Ban Members            | 1 <<  2 |
+------------------------+---------+
| Manage Roles           | 1 <<  3 |
+------------------------+---------+
| Manage Permissions     | 1 <<  3 |
+------------------------+---------+
| Manage Channels        | 1 <<  4 |
+------------------------+---------+
| Manage Channel         | 1 <<  4 |
+------------------------+---------+
| Manage Server          | 1 <<  5 |
+------------------------+---------+

Chat:
~~~~~

+------------------------+---------+
|       Permission       |  Shift  |
+========================+=========+
| Read Messages          | 1 << 10 |
+------------------------+---------+
| Send Messages          | 1 << 11 |
+------------------------+---------+
| Send TTS Messages      | 1 << 12 |
+------------------------+---------+
| Manage Messages        | 1 << 13 |
+------------------------+---------+
| Embed Links            | 1 << 14 |
+------------------------+---------+
| Attach Files           | 1 << 15 |
+------------------------+---------+
| Read Message History   | 1 << 16 |
+------------------------+---------+
| Mention Everyone       | 1 << 17 |
+------------------------+---------+

Voice:
~~~~~~

+------------------------+---------+
|       Permission       |  Shift  |
+========================+=========+
| Voice Connect          | 1 << 20 |
+------------------------+---------+
| Voice Speak            | 1 << 21 |
+------------------------+---------+
| Voice Mute Members     | 1 << 22 |
+------------------------+---------+
| Voice Deafen Members   | 1 << 23 |
+------------------------+---------+
| Voice Move Members     | 1 << 24 |
+------------------------+---------+
| Voice Use VAD          | 1 << 25 |
+------------------------+---------+