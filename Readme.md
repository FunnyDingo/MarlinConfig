# Overview
Sometime I found an example configuration[^1] for the Marlin firmware 2.1.1 for my Ender-5 Pro with BigTreeTech SKR Mini E3 3.0 mainboard. The Marlin project itself doesn't provide a configuration for this.

I compared that config against the official example for *Ender-5 Pro / BigTreeTech SKR Mini E3 2.0 with BLTouch* for Marlin 2.1.2 as a new start point for future changes.

# Changes
Here is a list of changes if you compare the config against the *SKR Mini E3 2.0* example

## Configuration.h
- PSU_ACTIVE_STATE HIGH
- BED_MAXTEMP 150
- DEFAULT_bedKp 77.5
- DEFAULT_bedKi 15.14
- DEFAULT_bedKd 264.5
- ENDSTOP_INTERRUPTS_FEATURE enabled
- Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN enabled
- NOZZLE_TO_PROBE_OFFSET { -46.3, -6.1, -0.58 }
- PROBING_NOZZLE_TEMP 205
- PROBING_BED_TEMP 60
- DISABLE_INACTIVE_EXTRUDER enabled
- X_BED_SIZE 220
- Y_BED_SIZE 220
- LEVELING_NOZZLE_TEMP 205
- GRID_MAX_POINTS_X 5
- PREHEAT_1_TEMP_HOTEND 205
- PREHEAT_1_TEMP_BED 60
- ENCODER_NOISE_FILTER disabled
- SPEAKER enabled
- LCD_FEEDBACK_FREQUENCY_DURATION_MS 20
- LCD_FEEDBACK_FREQUENCY_HZ 600
- FAN_SOFT_PWM disabled
- DIAG_JUMPERS_REMOVED enabled

## Configuration_adv.h
- CONTROLLER_FAN_PIN FAN2_PIN
- E0_AUTO_FAN_PIN FAN1_PIN
- SET_PROGRESS_MANUALLY enabled
- M73_REPORT enabled
- SDCARD_SORT_ALPHA enabled
- SDSORT_USES_RAM true
- SDSORT_CACHE_NAMES true
- BABYSTEP_WITHOUT_HOMING enabled
- BABYSTEP_ALWAYS_AVAILABLE enabled
- EMERGENCY_PARSER enabled
- M115_GEOMETRY_REPORT enabled
- M114_DETAIL enabled
- REPORT_FAN_CHANGE enabled
- HOST_ACTION_COMMANDS enabled
- HOST_PAUSE_M76 enabled
- HOST_PROMPT_SUPPORT enabled

[^1]: Sorry, I forgot the source. If I find it again, I will mention it here with thanks ;)