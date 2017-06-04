# Marlin Firmware for Clone

More info at [clone.earth](http://www.clone.earth).
<img align="right" src="https://i.imgur.com/U9apCaa.jpg" height='300px'/>

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

have you considered running your Z slower?
