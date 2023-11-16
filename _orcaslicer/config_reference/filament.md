---
layout: default
title: "Filament"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: Filament
---

Configuration options for a configuration file with `"type": "filament"`.

## Activate air filtration

Activate for better air filtration. G-code command: M106 P3 S(0-255)

**Key:** `activate_air_filtration`

**Type:** `Bools`

**Default** `[false]`

### Example

```json
"activate_air_filtration": [true]
```


## Activate temperature control

Enable this option for chamber temperature control. An M191 command will be added before "machine_start_gcode"\nG-code commands: M141/M191 S(0-255)

**Key:** `activate_chamber_temp_control`

**Type:** `Bools`

**Default** `[false]`

### Example

```json
"activate_chamber_temp_control": [true]
```


## Fan speed (auxiliary fan)

Speed of auxiliary part cooling fan. Auxiliary fan will run at this speed during printing except the first several layers which is defined by no cooling layers.
Please enable auxiliary_fan in printer settings to use this feature. G-code command: M106 P2 S(0-255)

**Key:** `additional_cooling_fan_speed`

**Type:** `Ints`

**Min:** `0`

**Max:** `100`

**Default** `[0]`

### Example

```json
"additional_cooling_fan_speed": [3]
```


## Chamber temperature

Higher chamber temperature can help suppress or reduce warping and potentially lead to higher interlayer bonding strength for high temperature materials like ABS, ASA, PC, PA and so on. At the same time, the air filtration of ABS and ASA will get worse.While for PLA, PETG, TPU, PVA and other low temperature materials, the actual chamber temperature should not be high to avoid cloggings, so 0 which stands for turning off is highly recommended

**Key:** `chamber_temperature`

**Type:** `Ints`

**Min:** `0`

**Max:** `1500`

**Default** `[0]`

### Example

```json
"chamber_temperature": [3]
```


## No cooling for the first

Close all cooling fan for the first certain layers. Cooling fan of the first layer used to be closed to get better build plate adhesion

**Key:** `close_fan_the_first_x_layers`

**Type:** `Ints`

**Min:** `0`

**Max:** `1000`

**Default** `[1]`

### Example

```json
"close_fan_the_first_x_layers": [0]
```


## Exhaust fan speed (print complete)

Speed of exhuast fan after printing completes

**Key:** `complete_print_exhaust_fan_speed`

**Type:** `Ints`

**Min:** `0`

**Max:** `100`

**Default** `[80]`

### Example

```json
"complete_print_exhaust_fan_speed": [78]
```


## Cool plate temperature

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the Cool Plate

**Key:** `cool_plate_temp`

**Type:** `Ints`

**Min:** `0`

**Max:** `300`

**Default** `[35]`

### Example

```json
"cool_plate_temp": [27]
```


## Cool plate temperature (initial layer)

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the Cool Plate

**Key:** `cool_plate_temp_initial_layer`

**Type:** `Ints`

**Min:** `0`

**Max:** `120`

**Default** `[35]`

### Example

```json
"cool_plate_temp_initial_layer": [29]
```


## Default color

Default filament color

