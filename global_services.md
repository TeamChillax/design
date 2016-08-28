# System Architecture

Global services is the name used for the "front end" servers that provide authentication, authorization, update, 
and matchmaking services to the overall community of players.

They are an integral part of the overall play experience and turn a simple game into a community.

## Fitting in with game servers
The global services components act as a front end to the game server (game node).

![Global Services Diagram](https://cloud.githubusercontent.com/assets/322174/17449088/0ccbcd46-5b0d-11e6-87a2-ab31fcab0d82.png)

In the diagram above the all components except "Client App", "Game Node 1" and "Game Node 2" are part of the global services
network.

## Components

### Authentication Service
This service is responsible for providing user management and authentication. Optimally it will have multiple load balanced
endpoints using a secure high availability protocol (HTTPS?). Other components will communicate with the authentication 
nodes to provide an identity to all users.

For clients, the authentication system will securely validate login credentials and issue some form of cryptographically secure 
token.

Clients will send this token to other services (such as the Lobby Service) for validation. These other services will then 
validate the token (ether cryptographically, or by contacting an authentication node).

Implementation Details TBD.

## Asset Management Service
This service is responsible for managing requests for game assets (textures, scripts, sounds, other media) made by client 
systems. This service will need to manage multiple versions of files and host them out quickly and efficiently. Ideally some 
type of repository or CDN would be used on the back end.

## Lobby Service
This service provides chat and matchmaking services for clients after they have logged in with the authentication services.
The Lobby system maintains a list of active Node controllers, and what games they are running. Based on player input, the 
lobby system will request game instances with specific settings from the Game Node network. It is the lobby system's job to
redirect players to specific game nodes for play.

## Game Node Controller
The Game Node Network is comprised of physical servers running the Node Controller Application. This application is
responsible for starting and stopping game nodes as needed. Node Controllers communicate with the lobby service over a secured
connection to the lobby server with specific cryptographic keys.
