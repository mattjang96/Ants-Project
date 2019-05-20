# Ants-Project

![Ants](https://s3-us-west-1.amazonaws.com/shuttr-dev-seeds/ants.png)

In this project, I created a tower defense game called Ants Vs. SomeBees (pun intended). As the ant queen, I populate my colony with the bravest ants I can muster. The ants must protect the queen from the evil bees that invade the territory. Irritate the bees enough by throwing leaves at them, and they will be vanquished. Fail to pester the airborne intruders adequately, and the queen will succumb to the bees' wrath. This game is inspired by PopCap Games' Plants Vs. Zombies.

This project combines functional and object-oriented programming paradigms. The project also involves understanding, extending, and testing a large program.

## Core Concepts
A game of Ants Vs. SomeBees consists of a series of turns. In each turn, new bees may enter the ant colony. Then, new ants are placed. Finally, all insects (ants, then bees) take individual actions: bees sting ants, and ants throw leaves at bees. The game ends either when a bee reaches the ant queen (you lose), or the entire bee flotilla has been vanquished (you win).

**The Colony** The colony consists of several places that are chained together. The `exit` of each `Place` leads to another Place.

**Placing Ants** There are two constraints that limit ant production. Placing an ant uses up some amount of the colony's food, a different amount for each type of ant. Also, only one ant can occupy each Place.

**Bees** When it is time to act, a bee either moves to the exit of its current Place if no ant blocks its path, or stings an ant that blocks its path.

**Ants** Each type of ant takes a different action and requires a different amount of food to place. The two most basic ant types are the HarvesterAnt, which adds one food to the colony during each turn, and the ThrowerAnt, which throws a leaf at a bee each turn.

## The Code
Most concepts in the game have a corresponding class that encapsulates the logic for that concept. For instance, a Place in the colony holds insects and connects to other places. A `Bee` stings ants and advances through exits.

The game can be run in two modes: as a text-based game or using a graphical user interface (GUI). The game logic is the same in either case, but the GUI enforces a turn time limit that makes playing the game more exciting. The text-based interface is provided for debugging and development.

The files are separated according to these two modes. ants.py knows nothing of graphics or turn time limits.

To start a text-based game, run:
```python
python3 ants.py
```

To start a graphical game, run:
```python
python3 ants_gui.py
```

