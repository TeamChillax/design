League and Tourmanment Support
==============================

The game system will be writen with full support for completive play. The goal of this feature is to make it very easy for groups of players to form leagues and play in a competitive manner. For this reason, the entire league system is integrated into the game and the global services model.

League Registration
===================

The global services system must support the ability for league administrators to register and manage named leagues. When a league is registered, one or more registered users are assigned to be league administrators. League administrators can set league rules such has;

-   Game Styles

-   Match Length

-   Scoring Types

-   Match game settings

-   Team Settings

Monetization (optional)
-----------------------

If desired, a donation to the project can be required before a league can be registered.

Teams
=====

Once a league is registered, it’s options will determine how teams are formed. If the league is open, then players can apply to register a new team. Depending on league settings, new teams may require manual approval. The user that registers a team will be set as the team leader by default. A team leader or league admin can transfer leadership of a team as needed.

Once a team is registered, based on league settings, players can then join, or be invited. Once accepted/joined, a player is then associated with a team within that league.

Matches and Game Nodes
======================

The lobby network is aware of all registered leagues and will allow teams to spawn game nodes as league matches. Depending on League settings, matches can be scheduled, or started at any time.

All matches are always spawned into new game instances specifically for the teams that are playing. Team members participating in the match are directed to the game node from the lobby system. Only team members from the playing teams will be allowed to play in the match game instance, all other users will be forced into observer status. Depending on league settings, player substitutions may be allowed, initiated by team members, or league admins.

When a league match ends, it’s stats and scoring is sent to the league system automatically. Manual match entry is not needed, and specifically disallowed. Since the lobby system can create matches at any time, this should not be a problem for the players.

League Sites
============

The global services system will provide some type data display of data for matches that have been played. This system only needs to provide roster and match data, it does not need to support social aspects, such as forums or chat. Optimally the league, team, and match data will be accessible via some web based API for inclusion in third party league and team sites.
