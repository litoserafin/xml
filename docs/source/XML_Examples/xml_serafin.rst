XML EXAMPLE
================

DEVELOPERS:
----------------
- SERAFIN LITO B.

What is this XML example about?
-------------------------------

This XML example demonstrates a structured way to represent **League of Legends** champions  
in a **machine-readable** format using XML.  

Each ``<champion>`` element organizes rich metadata that describes key aspects of a champion, including:

- ✨ **Name and Title** — The official name and heroic or legendary title.
- 🛡️ **Role** — The champion’s typical battlefield role (e.g., Mage, Fighter, Tank).
- 🏹 **Team** — The faction, clan, or group the champion belongs to in the game lore.
- 🎯 **Difficulty Level** — How challenging the champion is to master.
- 📅 **Release Date** — The date when the champion was introduced into the game.
- 🗣️ **Voice Line** — A signature quote that captures their personality.
- 📖 **Lore** — A short backstory highlighting their motivation, journey, and values.
- ⚔️ **Abilities** — Special moves, magic, or skills that define the champion’s gameplay style.

The structure is designed to be:

- **Developer-friendly** — Easy to parse by applications, tools, or websites.
- **Organized** — Makes content management and updates more systematic.
- **Expandable** — New champions, teams, or abilities can easily be added.
- **Reusable** — Ideal for mobile apps, databases, or web companion guides.

> 🚀 This format is perfect for developers, database architects, or game designers  
> who need a flexible and efficient way to manage, share, or display champion data!



.. figure:: https://storage.googleapis.com/a1aa/image/725be2bf-54f1-4a14-73b8-8ad106ba34f3.jpg
   :alt: Viktor champion image with blue laser sword and dark background
   :width: 500px
   :align: center

   *Viktor - A futuristic champion wielding high-tech powers*

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

- ``<league>`` is the **root element** that holds all champions.
- Each ``<champion>`` element includes key details: name, title, role, difficulty, release date, team, and lore.
- ``<abilities>`` contains a list of ``<ability>`` elements.
- Each ``<ability>`` has **attributes** like ``power`` and ``action`` that describe its mechanics.





