# Set

```
 .----------------.  .----------------.  .----------------. 
| .--------------. || .--------------. || .--------------. |
| |    _______   | || |  _________   | || |  _________   | |
| |   /  ___  |  | || | |_   ___  |  | || | |  _   _  |  | |
| |  |  (__ \_|  | || |   | |_  \_|  | || | |_/ | | \_|  | |
| |   '.___`-.   | || |   |  _|  _   | || |     | |      | |
| |  |`\____) |  | || |  _| |___/ |  | || |    _| |_     | |
| |  |_______.'  | || | |_________|  | || |   |_____|    | |
| |              | || |              | || |              | |
| '--------------' || '--------------' || '--------------' |
 '----------------'  '----------------'  '----------------' 
   ======================================================
   |	   The Family Game of Visual Perception		|
   |							|
   |		    ported by ibid11962			|
   ======================================================
```

This is a port of the popular real-time card game "Set" for the ti83+/ti84+ graphing calculators. It was programmed in Axe Parser and compiled to z80 assembly. It features a full AI, "perfect" greyscale (achieved my flashing pixels in sync with the screen's refresh rate), and some configurable diffulty settings.

This game is best played on the ti83+SE/ti84+/ti84+SE calculators.

It can also be played on the ti83+ (and probably also the nspire based emulator), but the greyscale won't look as nice.

If you do not have a calculator, there are several PC, javascript, and android based calculator emulators available that should run this fine. Wabbitemu, jsTIfied, and TilEm are all good options.

This game is not compatible with the ti83, ti84+CSE, or ti84+CE calculators.

A lot of this code was written in 2012, then sat untouched for five years before being picked up again and finished in 2017.

[It was featured on ticalc.org in May 2019](https://www.ticalc.org/archives/news/articles/14/149/149262.html)

![animated screenshot](/Screenshot.gif)


# Installation

Send SET.8xp to your calculator using TI-Connect or TiLP.

The program has been compiled to MirageOS and thus will need a compatible shell such as [MirageOS](https://www.ticalc.org/archives/files/fileinfo/139/13949.html), DoorsCS, or Noshell to run.


# Rules

(Mostly copied from Wikipedia:)

A set consists of three cards satisfying all of these conditions:

- They all have the same number or have three different numbers.
- They all have the same symbol or have three different symbols.
- They all have the same shading or have three different shadings.
- They all have the same color or have three different colors.

The rules of Set are summarized by: If you can sort a group of three cards into "two of ___ and one of ___ ", then it is not a set.

For example, these three cards form a set:

- One black striped diamond
- Two black solid diamonds
- Three black open diamonds

Given any two cards from the deck, there is one and only one other card that forms a set with them.

Twelve cards are dealt out onto the table. When you see a set among the twelve cards, you call "Set" `[Graph]`, take the three cards, and the dealer lays three more cards on the table. (To call out "set" and not pick one up a correct set results in a penalty.) 

If you wait too long to call "set" then the calculator will "find" a set first and get a point. This time is defaulted to about 20 seconds, but you can adjust it in the settings for an easier/harder game.

It is possible that there is no set among the twelve cards; in this case, the dealer deals out three more cards to make fifteen dealt cards, or eighteen or more, as necessary. This process of dealing by threes and finding sets continues until the deck is exhausted and there are no more sets on the table. At this point, whoever has collected the most sets wins.

# Controls

Arrow keys - move cursor around
Graph - Call a set
Graph/2nd/Enter - Select cards (after calling a set)
2nd/Enter - Deal new cards (after the calculator calls a set)
Trace - Enter/Exit the settings menu
Clear - Exit

# Settings

You can access the settings menu at any time by pressing `[Trace]`. 

Difficulty - The amount of time the calculator will take to find a set. This is defaulted to "4" which is around 20 seconds. 

Penalty - Use this option to turn on/off the penalty for selecting an incorrect set (defaulted to on).

Tune Greyscale - Adjust the contrast and delay of the greyscale. This is launched automatically the first time the game is run. Try adjusting until you see four distinct colors and solid grey (besides for the "scrolling line glitch") Note that this "perfect" greyscale isn't really attainable on the regular ti83+ calculators.


# Source Code

This program was compiled with Axe Parser 1.2.2

SETSRC.8xp - The main file
SETPIC.8xp - The graphical data
GREYLIB.8xp - A library created by Runner112 that was used to implement "perfect" greyscale.

The source files are binary files, and cannot be viewed in a regular text editor. They're designed to be edited on a calculator with Axe installed, but they can also be opened with programs like [SourceCoder3](https://www.cemetech.net/sc/).

You can pretty much do whatever you want with the source code, but if you find yourself using it some credit would be appreciated.
