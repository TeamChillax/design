# Global Services

Global services will be run by the project which will provide the core functionality of authentication, authorization, global chat, matchmaking, and other services to the community of players.

## Stability and security

The services will be split up into multiple subprojects or modules. Each module should allow for running an arbitrary number of instances distributed across multiple datacenters and providers to enable scaling and to absorb attacks. There should also be some sort of health check system to ensure that each instance is behaving as expected, and if not, will remove or repair the instance.

Services should communicate with each other through defined APIs, using encrypted communication where it makes sense. Versioned APIs may be an option to allow gradual rollouts of other modules that depend on a newer API of another module.

The system will end up handling sensitive user information, such as passwords. The code that handles sensitive information should be written as simple and straightforward as possible to ease auditing. When possible, memory safe programming languages like Rust should be used.

## Fitting in with game servers

The global services components act as a front end to the game server (game node).

![Global Services Diagram](https://cloud.githubusercontent.com/assets/322174/17449088/0ccbcd46-5b0d-11e6-87a2-ab31fcab0d82.png)

In the diagram above the all components except "Client App", "Game Node 1" and "Game Node 2" are part of the global services network.

## Components

### Authentication

The authentication service will be a simple codebase that takes a username and password, if valid, will return a cryptographically secure token or certificate.  At the minimum, this will be used by the game client directly. It is likely to also be used by websites indirectly through some sort of web login system, perhaps using OAuth 2.0 or similar standard.  Game servers may also make use of this for authenticating themselves with the system.

Services (such as game servers) should not need to contact the authentication service to validate a user's identity. By this, I mean that whatever the client gives the service should offer trusted and immutable information that only that service is able to read. The obvious way to accomplish this would be through public key cryptography. On the flip side, we should avoid a system that allows information to be intercepted or recorded that ends up providing unauthorized access to an account with no way to revoke that access. Short token/certificate validity periods may be enough protection against this, however.

## Global Chat

The global chat service will be used to provide lobby and cross-server chat for players.

## Asset Management

This service is responsible for managing requests for game assets (textures, scripts, sounds, other media) made by client systems. This service will need to manage multiple versions of files and host them out quickly and efficiently. Ideally some type of repository or CDN would be used on the back end.

## Lobby

This service provides chat and matchmaking services for clients after they have logged in with the authentication services. The Lobby system maintains a list of active Node controllers, and what games they are running. Based on player input, the lobby system will request game instances with specific settings from the Game Node network. It is the lobby system's job to redirect players to specific game nodes for play.

## Game Node Controller

The Game Node Network is comprised of physical servers running the Node Controller Application. This application is
responsible for starting and stopping game nodes as needed. Node Controllers communicate with the lobby service over a secured connection to the lobby server with specific cryptographic keys.
