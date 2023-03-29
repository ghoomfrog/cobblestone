---
title: Cobblestone
header-includes:
- \usepackage{titling}
- \usepackage{fontspec}
- \usepackage[margin=1in]{geometry}
- \usepackage{sectsty}
- \usepackage[splitrule]{footmisc}
- \usepackage{fancyhdr}
- \setlength{\droptitle}{-0.5in}
- \setmainfont{IM Fell DW Pica}
- \interfootnotelinepenalty=10000
- \pretitle{\begin{center}\fontsize{86.75}{0}\fontspec{IM Fell English SC}\selectfont}
- \posttitle{\par\end{center}}
- \sectionfont{\fontsize{28}{1.5\baselineskip}\fontspec{IM Fell DW Pica SC}\selectfont}
- \subsectionfont{\fontsize{24}{1.5\baselineskip}\fontspec{IM Fell DW Pica SC}\selectfont}
- \subsubsectionfont{\fontsize{20}{1.5\baselineskip}\fontspec{IM Fell DW Pica SC}\selectfont}
- \AtBeginDocument{\fontsize{18}{1.5\baselineskip}\selectfont}
- \renewcommand{\footnotesize}{\fontsize{15}{0}\selectfont}
- \pagestyle{fancy}
- \fancyhf{}
- \fancyfoot[C]{\fontsize{15}{0}\selectfont\thepage}
- \renewcommand{\headrulewidth}{0pt}
- \renewcommand{\footrulewidth}{0pt}
- \fancypagestyle{plain}{\pagestyle{fancy}}
---

# Overview

Cobblestone is a turn-based survival tabletop RPG where players alternate between roleplaying and narrating in a custom fantasy setting. It's designed around heavy character customization, and systemization of many aspects of roleplay.
&nbsp;
The game starter (GS) narrates the setting. After that, the first player in every other consecutive pair acts, and the second narrates, and if the number of players is even, the GS always gets two turns, one for acting and one for narration (or vice versa).[^ensure]

[^ensure]: This ensures that all players both act and narrate throughout the game in an even-numbered party.

# Traits

Things in the world have numerical traits that control aspects of gameplay. They are measured in trait points (TP). The higher a trait is, the higher the advantage. Every character has a total of 540 TP to distribute between their traits. The value by which a trait is defined, is both its initial value and peak. The peak is a dynamic maximum that can be increased by levelling up (explained later).
&nbsp;
Characters don't benefit from a magic trait if it's not positive.
&nbsp;
These are the traits that every character has:

Trait|Typical Peak|Description
-------------|-----------|------------------------
Strength      |20|Life, physical strength in kilograms, and maximum damage; at 0 STR the character undergoes the Dead condition.
Terramobility |20|Maximum speed on land, measured in feet per round[^round]
Muromobility  |10|Maximum climbing speed
Aquamobility  |10|Maximum swimming speed
Aeromobility  |0 |Maximum flight speed
Dexterity     |25|Physical skill
Energy        |30|Actions require and consume 1 E except food consumption which restores 1 E per round. At 0 E, the character undergoes the Starving condition in the next round.
Sleep         |50|1 sleep is drained every round, and restored by sleeping. At 0 sleep, the character undergoes the Exhausted condition in the next round.
Venomosity    |0 |The ability to inflict the Poisoned condition
Immunity      |0 |Poison resistance
Breath        |5 |1 breath is regenerated when breathing, and consumed otherwise. At 0 breath, the character undergoes the Suffocating condition in the next round.
Mana          |0 |Magic requires and consumes mana equal to the action criterion (explained later).
Antimagic     |0 |The anti-trait[^anti-trait] of magic: the ability to nullify external magical effects on oneself; characters can choose to neglect this trait when targetted in trait actions.
Warmth[^T]    |0 |Cold resistance; at 0 warmth, in cold places (below 50T), the character undergoes the Freezing condition in the next round.
Chill         |0 |Heat resistance; at 0 chill, in hot places (above 50T), the character undergoes the Sizzling condition in the next round.
Wit           |50|Intellect
Knowledge     |20|Situational knowledge
Eyesight      |50|Eyesight level and the radius of vision in decameters; also the anti-trait of invisibility
Darkvision[^L]|50|The ability to see in full brightness in and below a certain luminence
Invisibility  |0 |The anti-trait of eyesight
Hearing[^A]   |50|The ability to perfectly hear a certain sound amplitude and below; also the anti-trait of stealth
Stealth       |0 |The anti-trait of hearing
Charisma      |20|The ability to inflict the Charmed condition
Willpower     |20|The anti-trait of charisma and psychicness; trying to escape a charm depends on this trait.
Intimidation  |0 |The ability to inflict the Intimidated condition
Courage       |20|The anti-trait of intimidation; trying to overcome an intimidation depends on this trait.
Religion      |40|Praying depends on this trait.
Morphability  |0 |Morphing depends on this trait.
Transcendence |0 |Transtribution (explained later) depend on this trait.
Alchemy       |0 |Alchemy magic: the maximum mass of objects (in kilograms) that the character can transform
Psychicness   |0 |Clairvoyance and the ability to mind-read
Telekinesis   |0 |Either telekinesis range (in feet) and telekinesis strength (in kilograms) when moving things, or maximum damage when throwing things, in which case strength is the anti-trait instead of antimagic
Telemancy     |0 |Teleportation depends on this trait.
Luck          |50|A percentage that affects the success of trait actions (explained later)

