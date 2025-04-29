XML EXAMPLE
================
SERAFIN LITO B.
----------------

What is this XML example about?
-------------------------------

This XML example showcases a structured way to represent **Pokémon characters**  
in a **machine-readable** XML format.

Each ``<pokemon>`` element includes rich metadata about a specific Pokémon, such as:

- ✨ **Name and Species** — The Pokémon's name and species classification.
- 🔥 **Type** — One or two elemental types (e.g., Fire, Water, Electric).
- 🧠 **Category** — Describes the Pokémon's general behavior or role.
- 🎯 **Difficulty Level** — How hard it is to train or evolve.
- 📅 **First Appearance** — The game or generation in which the Pokémon debuted.
- 🗣️ **Voice Line** — A catchphrase or Pokédex entry.
- 📖 **Lore** — A short backstory or behavior description.
- ⚔️ **Moves** — Key abilities or attacks used in battle.

Designed to be:

- **Developer-friendly** — Ideal for use in apps, wikis, or databases.
- **Organized** — Easily updatable and searchable.
- **Expandable** — Add new Pokémon, types, or moves seamlessly.
- **Reusable** — Perfect for game guides, training apps, or encyclopedias.

> 🎮 Great for game developers, XML learners, or database designers  
> who want a fun yet structured data format!

.. image:: https://assets.pokemon.com/assets/cms2/img/pokedex/full/025.png
   :alt: Pikachu standing, smiling, and sparking with electricity
   :width: 300px
   :align: center

   *Pikachu - The iconic Electric-type Pokémon*

.. code-block:: xml

    <?xml version="1.0" encoding="UTF-8"?>
    <pokedex>
        <pokemon>
            <name>Pikachu</name>
            <species>Mouse Pokémon</species>
            <type>Electric</type>
            <category>Starter</category>
            <difficulty>Easy</difficulty>
            <first_appearance>Pokémon Red/Blue (1996)</first_appearance>
            <voice_line>"Pika Pika!"</voice_line>
            <lore>Pikachu stores electricity in its cheeks and releases it in thunderous bursts to defend itself.</lore>
            <moves>
                <move power="electric" action="shock">Thunder Shock</move>
                <move power="electric" action="zap">Electro Ball</move>
                <move power="electric" action="storm">Thunderbolt</move>
                <move power="physical" action="tackle">Quick Attack</move>
            </moves>
        </pokemon>

        <pokemon>
            <name>Charizard</name>
            <species>Flame Pokémon</species>
            <type>Fire/Flying</type>
            <category>Final Evolution</category>
            <difficulty>Moderate</difficulty>
            <first_appearance>Pokémon Red/Blue (1996)</first_appearance>
            <voice_line>"Charizard roars and breathes intense flames!"</voice_line>
            <lore>Charizard soars through the sky in search of powerful opponents, its breath hot enough to melt boulders.</lore>
            <moves>
                <move power="fire" action="blast">Flamethrower</move>
                <move power="dragon" action="rage">Dragon Claw</move>
                <move power="flying" action="charge">Fly</move>
                <move power="fire" action="eruption">Heat Wave</move>
            </moves>
        </pokemon>
    </pokedex>

What's going on here:
------------------------

- ``<pokedex>`` is the **root element** that wraps all Pokémon entries.
- Each ``<pokemon>`` entry stores name, species, types, difficulty, and backstory.
- ``<moves>`` is a nested container for the Pokémon's key attacks.
- ``<move>`` tags contain **attributes** like ``power`` and ``action`` to describe functionality.

