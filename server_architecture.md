# Server Archetcture 

## Overview
The overall design of the server focuses on modularity and extensibilty. The main ideas are to keep conenctions segregated into "rooms" for various different reasons. This allows the system to support a range of features with easy maintenance and security.

## Design

The inital network layer will be some kind of socket level interface, ether direct sockets or a networking library with a high level API. This layer will be responsible for managing incoming connections, reading new messages, and sending queed messages. This system will maintain a PEER object for each coneected user. The peer object encapsulates the network connection and stores both inbound and outbound messages that need to be processed. The socket level interface will use threads to ensure that message transport is handled asyncronsly.

Each peer object contains a reference to a peer handler object. this object has methods that are notified when a peer object receives new data. As a peer moves throughout the system it will be passed from one handler to another. All peers must have one and only one handler at a time. Peers with out handlers are invalid. Peer handlers only contain code to handle the message types or data they are responsible for. All othere data is considered out of scope and will be ignored.

All newly connected peers are initaly assigned to the security lobby. This is a special handler that manages all inital connection securty and authetnication. Peers will stay with this handler while the following security checks are completed.
1. IP ban checks
2. Reverse DNS Lookups
3. Hostmask ban checks
4. Flood/attak protecton ban checks
5. Authentication
6. Authorization

The security lobby peer handler will use thread pools to manage these tasks asyncronsly. WHen a peer is validated, it's security status is marked as an attribute in the peer object, and the peer is transfered to a game lobby instance..

When a peer is sent to a game lobby, the client is told of the status change. The game lobby will send the client a list of game rooms and a list of lobby chat participants. The game lobby handler only contains code for the following.

1. Room listing
2. Room creation
3. Room selection
4. Chat user enumeration
5. Chat messages

While in this lobby, players can select a game room or create new ones with the desired attributes (game style, map, etc..). When the user wishes to join a game, they send a room selection request to the lobby. The game lobby will check with the room object and transfer the peer once approved. The server can have as many game lobby instances as needed and can manage what lobby players go to.

A game room is a peer handler that runs a game state. Each peer in a game room is assigned a player ID and a player record. When joining a game room a peer is sent all the data needed for the game and can spawn when they have a syncronzed state. If a player does not spawn, they will simply be observers in the game. The client side GUI manages how "observer only" players are displayed and will prevent them from sending a spawn message. For games with fixed players, the game room can deny spawns from inapropriate sources while matches are in play. MEssages to the client can provide GUI hints for who can and can not spawn.

From a game room a player can only quit or transfer back to a lobby. Changing rooms requires going back to a lobby first.


## Advantages
1. Code maintenance is easier. Each section of the process is wrapped up in it's own class. The code for the security lobby only has to deal with the messages it cares about, same for game lobbies and game rooms.
2. Scaling. Each room can use it's own threads and gamestates, so as more games are needed more system resources can be used.
3. Multiple endpoints. Multiple socket level interfaces can feed into the same pool of rooms and lobbies, since the guts of the networking code is wrapped up in the peer class.





