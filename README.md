# ARTY-ANGLICO

## DESCRIPTION:

### ARTY-ANGLICO is a tie-in script that works with (but doesn't necessarily require) our specifically modified CTLD script. If used with CTLD, it allows you to load either an Artillery observer, or an ANGLICO observer. When deployed, and within detection range of the enemy, these two units will find the nearest (ARTY/MISSILE SHIP) unit that can engage them, and begin calling in fire time after time until all detected units are destroyed.  

## SCRIPT USAGE:

* Load MOOSE.lua as a MISSION START trigger without conditions.
* Load ARTY-ANGLICO.lua next, as a MISSION START trigger without conditions.
* Continue on to load Mist, CTLD, CSAR as desired and documented elsewhere.


## MISSION USAGE:

* Any unit that is to fire on command of either observer must have their GROUP name begin with **"ARTY."** Reserve this name for ONLY those actual Artillery or Naval units that are expected to fire. Don't name other groups with "ARTY."
* You must place an HQ group somewhere on the map. This can be any unarmed ground vehicle you want, placed anywhere on the map at all. Its GROUP name must be HQ. This unit is relied on for message routing. 
* If you choose to place specific ARTY or ANGLICO personnel on the map, they should be named beginning with "JTAC" for Artillery observers, or ANGLICO for Naval Missile work. 
* The deployed unit via CTLD is the BSD Marine TOW Infantry Unit. You can use other units, but this one is more easily CTLD transportable. A regular Infantry guy has no sensors and won't detect anything. The TOW unit is highly recommended.
* Behaviors:
  * Detection range is highly conditions dependent, LoS only, and will extend to 6-7km at max. 
  * The TOW unit will fire on enemies himself unless you are too far away (4km+) for him to engage. You can CA him to HOLD FIRE if desired.
  * He will detect at night, but his range is severely reduced.
  * The ARTY or ANGLICO observer will keep fire coming from the nearest applicable asset until:
  * All detected targets are destroyed, or
  * The firing unit is out of ammo.
* For Cruise Missiles, the initial salvo will typically be 150% of the target population. They will re-engage as often as needed.

*  A variable must be set to allow automatic calls for fire.  This can be done in a DO_SCRIPT trigger with the following code statement:

call_for_fire_allowed = true

*If this is NOT set, the personnel will not issue calls for fire*


## ANGLICO SPECIFICS

* Calling for ANGLICO fire (cruise missile) is NOT automatic. It is a three step process:

1 - enable call_for_fire_allowed.  Either at large in your mission, or by creating radio menus that do so.  

2 - Assembling a target list.  This is the targets that the ANGLICO guy sees at any one time. The list of engageable targets is displayed as messages. The list will fluctuate somewhat (welcome to DCS), so re-select this radio menu item as many times as is necessary to get the list you want.

3 - Execute the call for fire. Selecting this takes the target package in step #2, calls them all in to the ship, and clears them to fire. If a target is NOT in the list in #2, it will NOT be engaged.  

A salvo of BGM-109 missiles will be sent to your targets.  

## DCS LIMITATIONS:

* Ground Artillery is not point-accurate in DCS and cannot be made to be so. It may take numerous engagement cycles to hit even a single target. 
* Cruise missiles (From the Arleigh Burke or Ticonderoga class ships) sometimes follow terrain too closely. They may crash into terrain if they encounter repeated and steep peaks and valleys. It is not possible to modify the missile trajectory. Find some other way to engage that target.
* Cruise missiles need lofting room to see their target. They cannot successfully attack a target that is on the leeward (far) side of a hill. They will often overshoot.
* If you see this happening, or see the cruise missile crashing into the same tree over and over that is blocking the target, don't let the ship exhaust its ordnance. Instead:
* retrieve the observer back into the helicopter, or 
* Use CA to place the ship on "HOLD FIRE" ROE.  
* Reposition the ship with CA to avoid the troublesome obstacle (time consuming)
  
  
  
