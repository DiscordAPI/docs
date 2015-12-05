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
-----------------

Request
~~~~~~~

.. code-block:: http

    DELETE https://discordapp.com/api/channels/:channel_id/permissions/:target_id



Events
------



Permissions Number
------------------

Overall permission numbers are stored as decimal, but interpreted as bits. Each bit stores one permission's state. The bit indexes of each permission are below.

Note: Instead of having 3 states (none/allow/deny), channel permissions are stored as allow and deny.

General:
~~~~~~~~

+------------------------+------------+
|       Permission       | Bit Offset |
+========================+============+
| Create Instant Invite  |      0     |
+------------------------+------------+
| Kick Members           |      1     |
+------------------------+------------+
| Ban Members            |      2     |
+------------------------+------------+
| Manage Roles           |      3     |
+------------------------+------------+
| Manage Permissions     |      3     |
+------------------------+------------+
| Manage Channels        |      4     |
+------------------------+------------+
| Manage Channel         |      4     |
+------------------------+------------+
| Manage Server          |      5     |
+------------------------+------------+

Chat:
~~~~~

+------------------------+------------+
|       Permission       | Bit Offset |
+========================+============+
| Read Messages          |     10     |
+------------------------+------------+
| Send Messages          |     11     |
+------------------------+------------+
| Send TTS Messages      |     12     |
+------------------------+------------+
| Manage Messages        |     13     |
+------------------------+------------+
| Embed Links            |     14     |
+------------------------+------------+
| Attach Files           |     15     |
+------------------------+------------+
| Read Message History   |     16     |
+------------------------+------------+
| Mention Everyone       |     17     |
+------------------------+------------+

Voice:
~~~~~~

+------------------------+------------+
|       Permission       | Bit Offset |
+========================+============+
| Voice Connect          |     20     |
+------------------------+------------+
| Voice Speak            |     21     |
+------------------------+------------+
| Voice Mute Members     |     22     |
+------------------------+------------+
| Voice Deafen Members   |     23     |
+------------------------+------------+
| Voice Move Members     |     24     |
+------------------------+------------+
| Voice Use VAD          |     25     |
+------------------------+------------+