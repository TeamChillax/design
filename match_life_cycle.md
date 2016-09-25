# Match Life Cycle

This page describes the life cycle of a "match" (or an "instance" of a game).

## Beginning a Match

Players will be able to create a game instance by selecting a map and choosing any applicable game options. Game options may include such things as whether shots ricochet, whether tanks may jump, the particular game style (or objective) to be played, and when the game will end (see "Ending a Match" below). If the match is configured to have a countdown with a formal/manual start, the game should allow a "warm up" period prior to the formal match time to allow for teams to be assigned and for the players to prepare (once the game formally starts, the game state and the scoreboard should be reset).

## Basic Game Objectives

The game will include several basic modes, each with a specific objective. The objective for one mode might be attaining the greatest number of kills (and fewest deaths), while the objective for another mode might be capturing an enemy flag (and defending the friendly flag).

## Custom Game Objectives

In order to maintain player interest, there should be support for a variety of game modes/objectives, including more complicated ones that may require teamwork, may require a task to be completed within a specific period of time, or may have teams arranged in an unequal way for a period of time, etc. In order to open up the game to new ideas for objectives, the game will need at least a server-side API or scripting interface so that contributors can customize this behavior. The specific implementation choices for this API or scripting interface will be made at a later time, but currently Lua, AngelScript, and possibly JavaScript appear to be viable options.

## Ending a Match

Several options for ending a match will be made available for configuration, including a time limit/countdown, a player score limit, or a particular number of objective completions. Open-ended games should also be possible, but matches with pre-defined limits should be encouraged and should be the default setting. The reason for this is that there are several advantages to resetting the game from time to time, including rearranging the players on teams so they are more evenly matched, giving players who can only play for a short time clear increments where they can join and then leave, allowing for an entire group of players to migrate from one map or game style to another (such as with a rotation), and so on.

## League and Tournament Support

If this project results in a successful and popular game, we should anticipate that there may be a demand for competitive league play. In leagues, players would join teams and compete for high rankings on a ladder. League play will require tight integration into the client, global game services, and web services so that players will be able to start league matches, find teammates and opponents for matches, view the ranking ladder and activity counts, and keep themselves informed of league rules and announcements. At this time, it would be premature to make these league-related features requirements, since we do not currently know if such a system will be in demand. However, the game client, infrastructure, and other modules must be implemented with these features in mind so that if these features are needed, they also may be implemented without excessive revision or reorganization of the existing code.
