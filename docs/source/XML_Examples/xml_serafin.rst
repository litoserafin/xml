XML EXAMPLE
================
SERAFIN LITO B.
----------------


.. figure:: https://storage.googleapis.com/a1aa/image/httyd-toothless.jpg
   :alt: Toothless the Night Fury dragon flying with Hiccup
   :width: 500px
   :align: center


   *Toothless - The Night Fury, flying with Hiccup in the skies of Berk*

.. code-block:: xml

    <?xml version="1.0" encoding="UTF-8"?>
    <dragons>
        <dragon>
            <name>Toothless</name>
            <species>Night Fury</species>
            <rider>Hiccup</rider>
            <class>Strike</class>
            <affiliation>Berk Dragon Riders</affiliation>
            <release_date>2010-03-26</release_date>
            <personality>Loyal, Intelligent, Playful</personality>
            <abilities>
                <ability type="plasma" power="high">Plasma Blast</ability>
                <ability type="stealth" power="medium">Camouflage</ability>
                <ability type="flight" power="high">High-Speed Flight</ability>
            </abilities>
        </dragon>

        <dragon>
            <name>Stormfly</name>
            <species>Deadly Nadder</species>
            <rider>Astrid</rider>
            <class>Tracker</class>
            <affiliation>Berk Dragon Riders</affiliation>
            <release_date>2010-03-26</release_date>
            <personality>Agile, Loyal, Fierce</personality>
            <abilities>
                <ability type="spikes" power="medium">Tail Spike Launch</ability>
                <ability type="fire" power="medium">Magnesium Flames</ability>
                <ability type="flight" power="high">Aerial Acrobatics</ability>
            </abilities>
        </dragon>
    </dragons>

What's going on here:
------------------------

- ``<dragons>`` is the **root element**, representing all trained dragons.
- Each ``<dragon

What's going on here:
------------------------

- ``<league>`` is the **root element** that holds all champions.
- Each ``<champion>`` element includes key details: name, title, role, difficulty, release date, team, and lore.
- ``<abilities>`` contains a list of ``<ability>`` elements.
- Each ``<ability>`` has **attributes** like ``power`` and ``action`` that describe its mechanics.


What's going on here:
------------------------

- ``<league>`` is the **root element** containing all champions.
- Each ``<champion>`` has **child elements** such as ``<name>``, ``<title>``, ``<role>``, ``<difficulty>``, ``<release_date>``, ``<team>``, ``<team_lore>``, ``<lore>``, and ``<abilities>``.
- ``<abilities>`` contains multiple ``<ability>`` elements, each with **attributes** like ``power`` and ``action`` to describe their special skills.
- **Attributes** are used inside ``<ability>`` (e.g., ``power="magic"``, ``action="orb"``) to provide extra information about the ability.

