XML EXAMPLE
================
SERAFIN LITO B.
----------------

.. figure:: https://static.wikia.nocookie.net/howtotrainyourdragon/images/5/5e/Light_Fury_RotR.png
   :alt: Light Fury dragon flying gracefully in the sky
   :width: 450px
   :align: center

   Light Fury - A rare and beautiful dragon with dazzling speed and plasma blasts.

.. code-block:: xml

    <?xml version="1.0" encoding="UTF-8"?>
    <dragons>
        <dragon>
            <name>Light Fury</name>
            <species>Light Fury</species>
            <rider>None</rider>
            <class>Strike</class>
            <affiliation>Hidden World</affiliation>
            <release_date>2019-02-22</release_date>
            <personality>Curious, Brave, Playful</personality>
            <abilities>
                <ability type="plasma" power="high">Plasma Blast</ability>
                <ability type="stealth" power="high">Invisibility Cloak</ability>
                <ability type="flight" power="very_high">Supersonic Flight</ability>
            </abilities>
        </dragon>

        <dragon>
            <name>Hookfang</name>
            <species>Monstrous Nightmare</species>
            <rider>Snotlout</rider>
            <class>Stoker</class>
            <affiliation>Berk Dragon Riders</affiliation>
            <release_date>2010-03-26</release_date>
            <personality>Fiery, Aggressive, Loyal</personality>
            <abilities>
                <ability type="fire" power="very_high">Self-Ignite</ability>
                <ability type="flight" power="medium">Strong Gliding</ability>
            </abilities>
        </dragon>
    </dragons>

What's going on here:
------------------------

- ``<dragons>`` is the **root element** that groups all dragon entries.
- Each ``<dragon>`` contains info like ``<name>``, ``<species>``, ``<rider>``, ``<class>``, ``<affiliation>``, and ``<release_date>``.
- ``<abilities>`` holds special moves or natural powers, with attributes like ``type`` and ``power``.
- This XML structure would be perfect for a "Dragon Database" or a "Training Manual App".