**Key:** `default_filament_colour`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"default_filament_colour": [""]
```


## Exhaust fan speed (during print)

Speed of exhuast fan during printing.This speed will overwrite the speed in filament custom gcode

**Key:** `during_print_exhaust_fan_speed`

**Type:** `Ints`

**Min:** `0`

**Max:** `100`

**Default** `[60]`

### Example

```json
"during_print_exhaust_fan_speed": [49]
```


## Force cooling for overhang and bridge

Enable this option to optimize part cooling fan speed for overhang and bridge to get better cooling

**Key:** `enable_overhang_bridge_fan`

**Type:** `Bools`

**Default** `[true]`

### Example

```json
"enable_overhang_bridge_fan": [false]
```


## Enable pressure advance

Enable pressure advance, auto calibration result will be overwriten once enabled.

**Key:** `enable_pressure_advance`

**Type:** `Bools`

**Default** `[false]`

### Example

```json
"enable_pressure_advance": [false]
```


## Engineering plate temperature

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the Engineering Plate

**Key:** `eng_plate_temp`

**Type:** `Ints`

**Min:** `0`

**Max:** `300`

**Default** `[45]`

### Example

```json
"eng_plate_temp": [37]
```


## Engineering plate temperature (initial layer)

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the Engineering Plate

**Key:** `eng_plate_temp_initial_layer`

**Type:** `Ints`

**Min:** `0`

**Max:** `300`

**Default** `[45]`

### Example

```json
"eng_plate_temp_initial_layer": [40]
```


## Enable fan cooling for short layer times

Part cooling fan will be enabled for layers of which estimated time is shorter than this value. Fan speed is interpolated between the minimum and maximum fan speeds according to layer printing time

**Key:** `fan_cooling_layer_time`

**Type:** `Floats`

**Min:** `0`

**Max:** `1000`

**Default** `[60.0]`

### Example

```json
"fan_cooling_layer_time": [64.24]
```


## Fan speed (max)

Part cooling fan speed may be increased when auto cooling is enabled. This is the maximum speed limitation of part cooling fan

**Key:** `fan_max_speed`

**Type:** `Ints`

**Min:** `0`

**Max:** `100`

**Default** `[100]`

### Example

```json
"fan_max_speed": [79]
```


## Fan speed (min)

Minimum speed for part cooling fan

**Key:** `fan_min_speed`

**Type:** `Ints`

**Min:** `0`

**Max:** `100`

**Default** `[20]`

### Example

```json
"fan_min_speed": [18]
```


## Filament color

Only used as a visual help on UI

**Key:** `filament_colour`

**Type:** `Strings`

**Default** `["#F2754E"]`

### Example

```json
"filament_colour": [""]
```


## Cooling move speed (last)

Cooling moves are gradually accelerating towards this speed.

**Key:** `filament_cooling_final_speed`

**Type:** `Floats`

**Min:** `0`

**Default** `[3.4]`

### Example

```json
"filament_cooling_final_speed": [2.98]
```


## Cooling move speed (first)

Cooling moves are gradually accelerating beginning at this speed.

**Key:** `filament_cooling_initial_speed`

**Type:** `Floats`

**Min:** `0`

**Default** `[2.2]`

### Example

```json
"filament_cooling_initial_speed": [1.92]
```


## Number of cooling moves

Filament is cooled by being moved back and forth in the cooling tubes. Specify desired number of these moves.

**Key:** `filament_cooling_moves`

**Type:** `Ints`

**Max:** `20`

**Default** `[4]`

### Example

```json
"filament_cooling_moves": [4]
```


## Filamet cost per kg

Filament price. For statistics only

**Key:** `filament_cost`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0]`

### Example

```json
"filament_cost": [2.56]
```


## Filament density

Filament density. For statistics only

**Key:** `filament_density`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0]`

### Example

```json
"filament_density": [0.52]
```


## Deretraction speed

Speed for reloading filament into extruder. Zero means same speed with retraction

**Key:** `filament_deretraction_speed`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"filament_deretraction_speed": [1.28]
```


## Filament diameter

Filament diameter is used to calculate extrusion in gcode, so it's important and should be accurate

**Key:** `filament_diameter`

**Type:** `Floats`

**Min:** `0`

**Default** `[1.75]`

### Example

```json
"filament_diameter": [1.72]
```


## End G-code

End G-code when finish the printing of this filament

**Key:** `filament_end_gcode`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"filament_end_gcode": [""]
```


## Flow ratio

The material may have volumetric change after switching between molten state and crystalline state. This setting changes all extrusion flow of this filament in gcode proportionally. Recommended value range is between 0.95 and 1.05. Maybe you can tune this value to get nice flat surface when there has slight overflow or underflow

**Key:** `filament_flow_ratio`

**Type:** `Floats`

**Max:** `2`

**Default** `[1.0]`

### Example

```json
"filament_flow_ratio": [1.02]
```


## Support material

Support material is commonly used to print support and support interface

**Key:** `filament_is_support`

**Type:** `Bools`

**Default** `[false]`

### Example

```json
"filament_is_support": [true]
```


## Filament load time

Time for the printer firmware (or the Multi Material Unit 2.0) to load a new filament during a tool change (when executing the T code). This time is added to the total print time by the G-code time estimator.

**Key:** `filament_load_time`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0]`

