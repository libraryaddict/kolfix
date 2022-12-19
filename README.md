# kolfix

Provides shortcuts for setting commonly used [KoLmafia](https://github.com/kolmafia/kolmafia/) preferences. Useful for users who have had their preferences recently lost.

## Currently supported things:

__Updated via `auto`:__

&#x2611; Crafting Discoveries

&#x2611; Sweat from [Designer Sweatpants](https://kol.coldfront.net/thekolwiki/index.php/Designer_sweatpants)

&#x2611; Puzzle Champ from [Witchess](https://kol.coldfront.net/thekolwiki/index.php/Your_Witchess_Set)

&#x2611; [Source Terminal](https://kol.coldfront.net/thekolwiki/index.php/Source_Terminal) (Some properties can't be read if you've used all the resources today)

__Requires Individual Setting or `maxAll`:__

&#x2611; [\[glitch season reward name\]](https://kol.coldfront.net/thekolwiki/index.php/Glitch_season_reward_name)

&#x2611; Calculate the Universe from the [Manual of Numberology](https://kol.coldfront.net/thekolwiki/index.php/Manual_of_Numberology)

&#x2611; [Gingerbread City](https://kol.coldfront.net/thekolwiki/index.php/Civic_Planning_Office)

&#x2611; Rack 'em up at [A Shark's Chum](https://kol.coldfront.net/thekolwiki/index.php/A_Shark's_Chum). (Your permanent pool skill (as shown in the quest log at start of ascension) is derived from: $\lfloor2\sqrt{RackEmUps}\rfloor$)

&#x2611; [Tunnel of L.O.V.E.](https://kol.coldfront.net/thekolwiki/index.php/The_Tunnel_of_L.O.V.E.)

__Daily Flag Fixes:__

&#x2611; [June Cleaver](https://kol.coldfront.net/thekolwiki/index.php/June_cleaver)

## Installation

To install, copy and paste the following into the KoLmafia Graphical CLI aka GCLI:

```
git checkout https://github.com/s-k-z/kolfix.git release
```

## Usage

__For a full list of options in KoLmafia__:
```
kolfix
```

__Examples__:

Set today's June Cleaver counters to safe values, for other scripts to continue automating with it (also resets on rollover/ascension):
```
kolfix cleaver
```

Check any properties that can be automatically updated, set permanent pool skill and manual of numberology to the maximum, and mark gingerbread city and tunnel of love as owned and fully upgraded:
```
kolfix auto maxAll
```

Set the quantity of manuals of numberology used to 3, and rack 'em up count to 10:
```
kolfix numberology=3 pool=10
```

To set the number of [glitch season reward name] implementations, either fight the %monster% today and record the big meat drop (same value as hp and mp restored) or search your most recent session log for this value. Calculate: 

`X = today's %monster% meat drop / (5 x [glitch season reward names] owned)`

for example: `100 = 1000 meat / (5 x 2 [glitch season reward names])`
```
kolfix glitch=100
```