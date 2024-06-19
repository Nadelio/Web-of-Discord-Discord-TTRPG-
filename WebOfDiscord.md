# Web of Discord Base Ruleset and Information

### Rules:
#
- Choose a starting class for your character
- Every `5 + <level>` interactions will level up your character, you can choose 1 stat to add +1 point to
- On a level up, you can also choose a skill, every 5 levels you can choose a mastery skill
    - A skill gives you the ability to have special interactions with interactables
        - A mastery skill will reduce one stat but add +2 points to the stat that corresponds to the skill, it will also give you a special interaction with interactables
- On a turn, you can only move the number of squares that your Move stat is, you can interact with any number of interactables, as long as you are within a 1 tile distance of them (this includes diagonally), and/or you can use any number of items.
- You have to log the path you traveled as you complete your turn, then a "Game Master" will update the board accordingly
- Players can talk freely with one another
- Players count as interactables, you can trade items, fight, heal, and more, players decide!
- Homebrew is allowed, add more items, more interactables, more tile types, etc.! As long as you document them properly and make sure the players understand how to interact with these homebrew changes
- "Game Masters" have final say on player interactions (i.e. don't let players do anything each other if one is really against that idea)
- "Game Masters" control the events of the game (so like NPC actions, random events, PvE interactions, etc.)
- "Game Masters" control the map, what items players get, how environment interactions play out, etc.
- This is like DnD, there really isn't an "end point" unless the GM (Game Master) decides there is.
- You can have a story and goals, but in the end, the GM choose what happens
- This is basically DnD but in Discord lol
- Follow the standardized formatting*
    - it isn't strictly necessary, you don't have to, just make sure people understand your formatting
- GM can choose whatever dice they see fit for actions, and in most cases higher number = better
- You will update your character message after every turn, unless nothing changes (you can pass your turn)
- The GM will keep track of the turns, only updating the turn after every NPC and Player has taken that turn 
- The GM will need two maps, a regular game map, and an interaction map, both will need keys, you can use any single ascii character to define a tile (you can use multiple characters but I suggest showing some way to differentiate tiles from one another, my personal suggestion is brackets `[<tile_code>]`)
- GMs will also need an event list, loot table, a set of dice (or a Discord bot, I suggest Dice Madien), and various NPC/Enemy sheets.
- Players can equip as many items as they want (or follow the GMs discretion) 
- Maps can be as big as the GM wants, but:
    - Maps have to be able to be navigated by players
    - Maps have to at least be 5x5

### How stats are used:
#
Level:
- The level of the player

Health:
- How much damage a player can take before being killed
- When under 50% health, player has 1/2 their movement stat
- When under 10% health, players have only 1 movement and can no longer interact with anything but players, they also cannot use items. 
- When killed, a player can loot items from the dead player

Movement:
- How many tiles a player can move in a turn, players can move in any of the surrounding 8 tiles.

Luck:
- Add luck to rolls
- Do not apply luck to rolls with `Disadvantage` (`Disadvantage` behaves the same way as in DnD)
- Add 1.5x luck to rolls with `Advantage` (see Advantage for more information on how `Advantage` works)

Defense:
- This is your AC (like in DnD)

Unarmed Attack:
- This is your base attack, whenever you do not have a weapon, use this stat to calculate damage
- When armed, add 1/4 this stat to your damage *at the end of calculations*

Class/Species:
- This helps easily define what players base stats are supposed to be
- See Classes/Species for base player stats

Homebrew Stats:
- This just contains all the homebrew stats

### Misc. Info:
#
- Advantage
    - Advantage applies to attacks, interactions with tiles, NPCs, and Enemies
    - Advantage adds `1.5 * <player_level>` to *attack damage* (not attack rolls) and non-PvP/PvE interaction rolls
    - Advantage adds `1/2 * <player_level>` to *attack rolls*
- Classes/Species
    - Human `{10, 3, 2, 1, 3}`
    - Boxer `{9, 3, 2, 3, 5}`
    - Gambler `{8, 3, 5, 1, 1}`
    - Doctor `{9, 3, 2, 1, 3}` (Doctors have advantage when healing another player/NPC or themselves)
    - Runner `{8, 7, 2, 1, 3}`
    - Boxer's Punching Bag `{10, 3, 2, 5, 3}`
- Skills
    - Uhhh, idk, come up with your own ig? (this will change in the future if I get good or if people suggest things I think would be good)

### Examples of Gameboards:
#
Gameboard:
```
WWWWWW
W1XXXW
WXXXXW
WIWIWW
WWWWWW
```
Key:
```
W - wall
1 - player 1
X - open space
I - interactable
D - door
```

### Example of Interactable Map:
#
Interactable Map:
```
XXXXXX
XPXXXX
XXXXXX
XBXCXX
XXXXXX
```
Key:
```
X - non-interactable
P - player
B - bed
C - container
```

### Basic Player Data Sheet:
#
User: `<username>`
Stats: `Level: <level>, Health: <health>, Move: <move>, Luck: <luck>, Defense: <defense>, Unarmed Attack: <unarmed_attack>, Class/Species: <class/species>, Homebrew Stats: {...}`\
Items: `{...}`\
Equiped Items: `{...}`\
Movement Log: `{...}`

### Movement Log Documentation:
#
Movement Log Example:
```
{
Current Tile: X1Y1
Movement: X1Y1-X3Y1, ...
Interaction: X4Y1, Traded <item> with <player>
Movement: X3Y1-X3Y2
Equiped: <item>, <item>, ...
Leveled Up: <Stat> <+/-> <number>, Gained <mastery_skill/skill>, ...
End Turn: <current_tile_player_is_on>
}
```
1. Start the log with your current tile in the format: `X<number>Y<number>`
2. Start your first movement/interaction series
    - A2. Movements are in the same format as current tile (`X<number>Y<number>`), you can individual document every change in position, or for things like straight away's or unbranching paths, you can just do `X<number>Y<number>-X<number>Y<number>`
    - 2B. Interactions start with the interacted tile, in the tile position format used in previous log rules, followed by the interaction and the result of interaction (of which is discussed with the GM)
    - C2. Equiping items starts with `Equiped: `, followed by the items you equip
    - 2D. Leveling up starts with `Leveled Up: `, followed by the changes to your stats, and what skills/mastery skills you chose
3. To end your log, you will finish with `End Turn: `, then the tile you are currently on
4. *You don't need the curly braces before/after your log, I just use it for visual flare*

# 
*Just some rule reading knowledge, anything with `<>` surrounding it is either a player stat, or able to be replaced with a number/word/skill/coordinate as the word inside the `<>` would suggest*
