XML EXAMPLE
================
BAYLE MARY JOY
----------------

What is this XML example about?
-------------------------------

This XML example demonstrates a structured way to represent **Super Mario** characters  
in a **machine-readable** XML format.

Each ``<character>`` element holds key details about a specific character in the Super Mario universe, such as:

- ✨ **Name and Alias** — The character's name and any known aliases.
- 🌟 **Role** — The character's primary role or function (e.g., Hero, Villain).
- 🎮 **Abilities** — Powers or skills the character uses in their adventures.
- 🏆 **First Appearance** — The game where the character first appeared.
- 🗣️ **Catchphrase** — A memorable line or catchphrase that the character is known for.
- 📖 **Lore** — A short backstory or origin story for the character.
- ⚔️ **Actions** — Key actions or abilities used in the game.

Designed to be:

- **Developer-friendly** — Ideal for apps, game databases, or fan sites.
- **Organized** — Easy to update, manage, and retrieve character details.
- **Expandable** — Additional characters, powers, and moves can be added effortlessly.
- **Reusable** — Perfect for creating guides, fan projects, or game documentation.

> 🎮 Perfect for game developers, game designers, or anyone building fan content  
> for the Super Mario series!

.. image:: https://www.mariowiki.com/images/0/0c/MarioArtwork.png
   :alt: Mario jumping with his iconic red hat and mustache
   :width: 300px
   :align: center

   *Mario - The famous plumber and hero of the Mushroom Kingdom*

.. code-block:: xml

    <?xml version="1.0" encoding="UTF-8"?>
    <super_mario>
        <character>
            <name>Mario</name>
            <alias>Super Mario</alias>
            <role>Hero</role>
            <abilities>
                <ability power="jump" action="higher">Super Jump</ability>
                <ability power="fire" action="attack">Fireball</ability>
                <ability power="speed" action="move">Super Speed</ability>
                <ability power="strength" action="smash">Ground Pound</ability>
            </abilities>
            <first_appearance>Donkey Kong (1981)</first_appearance>
            <catchphrase>"It's-a me, Mario!"</catchphrase>
            <lore>Mario is a plumber who ventures through the Mushroom Kingdom to rescue Princess Peach from Bowser's clutches.</lore>
        </character>

        <character>
            <name>Princess Peach</name>
            <alias>Princess Toadstool</alias>
            <role>Heroine</role>
            <abilities>
                <ability power="float" action="hover">Floating Jump</ability>
                <ability power="defend" action="shield">Royal Shield</ability>
                <ability power="healing" action="restore">Healing Heart</ability>
            </abilities>
            <first_appearance>Super Mario Bros. (1985)</first_appearance>
            <catchphrase>"Thank you Mario, but our princess is in another castle!"</catchphrase>
            <lore>Princess Peach is the ruler of the Mushroom Kingdom, often kidnapped by Bowser, but always determined to fight for her kingdom.</lore>
        </character>

        <character>
            <name>Bowser</name>
            <alias>King of the Koopas</alias>
            <role>Villain</role>
            <abilities>
                <ability power="fire" action="breath">Fire Breath</ability>
                <ability power="strength" action="crush">Claw Crush</ability>
                <ability power="summon" action="minions">Summon Koopa Troopas</ability>
            </abilities>
            <first_appearance>Super Mario Bros. (1985)</first_appearance>
            <catchphrase>"Gwahahaha!"</catchphrase>
            <lore>Bowser is the evil king of the Koopa race, constantly trying to take over the Mushroom Kingdom and defeat Mario.</lore>
        </character>
    </super_mario>

What's going on here:
------------------------

- ``<super_mario>`` is the **root element** that wraps all character data.
- Each ``<character>`` stores information such as name, role, abilities, and lore.
- ``<abilities>`` contains a list of actions like jumping, fire breathing, and crushing.
- Each ``<ability>`` has **attributes** like ``power`` and ``action`` describing the action's effects.