### Example

```json
"filament_load_time": [3.77]
```


## Filament oading speed

Speed used for loading the filament on the wipe tower.

**Key:** `filament_loading_speed`

**Type:** `Floats`

**Min:** `0`

**Default** `[28.0]`

### Example

```json
"filament_loading_speed": [22.98]
```


## Filament oading speed at the start

Speed ulsed at the very beginning of loading phase.

**Key:** `filament_loading_speed_start`

**Type:** `Floats`

**Min:** `0`

**Default** `[3.0]`

### Example

```json
"filament_loading_speed_start": [2.68]
```


## Volumetric speed (max)

This setting stands for how much volume of filament can be melted and extruded per second. Printing speed is limited by max volumetric speed, in case of too high and unreasonable speed setting. Can't be zero

**Key:** `filament_max_volumetric_speed`

**Type:** `Floats`

**Min:** `0`

**Max:** `200`

**Default** `[2.0]`

### Example

```json
"filament_max_volumetric_speed": [1.65]
```


## Minimal purge on wipe tower

After a tool change, the exact position of the newly loaded filament inside the nozzle may not be known, and the filament pressure is likely not yet stable. Before purging the print head into an infill or a sacrificial object, Slic3r will always prime this amount of material into the wipe tower to produce successive infill or sacrificial object extrusions reliably.

**Key:** `filament_minimal_purge_on_wipe_tower`

**Type:** `Floats`

**Min:** `0`

**Default** `[15.0]`

### Example

```json
"filament_minimal_purge_on_wipe_tower": [11.65]
```


## Enable ramming for multitool setups

Perform ramming when using multitool printer (i.e. when the 'Single Extruder Multimaterial' in Printer Settings is unchecked). When checked, a small amount of filament is rapidly extruded on the wipe tower just before the toolchange. This option is only used when the wipe tower is enabled.

**Key:** `filament_multitool_ramming`

**Type:** `Bools`

**Default** `[false]`

### Example

```json
"filament_multitool_ramming": [false]
```


## Multitool ramming flow

Flow used for ramming the filament before the toolchange.

**Key:** `filament_multitool_ramming_flow`

**Type:** `Floats`

**Min:** `0`

**Default** `[10.0]`

### Example

```json
"filament_multitool_ramming_flow": [7.67]
```


## Multitool ramming volume

The volume to be rammed before the toolchange.

**Key:** `filament_multitool_ramming_volume`

**Type:** `Floats`

**Min:** `0`

**Default** `[10.0]`

### Example

```json
"filament_multitool_ramming_volume": [9.44]
```


## Filament notes

You can put your notes regarding the filament here.

**Key:** `filament_notes`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"filament_notes": [""]
```


## Ramming parameters

This string is edited by RammingDialog and contains ramming specific parameters.

**Key:** `filament_ramming_parameters`

**Type:** `Strings`

**Default** `["120 100 6.6 6.8 7.2 7.6 7.9 8.2 8.7 9.4 9.9 10.0| 0.05 6.6 0.45 6.8 0.95 7.8 1.45 8.3 1.95 9.7 2.45 10 2.95 7.6 3.45 7.6 3.95 7.6 4.45 7.6 4.95 7.6"]`

### Example

```json
"filament_ramming_parameters": [""]
```


## Retract amount before wipe

The length of fast retraction before wipe, relative to retraction length

**Key:** `filament_retract_before_wipe`

**Type:** `Percents`

**Nullable:** true

**Default** `[100]`

### Example

```json
"filament_retract_before_wipe": ["98%"]
```


## Only lift Z above

If you set this to a positive value, Z lift will only take place above the specified absolute Z.

**Key:** `filament_retract_lift_above`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"filament_retract_lift_above": [4.07]
```


