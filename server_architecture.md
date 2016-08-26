# Server Architecture

## Fitting into global services
The game server itself fits into the integrated global services system as an endpoint module.

![Global Services Diagram](https://cloud.githubusercontent.com/assets/322174/17449088/0ccbcd46-5b0d-11e6-87a2-ab31fcab0d82.png)

In the diagram above the game server itself is listed as "Game Node 1" and "Game Node 2". 

## Game Node Module
The game node module itself is responsible for running a single game instance, or "match". This module can be started by
the global services systems (node controllers), or by individuals, such as developers needing to test code changes.

Once a node is running, it accepts game protocol connections and services players as needed. IF started via a Node controller,
the game node will be required to send status information back to the controller so it can be managed by the global system.

## Authentication
Describe how the game node gets authentication info from global and validates them (one time crypto magic from node controller?)

## Networking Threads
For performance and scalability, the game node must detach it's networking workflow from the gameplay workflow. This will most
likely be implemented using a separate networking thread that handles lower level transport code and pushes messages into the
game state. Some networking libraries already support this method so implementation will depend on what library is selected.

## Game State
The server must maintain an accurate and authoritative game state. 

## Logging
We should have some.
