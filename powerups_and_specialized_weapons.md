# Power-ups and Specialized Weapons

A power-up is an in-game object that applies some effect to a player tank when it is acquired. The effects will generally be beneficial to the player and will give an advantage in some way (a more powerful weapon, a tank ability, or an informational/situational ability), but "bad" power-ups will be considered for inclusion in the game at a later time if they would improve the overall experience. Power-ups are located on maps (based on config settings) and are picked up by players when they are run over. Power-ups will have a graphical representation to allow users to recognize their location in the world, and will also have an indicator of their locations on the radar.

Players may only have a single power-up at a time. Players may choose to drop a power-up at any time and lose its abilities (if "bad" power-ups are implemented, users would not be able to drop them at will but would be required to complete some maneuver or wait a period of time). Power-ups are automatically dropped when a player is killed. Dropped power-ups may have one of 3 behaviors based on server settings.

1.	De-spawn
2.	Drop to the map location where they are at.
3.	Respawn at a new location.

In the list of power-ups below, the term "damage" is used when discussing shots hitting tanks. At first, it will only take one hit to destroy a tank. However, the game will be designed to be flexible enough that this could be changed in the future. For this reason, this specification will use the term "damage" to describe any kind of hit, whether it be an instant kill or the removal of some "health statistic" at a later date.

## Weapon Enhancements

These power-ups enhance the weapons of a tank:

* Guided Missile – The tank stops firing shells and fires guided missiles. The tank is given the ability to “lock on” to another tank that is within some visible cone. If the shooter has a valid lock, missiles fired will track the target until the lock changes or the missile expires. Missiles fired when there is no valid lock will fly forward like normal shells. When a lock changes, all missiles in flight will track the new lock target. If a lock is cleared, or the locked target is killed, all missiles in flight will continue on the last path. If the shooter loses the power-up (by dropping it or by being killed), the lock will be cleared.
* Laser – The tank stops firing shells and instead fires continuous beam of laser energy for some specific length of time. All tanks that come in contact with this beam will take damage. If the server settings allow shots to ricochet, the laser will also ricochet up to some maximum number of bounces (or some maximum linear distance).  If a shooter encounters his own laser beam due to a ricochet, it still does damage. Laser shots will have an increased shot reload time.
* Rapid Fire – The tank fires multiple shells at a much faster rate than normal (faster reload). Shells fired from this enhancement have a faster shot speed then normal as well. All other shell properties are identical to normal shells.
* Ricochet – This enhancement is only available if the server is not configured for shot ricochet. When acquired, all normal shots from this tank ricochet as if the server was configured in such a way. All other shell properties are identical to normal shells.
* Shock Wave – The tank stops firing normal shells and instead emits a spherical energy wave with the tank at the center. Tanks that come in contact with the wave take damage for the amount of time they are in the wave. If fractional health is ever implemented, tanks will receive more damage the closer they are to the center of the shock wave. The entry wave does not ricochet, nor does it pass through teleporters like normal shots.
* Phased Shots – This enhancement modifies a player’s shots so they are not stopped by world geometry or other tanks.  The shot will not ricochet even if the server is configured to allow it. The shot is not stopped by contact with other tanks, but it does damage them as it passes through them.
* Thief – The tank stops firing shells, and instead fires a short ranged energy beam, that has identical behavior to the laser. When this energy beam contacts another tank, it steals any power-up that the target tank has. This stolen power-up then replaces the Thief power up on the shooters tank and the thief power up is dropped. There is a brief “cool down” time before the acquired power-up is activated and during that time the tank behaves as if it had no power-up (except in the fact that it will not automatically pick up a new power-up). While the tank has the thief power-up, the tank also has the physical abilities of the "Tiny," "Quick Turn," and "High Speed" power-ups below.

## Tank Enhancements

These power-ups enhance the physical or informational/situational properties of a tank:

* Cloaking – When acquired, the tank has the ability (which can be toggled at will) to become invisible both on radar and in the 3D view from players without the Seer power-up. Engaging and disengaging the cloaking ability will require a delay (the specific delays of each will be determined during implementation and play testing). When a tank is cloaked or in the process of engaging or disengaging cloaking, it cannot fire shots of any kind. While de-cloaking a tank is visible and is surrounded by a bright energy flash.
* Seer – When acquired, the tank has enhanced sensors that provide it with much greater information about the world around it. A tank with Seer can see the following items:
  1. Cloaked tanks (on the screen and on the radar); cloaked tanks are highlighted in a special way.
  2. The contents of all unclaimed power-ups; this information persists even after the Seer power-up is no longer held until each unclaimed power-up is claimed and reset.
* High Speed – When acquired, a tank’s maximum speed will increase in both the forward and backwards directions.
* Jumping – This power-up is only available on servers where jumping is disabled. When acquired, this power-up enables a tank to jump as if it were enabled.
* Narrow – When acquired, a tank’s horizontal size is scaled to a very small dimension. This scaling affects both the visual representation and the hitbox of the tank, allowing it to move through places an unmodified tank could not (and to be much harder to be hit).
* Quick Turn – When acquired, a tank’s turning speed is massively increased.
* Tiny – When acquired, a tank’s scale is massively reduced, both visually and for the hit box.
* Shield – When acquired, a tank is surrounded by a damage shield that can absorb some fixed amount of damage. While equipped, all damage to a tank is applied to the shield first. When a shield has reached its damage limit, it will be dropped. Additional damage over the limit will be applied to the tank.
* Thrusters – When acquired a tank’s ability to jump is change dramatically. Instead of a fixed force jump, a tank is able to control the thrust of the jump jets with much more precision. When this power-up is equipped, a tank is given a specific amount of "jump jet power." When activated, the jump jets thrust upwards at a fixed acceleration. The tank only accelerates upward while the thruster is activated. When activated, the thruster uses up jump jet power at a fixed rate. The jet deactivates when the power is used up. Tanks have a certain amount of air control (defined as a % of normal movement speed) when in the air. The thruster can also be used to slow down falls. Based on power-up settings the Jump Jet power recharges slowly over time or is a fixed resource. This power-up is available even if the server is configured to disallow jumping.
