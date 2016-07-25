# Vehicle World Interactions

We need to decide how we want the various vehciles to interact with the world. We all know what bzflag does, but there are many questions regarding what should be done.

## Open questions

1. Will vehicles stay flat?
2. How will vehicles deal with non flat world geometry?
3. Will weapons be able to rotate seperate from the vehicle (tilt, rotation, tilt and rotation?)
4. Jumping?
5. Intagabiity powerups?
6. Dyanmic world geometry? Doors?
7. Teleporters?
8. Local physics overide on world geometry? (like bzflag physics drivers).


## Flat Tanks
Will vehicles stay flat? This is known as the tilting tank issue. In bzflag tanks are flat. There are many reasons for this, mainly it's simple and it allows gameplay to be fun with out turret aiming.

If we allow tanks to tilt, we have to solve the following problems.

How do people aim the guns when on a slope? Obvious solution is to allow some form of weapon rotaiton. Failure to allow some form of aiming will make it very hard to to line up shots when on a slope.

If we allow tanks to tilt, we also have to deal with how tanks fall off ledges. Do we allow them to flip over? If we do how do players get right side up again? Do we do a hybrid method where tanks can tilt from the ground, but not from a ledge?


## Weapon rotation
Another big often asked question, should turrets be aimable?

Allowing vertical aiming does solve many problems with allowing vehciles to tilt, and adds a different dimension to the game. It does bring up additional requirements, namely in the realm of input.

Allowing aiming of any axis will require a second set of input axes. Right now BZFLag gets away with a single set of axes, X and Y. This means it can be played with one hand, keyboard or mouse. Adding aiming will mean at least 3 axes will be needed, X and Y for driving, and Z for aiming.

Most games solve this by having players use 2 hands. motion on one, aiming on another. this is most commonly implmented as a mouse/keyboard combination. Of the two input devices the mouse has much more granularity than the keyboard (it is effectilvy an analog control). For this reason most players will prefer to have the axes that afect the shot direction assigned to the mouse. This means steering and vertical aiming on the mouse, and forward/backward motion on the keyboard.

There are of course alternative inputs, like a gamepad, that will be a fine solution. Some people have sugested other alternate inputs, such as using the mouse wheel for vertical aiming, or various "up/down" keys to move the turret. While these may be possible, they will not offer the speed and precision of a mouse. We need to take this all into accoutn when thinking about this feature.

Turret rotaiton adds an additonal axis, so it compounds the issue further. Additiialy if we assume that we will want the camera to be alligned with the weapons system (for aiming), then we have cases where people can't see where they are driving. This may be a desirable trade off, but we should investegate it's frustation level. Perhaps the system would need driving modes, or controls to quicly allign the vehcile to the camera.

## Jumping
Jumping has the fewest questions and ramfications. It is mainly a gameplay choice and will only really affect map design.

## Inagability
Do we want to allow players go pass through world geometry. The only reason we need to make this choice is so our design can include features to allow it. If we allow it we'll need to come up with some graphical effect to show it, and decide how we want to handle ambigous cases in world geomentry (preventing players from phasing through the floor for instance).

## Dynamic world geometry
If we want to do this, it will require some choices for our 3d engine (redering and lighting), simulation, networking, and physics systems. The answer to this basicly helps set up requirements for those systems.

## Teleporters
Like jumping this does not have a large number of ramfiications, it just sets some requirements.

## Physics override
This as the same conerns as Dynamic world geometry.

