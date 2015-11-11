|stub| General
==============

Get Server Regions
------------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/voice/regions

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