## Only lift Z below

If you set this to a positive value, Z lift will only take place below the specified absolute Z.

**Key:** `filament_retract_lift_below`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"filament_retract_lift_below": [1.49]
```


## Enforce z-hop behavior

Enforce Z Hop behavior. This setting is impacted by the above settings (Only lift Z above/below).

**Key:** `filament_retract_lift_enforce`

**Type:** `Enums`

**Nullable:** true

**Default** `["AllSurfaces"]`

**Enum values:**


### Example

```json
"filament_retract_lift_enforce": ["Top Only"]
```


## Extra length on restart

When the retraction is compensated after the travel move, the extruder will push this additional amount of filament. This setting is rarely needed.

**Key:** `filament_retract_restart_extra`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"filament_retract_restart_extra": [4.3]
```


## Retract when change layer

Force a retraction when changes layer

**Key:** `filament_retract_when_changing_layer`

**Type:** `Bools`

**Nullable:** true

**Default** `[false]`

### Example

```json
"filament_retract_when_changing_layer": [false]
```


## Retraction length

Some amount of material in extruder is pulled back to avoid ooze during long travel. Set zero to disable retraction

**Key:** `filament_retraction_length`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.8]`

### Example

```json
"filament_retraction_length": [0.9]
```


## Travel distance threshold

Only trigger retraction when the travel distance is longer than this threshold

**Key:** `filament_retraction_minimum_travel`

**Type:** `Floats`

**Nullable:** true

**Default** `[2.0]`

### Example

```json
"filament_retraction_minimum_travel": [2.46]
```


## Retraction speed

Speed of retractions

**Key:** `filament_retraction_speed`

**Type:** `Floats`

**Nullable:** true

**Default** `[30.0]`

### Example

```json
"filament_retraction_speed": [31.64]
```


## Filament seam gap [deprecated]

In order to reduce the visibility of the seam in a closed loop extrusion, the loop is interrupted and shortened by a specified amount.\nThis amount can be specified in millimeters or as a percentage of the current extruder diameter. The default value for this parameter is 10%.

**Key:** `filament_seam_gap`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `10%`

### Example

```json
"filament_seam_gap": "8%"
```


## Filament shrinkage

Enter the shrinkage percentage that the filament will get after cooling (94% if you measure 94mm instead of 100mm). The part will be scaled in xy to compensate. Only the filament used for the perimeter is taken into account.\nBe sure to allow enough space between objects, as this compensation is done after the checks.

**Key:** `filament_shrink`

**Type:** `Percents`

**Min:** `10`

**Default** `[100]`

### Example

```json
"filament_shrink": ["97%"]
```


## Soluble material

Soluble material is commonly used to print support and support interface

**Key:** `filament_soluble`

**Type:** `Bools`

**Default** `[false]`

### Example

```json
"filament_soluble": [false]
```


## Start G-code

Start G-code when start the printing of this filament

**Key:** `filament_start_gcode`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"filament_start_gcode": [""]
```


## Delay after unloading filament

Time to wait after the filament is unloaded. May help to get reliable toolchanges with flexible materials that may need more time to shrink to original dimensions.

**Key:** `filament_toolchange_delay`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0]`

### Example

```json
"filament_toolchange_delay": [3.51]
```


## Filament type

The material type of filament

**Key:** `filament_type`

**Type:** `Strings`

**Default** `["PLA"]`

**Enum values:**


### Example

```json
"filament_type": [""]
```


## Filament unload time

Time for the printer firmware (or the Multi Material Unit 2.0) to unload a filament during a tool change (when executing the T code). This time is added to the total print time by the G-code time estimator.

**Key:** `filament_unload_time`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0]`

### Example

```json
"filament_unload_time": [2.84]
```


## Filament unloading speed

Speed used for unloading the filament on the wipe tower (does not affect  initial part of unloading just after ramming).

**Key:** `filament_unloading_speed`

**Type:** `Floats`

**Min:** `0`

**Default** `[90.0]`

### Example

```json
"filament_unloading_speed": [74.63]
```