[^round]: two cycles of turns from the GS
[^anti-trait]: a trait representing an aspect of the world that counter a trait
[^T]: Warmth and chill are measured in T. 50T is the optimal temperature for life.
[^L]: Luminance is measured in L. 50L is the brightness of a typical sunny day.
[^A]: Sound amplitude is measured in A.

# Fall Damage

Fall damage is taken as the falling distance (in feet) minus the faller's strength if the result is positive.

# Trait Bonuses

A character's trait bonuses are added to their respective traits.[^active-equipement] Characters can have as many as desired,[^multiple] but they can only start with 100 distributable bTP.
&nbsp;
Trait bonuses can be swapped[^swap] in and out, and are consumed before their respective traits.

[^active-equipement]: like from active equipement
[^multiple]: and can have multiple bonuses per trait
[^swap]: like dropping a weapon in exchange for another

# Trait Penalties

Trait penalties are just like trait bonuses except they are subtracted from their respective traits.
&nbsp;
For example, a sticky floor might pose an agility penalty of 10 to non-flying characters. Another example is that anything carried poses a strength penalty equal to its weight (in kilograms).

# Trait Actions

Trait actions are ones that depend on a trait. They can be done by and directed at player characters and NPCs alike. Actors (including NPCs) can only make one trait action per turn.
&nbsp;
Trait actions only succeed if the following inequality is met: *t* - *c* + *l* + *r* > *T* + 100, where:

- *t* is the trait (with bonuses and penalties),
- *c* is the action criterion[^criterion] (0 if not needed),
- *l* is the actor's luck,
- *r* is a 100-sided die roll,
- *T* is the anti-trait (with bonuses and penalties; 0 if the trait isn't countered).

&nbsp;
It's up to the previous narrator to determine the variables that don't belong to player characters if they haven't been determined yet.

[^criterion]: For example, 26 is the action criterion when trying to inflict 26 damage.

# Experience

Characters start at level 0. Trait actions grant their actors XP equal to *c*. Characters can use up 1000 XP to level themselves or someone else up: increasing the peak of one of the target's traits by 1 TP.

# Transtribution

Transtribution is the magical act of modifying traits in things in the world, except the user's mana. For example, one can transtribute mana to warm up the room by 20T, to heal themselves by 40 STR, to cast a 20L light, or to create a creature with 25 STR initially.
&nbsp;
The latter example is how one "summons" a creature: by slowly transtributing to its traits, one transtribution per round. The creature must still be charmed to obey orders though.

# Praying

Praying is similar to transtribution except that the user can use different traits of different things as mana: this is called sacrifice. Sacrificing from traits doesn't decrease their peaks.

# Morphing

Polymorphs are characters that have other forms that they can morph into. Forms must be defined the same way as a character, and can level up alongside their polymorphs.

# Teleportation

Teleporting something works by tagging it in one round, starting with a teleportation range of *c* (feet), then optionally increasing that range by the *c* of every other round, before finally completing the teleportation in one final round.
&nbsp;
The user can't do anything else in this process until they cancel the teleportation which takes up their round.

# Conditions

Condition|Description
-|----
Dead       |Can't act while strength is not positive
Suffocating|Loses 1 STR every round while breath is not positive
Starving   |Loses 1 STR every round while energy is not positive
Exhausted  |Loses 1 STR every round while sleep is not positive
Poisoned   |Loses 1 STR every round until cured
Intimidated|Can't disadvantage the intimidator
Charmed    |Hypnotized by the charmer but can try to escape the charm					
Freezing   |Loses 1 STR every round while warmth is not positive
Sizzling   |Loses 1 STR every round while chill is not positive

# Credits

### Dungeons & Dragons — Inspiration

### One Shot Questers — The Most D&D Interest

### Ghoom — Game Design & Documentation

### Igino Marini — Fonts Used in This Document

- IM Fell English (on the title)
- IM Fell DW Pica SC (on headings)
- IM Fell DW Pica (everywhere else)