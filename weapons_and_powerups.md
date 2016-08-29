# Power-ups
A power-up is an in game object that applies some effect to a player tank when it is acquired. Power-ups are located on maps (based on config settings) and are picked up by players when they are run over.
## Visual Effect
Power-ups are represented graphically in 3d view as a crate or box. They also have some TBD radar representation (if radar is allowed on the server). Visually all power-ups are identical, they do not have any indication of their contents.
## Picking up Power-Ups
Players may only have a single power-up at a time. Players may choose to drop a power-up at any time and loose it’s abilities. Power-ups are automatically dropped when a player is killed. Dropped power ups may have one of 3 behaviors based on server settings.
1)	De-spawn
2)	Drop to the map location where they are at.
3)	Respawn at a new location.
## Notes on the term “Damage”
The following descriptions will all use the term “Damage” when discussing shots hitting tanks. By default, the game is going to only allow a single hit to destroy a tank, but it will be written in a way that will allow this behavior to be extended in the future. For this reason, this specification will use the term “damage” to describe any “hit action” whether it be an instant kill, or the removal of some “health stat” at a later date.
# Weapon Enhancements
Some power ups enhance the weapons of a tank. 
* Guided Missile – The tank stops firing shells and fires guided missiles. The tank is given the ability to “lock on” to another tank that is within some visible cone. If the shooter has a valid lock then, missiles fired will track the target until the lock changes, or the missile expires. Missiles fired when there is no valid lock, will fly forward like normal shells. When a lock changes, all missiles in flight will track the new lock target. If a lock is cleared, or the locked target is killed, all missiles in flight will continue on the last path. If the shooter loses (drops or is killed) the power-up, the lock will be cleared. 
* Laser –The tank stops firing shells and instead fires continuous beam of laser energy for some specific length of time. All tanks that come in contact with this beam will take damage. If the server settings allow shots to ricochet, the laser will also ricochet up to some maximum number of bounces (or some maximum linear distance).  If a shooter encounters her own laser beam due to a ricochet, it still does damage. If a shooter turns while the beam is on, the beam will dynamically sweep and ricochet in line with the shooters barrel axis. As a general rule, laser has a longer recharge time than other weapons.
* Rapid Fire – The tank fires multiple shells at a much faster rate than normal (faster reload). Shells fired from this enhancement have a faster shot speed then normal as well. All other shell properties are identical to normal shells. 
* Ricochet – This enhancement is only available if the server is not configured for shot ricochet. When acquired all normal shots from this tank ricochet as if the server was configured in such a way All other shell properties are identical to normal shells. 
* Shock Wave – The tank stops firing normal shells and instead emits a spherical energy wave with the tank at the center. Tanks that come in contact with the wave take damage for the amount of time they are in the wave. This means tanks closer to the shooter will receive more damage. The entry wave does not ricochet, or pass through teleporters like normal shots.
* Phased Shots– This enhancement modifies a player’s shots so they are not stopped by world geometry or other tanks.  The shot will not ricochet even if the server is configured to allow it. The shot is not stopped by contact with other tanks, but it does damage them as it passes through them.
* Thief – The tank stops firing shells, and instead fires a short ranged energy beam, that has identical behavior to the laser. When this energy beam contacts another tank, it steals any power-up that the target tank has. This stolen power-up then replaces the Thief power up on the shooters tank and the thief power up is dropped. There is a brief “cool down” time before the acquired power-up is activated and during that time the tank behaves as if it had no power-up (except in the fact that it will not automatically pick up a new power-up). While the tank has the thief power-up, the tank will be shrunk by some factor, and will have increased speed and turning ability as defined by the flag parameters.

# Tank Enhancements
Some power ups enhance the specific properties of a tank. 
* Cloaking – When acquired the tank has the toggle-able ability to become invisible both on radar and in the 3d View from players without the Seer power-up. When a tank is cloaked in this way, it cannot fire shots of any kind.  Entering the cloaked state is relatively quick (a fraction of a second), but de-cloaking takes significantly longer (greater than one second). While de-cloaking a tank is visible and is surrounded by a bright energy flash.  A tank cannot fire until the de-cloaking procedure is fully complete. There is a cool-down that prevents re-cloaking for some short time.
* Seer – When acquired, the tank has enhanced sensors that provide it with much greater information about the world around it. A tank with Seer can see the following items.
1) Cloaked tank, on the screen and on radar. Cloaked tanks are highlighted in a special way
2) The contents of all unclaimed power-ups
3) The power-ups carried by all players
* High Speed – When acquired a tank’s maximum speed will increase in both the forward and backwards directions. If Jumping is enabled on the server, the jump height is increased. 
* Jumping – This power-up is only available on servers where jumping is disabled. When acquired a tank can jump as if it was enabled.

* Narrow – When acquired a tank’s horizontal size is scaled to a very small dimension.  This scaling affects both the visual and hitbox of the tank making it able to move through places an unmodified tank could not, and be much harder to be hit
* Quick Turn – When acquired a tank’s turning speed is massively increased.
* Tiny – When acquired a tank’s scale is massively reduced, both visually and in hit box. A tank’s speed is also lowered proportionally.