## Filament unloading speed at the start

Speed used for unloading the tip of the filament immediately after ramming.

**Key:** `filament_unloading_speed_start`

**Type:** `Floats`

**Min:** `0`

**Default** `[100.0]`

### Example

```json
"filament_unloading_speed_start": [96.73]
```


## Vendor

Vendor of filament. For show only

**Key:** `filament_vendor`

**Type:** `Strings`

**Default** `["(Undefined)"]`

### Example

```json
"filament_vendor": [""]
```


## Wipe while retracting

Move nozzle along the last extrusion path when retracting to clean leaked material on nozzle. This can minimize blob when print new part after travel

**Key:** `filament_wipe`

**Type:** `Bools`

**Nullable:** true

**Default** `[false]`

### Example

```json
"filament_wipe": [false]
```


## Wipe Distance

Discribe how long the nozzle will move along the last path when retracting

**Key:** `filament_wipe_distance`

**Type:** `Floats`

**Nullable:** true

**Min:** `0`

**Default** `[1.0]`

### Example

```json
"filament_wipe_distance": [0.76]
```


## Z hop when retract

Whenever the retraction is done, the nozzle is lifted a little to create clearance between nozzle and the print. It prevents nozzle from hitting the print when travel move. Using spiral line to lift z can prevent stringing

