# Introduction
This is the repository where Team Chillax will be designing its current open-source game project: an as-of-yet unnamed 3D internet multiplayer action game. We are using this repository to lay out design specifications for this project which will be used to guide development efforts and provide a clear vision for what we want to accomplish. These plans are a work in progress and updates may occur as designs are created and refined.

## Overall Game Design

This will be a game where the player will be presented with a 3D view of the simulated world. The player will be represented in this world by a vehicle (specifically a tank, with the possibility of support for other vehicles later). The game will have several modes with different objectives, while a significant aspect of game activity will involve shooting other players. There will be powerups that players can pick up which alter some aspect of game behavior, especially adding a capability or weapon. The game should be playable on multiple PC platforms (Windows, Mac OS X and Linux) as well as a limited set of common mobile/embedded platforms. Players on all PC platforms should be able to play together, and ideally players on all platforms (PC and mobile) should be able to play together if this is determined to be viable.

## History
We are a group of developers, players, and server owners from the open-source game [BZFlag](http://bzflag.org). Sadly, that project has run its course and it is time to make something newer and better. Our goal is to create a new game that echoes the fun elements of the game, but meets the expectations of modern users and brings a fresh take to open-source gaming.

## Guidelines
The [design guidelines](design_guidelines.md) document covers a basic overview of the design process. All potential designers and developers should read it to understand our overall development goals.

# Sections
The following is a list of design documents for the project. Some of these pages may not have content yet, but the links will begin working as content is created for them. Items marked with a * have not yet been created.

- [Licenses and Development Guidelines](licenses_and_development_guidelines.md)
- [Target Platforms](target_platforms.md)
- [Gameplay Mechanics](gameplay_mechanics.md)
  - [*Weapons and Powerups](weapons_and_powerups.md)
- [*Client and Server Design](client_and_server_design.md)
  - [*Networking and State Synchronization](networking_and_state_synchronization.md)
  - [*Cheat Prevention](cheat_prevention.md)
  - [*Map Definition](map_definition.md)
  - [*Rendering](rendering.md)
  - [*User Interface and Menus](user_interface_and_menus.md)
  - [Audio](audio.md)
  - [*Input](input.md)
  - [Server Architecture](server_architecture.md) {needs more work}
- [Global Services](global_services.md){needs more work}
- [*Tutorials and Documentation](tutorials_and_documentation.md)
- [*League and Tournament Support](league_and_tournament_support.md)
- [*Extensibility and Modification](extensibility_and_modification.md)

# Contributions
If this project interests you, please be aware that we will need help in many forms from people with many different skills. Specifically, we want help from experienced programmers, artists, level designers, and people with knowledge about build systems/IDEs, network abuse prevention, legal issues for open-source projects, etc. Even without those specific skills, people who are willing to build and test unstable development code on their systems can be a great benefit to the project once source code is generated and the usable product begins to take shape.

# Contact and Discussion
During this initial phase, we will be using this repository for content and will leverage GitHub's various social tools (such as comments) for discussion and collaboration. Additionally, discussion will take place on the ##teamchillax channel on the Freenode IRC network.
