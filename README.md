# Marlin Firmware for Clone

More info at [clone.earth](http://www.clone.earth).
<img align="right" src="https://s3-us-west-1.amazonaws.com/www-clone-earth-assets/home.jpg" height='300px'/>

This is [Marlin 1.1.x Firmware](https://github.com/MarlinFirmware/Marlin) which has been optimized for the Clone's hardware.

Much love to the Marlin folks. Thanks for the great work!

## Changes

### Configuration.h

* `STRING_CONFIG_H_AUTHOR`
* `STRING_SPLASH_LINE1`
* `STRING_SPLASH_LINE2`
* `TEMP_SENSOR_BED`
* `HEATER_0_MAXTEMP`
* `BED_MAXTEMP`
* `PREVENT_COLD_EXTRUSION`
* `EXTRUDE_MINTEMP`
* `ENDSTOPPULLUPS`
* `X_MIN_ENDSTOP_INVERTING`
* `Y_MIN_ENDSTOP_INVERTING`
* `FIX_MOUNTED_PROBE`
* `X_PROBE_OFFSET_FROM_EXTRUDER`
* `INVERT_X_DIR`
* `INVERT_Z_DIR`
* `GRID_MAX_POINTS_X`
* `Z_MIN_ENDSTOP_INVERTING`
* `Z_MIN_PROBE_ENDSTOP_INVERTING`
* `AUTO_BED_LEVELING_BILINEAR`
* `LEFT_PROBE_BED_POSITION`
* `RIGHT_PROBE_BED_POSITION`
* `BACK_PROBE_BED_POSITION`
* `X_MAX_ENDSTOP_INVERTING`
* `Y_MAX_ENDSTOP_INVERTING`
* `Z_MAX_ENDSTOP_INVERTING`
* `Z_CLEARANCE_BETWEEN_PROBES`
* `DEFAULT_AXIS_STEPS_PER_UNIT`

Disabled the following

* `MIN_SOFTWARE_ENDSTOPS`
* `MAX_SOFTWARE_ENDSTOPS`

### Calibration steps

1. `G28`
  * Home X, Y and Z
2. `G29`
  * Bed Leveling Routine
3. `G1 X50 Y30 F5000`
  * Move to a good place for the next steps
4. `G1 Z0`
  * Move the Z Axis to it’s absolute 0 point
5. `G92 Z10`
  * Tell the Z it’s now at 10mm, even though it won’t move
  * Manually move to where paper slides under extruder tip
6. `M114 Z`
  * Gets the axis current values
  * Take the Z value reported and plug it into this equation (Offset = 10 - Z + 0.1)
7. `M851 Z-Offset`
  * Note this means you would type the letter Z then a minus sign, and then the value of ‘Offset’ from the previous step: Ex: `M851 Z-0.7`
8. `M500`
  * Save to EEPROM