**Key:** `filament_z_hop`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.4]`

### Example

```json
"filament_z_hop": [0.46]
```


## Z hop type

Z hop type

**Key:** `filament_z_hop_types`

**Type:** `Enums`

**Nullable:** true

**Default** `["Normal"]`

**Enum values:**


### Example

```json
"filament_z_hop_types": ["Auto Lift"]
```


## Full fan speed at layer

Fan speed will be ramped up linearly from zero at layer "close_fan_the_first_x_layers" to maximum at layer "full_fan_speed_layer". "full_fan_speed_layer" will be ignored if lower than "close_fan_the_first_x_layers", in which case the fan will be running at maximum allowed speed at layer "close_fan_the_first_x_layers" + 1.

**Key:** `full_fan_speed_layer`

**Type:** `Ints`

**Min:** `0`

**Max:** `1000`

**Default** `[0]`

### Example

```json
"full_fan_speed_layer": [4]
```


## Hot plate temperature

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the High Temp Plate

**Key:** `hot_plate_temp`

**Type:** `Ints`

**Min:** `0`

**Max:** `300`

**Default** `[45]`

### Example

```json
"hot_plate_temp": [51]
```


## Hot plate temperature (initial layer)

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the High Temp Plate

**Key:** `hot_plate_temp_initial_layer`

**Type:** `Ints`

**Max:** `300`

**Default** `[45]`

### Example

```json
"hot_plate_temp_initial_layer": [51]
```


## Nozzle temperature

Nozzle temperature for layers after the initial one

**Key:** `nozzle_temperature`

**Type:** `Ints`

**Min:** `0`

**Max:** `1500`

**Default** `[200]`

### Example

```json
"nozzle_temperature": [242]
```


## Nozzle temperature (initial layer)

Nozzle temperature to print initial layer when using this filament

**Key:** `nozzle_temperature_initial_layer`

**Type:** `Ints`

**Min:** `0`

**Max:** `1500`

**Default** `[200]`

### Example

```json
"nozzle_temperature_initial_layer": [171]
```


## Filament maximum nozzle temperature

The maximum temperature this filament may be printed at

**Key:** `nozzle_temperature_range_high`

**Type:** `Ints`

**Min:** `0`

**Max:** `1500`

**Default** `[240]`

### Example

```json
"nozzle_temperature_range_high": [285]
```


## Filament minimum nozzle temperature

The minimum temperature this filament may be printed at

**Key:** `nozzle_temperature_range_low`

**Type:** `Ints`

**Min:** `0`

**Max:** `1500`

**Default** `[190]`

### Example

```json
"nozzle_temperature_range_low": [191]
```


## Fan speed (overhang)

Force part cooling fan to be this speed when printing bridge or overhang wall which has large overhang degree. Forcing cooling for overhang and bridge can get better quality for these part

**Key:** `overhang_fan_speed`

**Type:** `Ints`

**Min:** `0`

**Max:** `100`

**Default** `[100]`

### Example

```json
"overhang_fan_speed": [79]
```


## Cooling overhang threshold

Force cooling fan to be specific speed when overhang degree of printed part exceeds this value. Expressed as percentage which indicides how much width of the line without support from lower layer. 0% means forcing cooling for all outer wall no matter how much overhang degree

**Key:** `overhang_fan_threshold`

**Type:** `Enums`

**Default** `["95%"]`

**Enum values:**


### Example

```json
"overhang_fan_threshold": ["50%"]
```


## Pressure advance

Pressure advance(Klipper) AKA Linear advance factor(Marlin)

**Key:** `pressure_advance`

**Type:** `Floats`

**Max:** `2`

**Default** `[0.02]`

### Example

```json
"pressure_advance": [0.02]
```


## Keep fan always on

If enable this setting, part cooling fan will never be stoped and will run at least at minimum speed to reduce the frequency of starting and stoping

**Key:** `reduce_fan_stop_start_freq`

**Type:** `Bools`

**Default** `[false]`

### Example

```json
"reduce_fan_stop_start_freq": [false]
```


## Required nozzle HRC

Minimum HRC of nozzle required to print the filament. Zero means no checking of nozzle's HRC.

**Key:** `required_nozzle_HRC`

**Type:** `Ints`

**Min:** `0`

**Max:** `500`

**Default** `[0]`

### Example

```json
"required_nozzle_HRC": [4]
```


## Slow printing down for better layer cooling

Enable this option to slow printing speed down to make the final layer time not shorter than the layer time threshold in "Max fan speed threshold", so that layer can be cooled for longer time. This can improve the cooling quality for needle and small details

**Key:** `slow_down_for_layer_cooling`

**Type:** `Bools`

**Default** `[true]`

### Example

```json
"slow_down_for_layer_cooling": [true]
```


## Layer time

The printing speed in exported gcode will be slowed down, when the estimated layer time is shorter than this value, to get better cooling for these layers

**Key:** `slow_down_layer_time`

**Type:** `Floats`

**Min:** `0`

**Max:** `1000`

**Default** `[5.0]`

### Example

```json
"slow_down_layer_time": [6.12]
```


## Print speed (min)

The minimum printing speed for the filament when slow down for better layer cooling is enabled, when printing overhangs and when feature speeds are not specified explicitly.

**Key:** `slow_down_min_speed`

**Type:** `Floats`

**Min:** `0`

**Default** `[10.0]`

### Example

```json
"slow_down_min_speed": [9.2]
```


## Fan speed (support interface)

This fan speed is enforced during all support interfaces, to be able to weaken their bonding with a high fan speed.\nSet to -1 to disable this override.\nCan only be overriden by disable_fan_first_layers.

**Key:** `support_material_interface_fan_speed`

**Type:** `Ints`

**Min:** `-1`

**Max:** `100`

**Default** `[-1]`

### Example

```json
"support_material_interface_fan_speed": [0]
```


## Softening temperature

The material softens at this temperature, so when the bed temperature is equal to or greater than it, it's highly recommended to open the front door and/or remove the upper glass to avoid cloggings.

**Key:** `temperature_vitrification`

**Type:** `Ints`

**Default** `[100]`

### Example

```json
"temperature_vitrification": [103]
```


## Textured plate temperature

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the Textured PEI Plate

**Key:** `textured_plate_temp`

**Type:** `Ints`

**Min:** `0`

**Max:** `300`

**Default** `[45]`

### Example

```json
"textured_plate_temp": [41]
```


## Textured plate temperature (initial layer)

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the Textured PEI Plate

**Key:** `textured_plate_temp_initial_layer`

**Type:** `Ints`

**Min:** `0`

**Max:** `300`

**Default** `[45]`

### Example

```json
"textured_plate_temp_initial_layer": [39]
```
