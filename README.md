# NodeBB RPG Dice Roller Plugin

The goal of this plugin is to create a dice roller suitable for tabletop rpgs to be played in a Play By Post setup.

## Goals

The main goals of this project are as follows:
  1. Roll dice that follow similar characteristics of tabletop gaming dice
  2. Use a bracket syntax (described below)
  3. Write tests for the code using `mocha` or another similar tool
  4. Allow for several different mechanics:
    - Re-roll failed rolls
  5. Automatically detect tampering and mark it as such

## Syntax

The goal is to get a syntax like the following:

```
[dice name='<Name of Roll>']XdY+/-Z, reroll=A,B[/dice]
```

Where:
  - **Name of Roll** is a name, such as "Attack", or "Damage", or "Perception"
  - **X** Is the number of dice to roll
  - **Y** Is the number of sides on the die to roll
  - **+/-** Is the sign of the modifier
  - **Z** Is a modifier to the roll
  - **reroll=A,B** Is a command to automatically reroll numbers A or B once

Other syntax may be supported in the future.

The output of the plugin would be in a tabular format, including the rolls themselves to help GM/DMs see what was rolled.
