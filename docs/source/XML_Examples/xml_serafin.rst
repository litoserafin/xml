XML EXAMPLE
================

.. code-block:: xml

   <?xml version="1.0" encoding="UTF-8"?>
<league>
    <champion>
        <name>Ahri</name>
        <title>The Nine-Tailed Fox</title>
        <role>Mage</role>
        <difficulty>Moderate</difficulty>
        <release_date>2011-12-14</release_date>
        <team>Vastaya Clan</team>
        <team_lore>"Don't you trust me?"</team_lore>
        <lore>Ahri is a fox-like vastaya who can manipulate her prey’s emotions and consume their essence — for amusement or survival.</lore>
        <abilities>
            <ability power="magic" action="orb">Orb of Deception</ability>
            <ability power="charm" action="taunt">Charm</ability>
            <ability power="magic" action="burst">Fox-Fire</ability>
            <ability power="dash" action="move">Spirit Rush</ability>
        </abilities>
    </champion>

    <champion>
        <name>Yasuo</name>
        <title>The Unforgiven</title>
        <role>Fighter</role>
        <difficulty>High</difficulty>
        <release_date>2013-12-13</release_date>
        <team>Ionian Blades</team>
        <team_lore>"Death is like the wind — always by my side."</team_lore>
        <lore>An Ionian swordsman who lives with the burden of having to kill his own brother to survive, seeking redemption.</lore>
        <abilities>
            <ability power="wind" action="knockup">Steel Tempest</ability>
            <ability power="windwall" action="block">Wind Wall</ability>
            <ability power="dash" action="move">Sweeping Blade</ability>
            <ability power="wind" action="strike">Last Breath</ability>
        </abilities>
    </champion>
</league>


What's going on here:
------------------------

- ``<bookstore>`` is the **root element**.
- Each ``<book>`` has **child elements**: ``<title>``, ``<author>``, ``<year>``, and ``<price>``.
- **Attributes** are used inside ``<book>`` (e.g., ``category="fiction"``) and inside ``<title>`` (e.g., ``lang="en"``).
