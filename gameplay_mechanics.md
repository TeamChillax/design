# Player/World Interaction
Player vehicles (tanks) will interact with the world geometry in the following ways.

## Motion
* Tanks will always stay flat (oriented with a theoretical ground plane)
* Tanks can "step up" small changes in Z when driving over world geometry
* When tanks encounter world geometry that is not flat (slopes) they will attempt to climb them based on some traction computation (TBD)
- Proofs of concept of the traction computation will be done during implementation
* When tanks encounter world geometry that is not passable, they will not clip that geometry. If the ground under a tank is not flat, jump jets will be fired to make it look like the tank is using them to maintain stability.
* Tanks can Jump (see below)
* Tanks can not collide with other thanks

### Jumping
Normal Jumping is always a fixed force jump, and thus a fixed height jump. A tank has no controll over motion or rotaiton when it is not in contact with some surface. Power-ups such as Thusters can modify this behavor.

## World Assumptions
* In initial implementations the world will be static
* The world will define both graphics and collision properties
- Editor and Runtime formats TBD
* Provisions for "physics drivers" or "Physics volumes" will be evaluated
- Implementation if possible
- Surface properties if not
-- At least a "Death" property to create out of bounds areas
-- Implementing "passible" properties to allow one-way traversal of a solid object would be desired if feasible.

## Teleporters
* The world will be able to define teleporters
* Teleporter fields will be defined as any regular polygon
- A mapping algorithm will be made to convert from one regular polygon to another.
* A system to see what is on the other side of a teleporter will be evaluated.
- There may be mobile limitations, experimentation will tell.

# Shots

## Shooting
* Shots fired from tanks will always be flat.
- Turrets will not rotated up/down or left/right
* Some shot types will have the ability to ricochet
- To be defined with power-ups

## Getting Hit
* Tanks will maintain an internal "health" attribute
* Shots will maintain an internal "Damage" attribute.
- Initial implementation will give both attributes a value of 1 for legacy familiarity, attributes are only for extensibility
