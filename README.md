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
  * Detection range is highly conditions dependent, and will extend to 6-7km at max. 
  * The TOW unit will fire on enemies himself unless you are too far away (4km+) for him to engage. You can CA him to HOLD FIRE if desired.
  * He will detect at night, but his range is severely reduced.
  * The ARTY or ANGLICO observer will keep fire coming from the nearest applicable asset until:
    * All detected targets are destroyed, or
    * The firing unit is out of ammo.
* For Cruise Missiles, the initial salvo will typically be 150% of the target population. They will re-engage as often as needed.

## DCS LIMITATIONS:

* Cruise missiles (From the Arleigh Burke or Ticonderoga class ships) sometimes follow terrain too closely. They may crash into terrain if they encounter repeated and steep peaks and valleys. 
* Cruise missiles cannot successfully attack a target that is on the leeward (far, downhill) side of a hill. They will often overshoot.
* If you see this happening, or see the cruise missile crashing into the same tree over and over, stop the madness by either:
  * retrieving the observer back into the helicopter, or 
  * Using CA to place the ship on "HOLD FIRE" ROE.  
  
  
  
