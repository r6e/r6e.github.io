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

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"activate_air_filtration": ["1"]
```

## Activate temperature control

Enable this option for chamber temperature control. An M191 command will be added before "machine_start_gcode"
G-code commands: M141/M191 S(0-255)

**Key:** `activate_chamber_temp_control`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"activate_chamber_temp_control": ["1"]
```

## Fan speed

Speed of auxiliary part cooling fan. Auxiliary fan will run at this speed during printing except the first several layers which is defined by no cooling layers.
Please enable auxiliary_fan in printer settings to use this feature. G-code command: M106 P2 S(0-255)

**Key:** `additional_cooling_fan_speed`

**Type:** `[integer]`

**Default:** `0`

**Max:** `100`

**Min:** `0`

### Example

```json
"additional_cooling_fan_speed": ["70"]
```

## Chamber temperature

Higher chamber temperature can help suppress or reduce warping and potentially lead to higher interlayer bonding strength for high temperature materials like ABS, ASA, PC, PA and so on.At the same time, the air filtration of ABS and ASA will get worse.While for PLA, PETG, TPU, PVA and other low temperature materials,the actual chamber temperature should not be high to avoid cloggings, so 0 which stands for turning off is highly recommended

**Key:** `chamber_temperature`

**Type:** `[integer]`

**Default:** `0`

**Max:** `max_temp`

**Min:** `0`

### Example

```json
"chamber_temperature": ["0"]
```

## No cooling for the first

Close all cooling fan for the first certain layers. Cooling fan of the first layer used to be closed to get better build plate adhesion

**Key:** `close_fan_the_first_x_layers`

**Type:** `[integer]`

**Default:** `1`

**Max:** `1000`

**Min:** `0`

### Example

```json
"close_fan_the_first_x_layers": ["3"]
```

## Compatible machine

**Key:** `compatible_printers`

**Type:** `[string]`

**Default:** `null`

### Example

```json
"compatible_printers": [
    "Anker M5 0.4 nozzle",
    "Anker M5C 0.4 nozzle"
]
```

## Compatible machine condition

A boolean expression using the configuration values of an active printer profile. If this expression evaluates to true, this profile is considered compatible with the active printer profile.

**Key:** `compatible_printers_condition`

**Type:** `string`

**Default:** `null`

### Example

```json
"compatible_printers_condition": "printer_notes=~/.*PRINTER_VENDOR_PRUSA3D.*/ and printer_notes=~/.*PRINTER_MODEL_MK3.*/ and nozzle_diameter[0]==0.4"
```

## Compatible process profiles

**Key:** `compatible_prints`

**Type:** `[string]`

**Default:** `null`

### Example

```json
"compatible_prints": []
```

**Note:** There are currently no built-in profiles that use this setting.

## Compatible process profiles condition

A boolean expression using the configuration values of an active print profile. If this expression evaluates to true, this profile is considered compatible with the active print profile.

**Key:** `compatible_prints_condition`

**Type:** `string`

**Default:** `null`

### Example

```json
"compatible_prints_condition": ""
```

**Note:** There are currently no built-in profiles that use this setting.

## Fan speed

Speed of exhuast fan after printing completes

**Key:** `complete_print_exhaust_fan_speed`

**Type:** `[integer]`

**Default:** `80`

**Max:** `100`

**Min:** `0`

### Example

```json
"complete_print_exhaust_fan_speed": ["70"]
```

## Bed temperature

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the Cool Plate

**Key:** `cool_plate_temp`

**Type:** `[integer]`

**Default:** `35`

**Max:** `300`

**Min:** `0`

### Example

```json
"cool_plate_temp": ["60"]
```

## Initial layer bed temperature

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the Cool Plate

**Key:** `cool_plate_temp_initial_layer`

**Type:** `[integer]`

**Default:** `35`

**Max:** `120`

**Min:** `0`

### Example

```json
"cool_plate_temp": ["60"]
```

## Default color

Default filament color

**Key:** `default_filament_colour`

**Type:** `[string]`

**Default:** `[]`

### Example

```json
"default_filament_colour": [""]
```

**Note:** There are currently no built-in profiles that use this setting.

## Fan speed

Speed of exhuast fan during printing.This speed will overwrite the speed in filament custom gcode

**Key:** `during_print_exhaust_fan_speed`

**Type:** `[integer]`

**Default:** `60`

**Max:** `100`

**Min:** `0`

### Example

```json
"during_print_exhaust_fan_speed": ["70"]
```

## Force cooling for overhang and bridge

Enable this option to optimize part cooling fan speed for overhang and bridge to get better cooling

**Key:** `enable_overhang_bridge_fan`

**Type:** `[boolean]`

**Default:** `true`

### Example

```json
"enable_overhang_bridge_fan": ["1"]
```

## Enable pressure advance

Enable pressure advance, auto calibration result will be overwriten once enabled.

**Key:** `enable_pressure_advance`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"enable_pressure_advance": ["1"]
```

## Bed temperature

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the Engineering Plate

**Key:** `eng_plate_temp`

**Type:** `[integer]`

**Default:** `45`

**Max:** `300`

**Min:** `0`

### Example

```json
"eng_plate_temp": ["60"]
```

## Initial layer bed temperature

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the Engineering Plate

**Key:** `eng_plate_temp_initial_layer`

**Type:** `[integer]`

**Default:** `45`

**Max:** `300`

**Min:** `0`

### Example

```json
"eng_plate_temp_initial_layer": ["60"]
```

## Layer time

Part cooling fan will be enabled for layers of which estimated time is shorter than this value. Fan speed is interpolated between the minimum and maximum fan speeds according to layer printing time

**Key:** `fan_cooling_layer_time`

**Type:** `[float]`

**Default:** `60.0`

**Max:** `1000`

**Min:** `0`

### Example

```json
"fan_cooling_layer_time": ["35"]
```

## Max fan speed

Part cooling fan speed may be increased when auto cooling is enabled. This is the maximum speed limitation of part cooling fan

**Key:** `fan_max_speed`

**Type:** `[integer]`

**Default:** `100`

**Max:** `100`

**Min:** `0`

### Example

```json
"fan_max_speed": ["80"]
```

## Min fan speed

Minimum speed for part cooling fan

**Key:** `fan_min_speed`

**Type:** `[integer]`

**Default:** `20`

**Max:** `100`

**Min:** `0`

### Example

```json
"fan_min_speed": ["5"]
```

## Color

Only used as a visual help on UI

**Key:** `filament_colour`

**Type:** `[string]`

**Default:** `#F2754E`

### Example

```json
"filament_colour": [""]
```

**Note:** There are currently no built-in profiles that use this setting.

## Speed of the last cooling move

Cooling moves are gradually accelerating towards this speed.

**Key:** `filament_cooling_final_speed`

**Type:** `[float]`

**Default:** `3.4`

**Min:** `0`

### Example

```json
"filament_cooling_final_speed": ["3.4"]
```

## Speed of the first cooling move

Cooling moves are gradually accelerating beginning at this speed.

**Key:** `filament_cooling_initial_speed`

**Type:** `[float]`

**Default:** `2.2`

**Min:** `0`

### Example

```json
"filament_cooling_final_speed": ["2.2"]
```

## Number of cooling moves

Filament is cooled by being moved back and forth in the cooling tubes. Specify desired number of these moves.

**Key:** `filament_cooling_moves`

**Type:** `[integer]`

**Default:** `4`

**Max:** `20`

### Example

```json
"filament_cooling_moves": ["4"]
```

## Price

Filament price. For statistics only

**Key:** `filament_cost`

**Type:** `[float]`

**Default:** `0.0`

**Min:** `0`

### Example

```json
"filament_cost": ["24.99"]
```

## Density

Filament density. For statistics only

**Key:** `filament_density`

**Type:** `[float]`

**Default:** `0.0`

**Min:** `0`

### Example

```json
"filament_density": ["1.04"]
```

## Deretraction Speed

Speed for reloading filament into extruder. Zero means same speed with retraction

**Key:** `filament_deretraction_speed`

**Type:** `[float]`

**Default:** `0.0`

### Example

```json
"filament_deretraction_speed": ["nil"]
```

**Note:** All built-in profiles using this setting have it set to `["nil"]`

## Diameter

Filament diameter is used to calculate extrusion in gcode, so it's important and should be accurate

**Key:** `filament_diameter`

**Type:** `[float]`

**Default:** `1.75`

**Min:** `0`

### Example

```json
"filament_diameter": ["1.75"]
```

## End G-code

End G-code when finish the printing of this filament

**Key:** `filament_end_gcode`

**Type:** `[string]`

**Default:** ` `

### Example

```json
"filament_end_gcode": ["; filament end gcode \nM106 P3 S0\n"]
```

## Flow ratio

The material may have volumetric change after switching between molten state and crystalline state. This setting changes all extrusion flow of this filament in gcode proportionally. Recommended value range is between 0.95 and 1.05. Maybe you can tune this value to get nice flat surface when there has slight overflow or underflow

**Key:** `filament_flow_ratio`

**Type:** `[float]`

**Default:** `1.0`

**Max:** `2`

### Example

```json
"filament_flow_ratio": ["0.94"]
```

## Support material

Support material is commonly used to print support and support interface

**Key:** `filament_is_support`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"filament_is_support": ["1"]
```

## Filament load time

Time for the printer firmware (or the Multi Material Unit 2.0) to load a new filament during a tool change (when executing the T code). This time is added to the total print time by the G-code time estimator.

**Key:** `filament_load_time`

**Type:** `[float]`

**Default:** `0.0`

**Min:** `0`

### Example

```json
"filament_is_support": ["0"]
```

## Loading speed

Speed used for loading the filament on the wipe tower.

**Key:** `filament_loading_speed`

**Type:** `[float]`

**Default:** `28.0`

**Min:** `0`

### Example

```json
"filament_loading_speed": ["28"]
```

## Loading speed at the start

Speed used at the very beginning of loading phase.

**Key:** `filament_loading_speed_start`

**Type:** `[float]`

**Default:** `3.0`

**Min:** `0`

### Example

```json
"filament_loading_speed_start": ["3"]
```

## Max volumetric speed

This setting stands for how much volume of filament can be melted and extruded per second. Printing speed is limited by max volumetric speed, in case of too high and unreasonable speed setting. Can't be zero

**Key:** `filament_max_volumetric_speed`

**Type:** `[float]`

**Default:** `2.0`

**Max:** `200`

**Min:** `0`

### Example

```json
"filament_max_volumetric_speed": ["12"]
```

## Minimal purge on wipe tower

After a tool change, the exact position of the newly loaded filament inside the nozzle may not be known, and the filament pressure is likely not yet stable. Before purging the print head into an infill or a sacrificial object, Slic3r will always prime this amount of material into the wipe tower to produce successive infill or sacrificial object extrusions reliably.

**Key:** `filament_minimal_purge_on_wipe_tower`

**Type:** `[float]`

**Default:** `15.0`

**Min:** `0`

### Example

```json
"filament_minimal_purge_on_wipe_tower": ["15"]
```

## Enable ramming for multitool setups

Perform ramming when using multitool printer (i.e. when the 'Single Extruder Multimaterial' in Printer Settings is unchecked). When checked, a small amount of filament is rapidly extruded on the wipe tower just before the toolchange. This option is only used when the wipe tower is enabled.

**Key:** `filament_multitool_ramming`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"filament_multitool_ramming": ["0"]
```

## Multitool ramming flow

Flow used for ramming the filament before the toolchange.

**Key:** `filament_multitool_ramming_flow`

**Type:** `[float]`

**Default:** `10.0`

**Min:** `0`

### Example

```json
"filament_multitool_ramming_flow": ["10"]
```

## Multitool ramming volume

The volume to be rammed before the toolchange.

**Key:** `filament_multitool_ramming_volume`

**Type:** `[float]`

**Default:** `10.0`

**Min:** `0`

### Example

```json
"filament_multitool_ramming_volume": ["10"]
```

## Filament notes

You can put your notes regarding the filament here.

**Key:** `filament_notes`

**Type:** `[string]`

**Default:** ``

### Example

```json
"filament_notes": [""]
```

## Ramming parameters

This string is edited by RammingDialog and contains ramming specific parameters.

**Key:** `filament_ramming_parameters`

**Type:** `[string]`

**Default:** `["120 100 6.6 6.8 7.2 7.6 7.9 8.2 8.7 9.4 9.9 10.0|0.05 6.6 0.45 6.8 0.95 7.8 1.45 8.3 1.95 9.7 2.45 10 2.95 7.6 3.45 7.6 3.95 7.6 4.45 7.6 4.95 7.6"]`

### Example

```json
"filament_ramming_parameters": ["120 100 6.6 6.8 7.2 7.6 7.9 8.2 8.7 9.4 9.9 10.0| 0.05 6.6 0.45 6.8 0.95 7.8 1.45 8.3 1.95 9.7 2.45 10 2.95 7.6 3.45 7.6 3.95 7.6 4.45 7.6 4.95 7.6"]
```

## Retract amount before wipe

The length of fast retraction before wipe, relative to retraction length

**Key:** `filament_retract_before_wipe`

**Type:** `[percent]`

**Default:** `100`

### Example

```json
"filament_retract_before_wipe": ["nil"]
```

**Note:** All built-in profiles using this setting have it set to `["nil"]`

## Only lift Z above

If you set this to a positive value, Z lift will only take place above the specified absolute Z.

**Key:** `filament_retract_lift_above`

**Type:** `[float]`

**Default:** `0.0`

### Example

```json
"filament_retract_lift_above": ["nil"]
```

**Note:** All built-in profiles using this setting have it set to `["nil"]`

## Only lift Z below

If you set this to a positive value, Z lift will only take place below the specified absolute Z.

**Key:** `filament_retract_lift_below`

**Type:** `[float]`

**Default:** `0.0`

### Example

```json
"filament_retract_lift_below": ["nil"]
```

**Note:** All built-in profiles using this setting have it set to `["nil"]`

## On surfaces

Enforce Z Hop behavior. This setting is impacted by the above settings (Only lift Z above/below).

**Key:** `filament_retract_lift_enforce`

**Type:** `[enum]`

**Default:** `All Surfaces`

**Values:**
* **All Surfaces**: `All Surfaces`
* **Top Only**: `Top Only`
* **Bottom Only**: `Bottom Only`
* **Top and Bottom**: `Top and Bottom`

### Example

```json
"filament_retract_lift_enforce": ["nil"]
```

**Note:** All built-in profiles using this setting have it set to `["nil"]`

## Extra length on restart

When the retraction is compensated after the travel move, the extruder will push this additional amount of filament. This setting is rarely needed.

**Key:** `filament_retract_restart_extra`

**Type:** `[float]`

**Default:** `0.0`

### Example

```json
"filament_retract_restart_extra": ["nil"]
```

**Note:** All built-in profiles using this setting have it set to `["nil"]`

## Retract when change layer

Force a retraction when changes layer

**Key:** `filament_retract_when_changing_layer`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"filament_retract_when_changing_layer": ["nil"]
```

**Note:** All built-in profiles using this setting have it set to `["nil"]`

## Retraction Length

Some amount of material in extruder is pulled back to avoid ooze during long travel. Set zero to disable retraction

**Key:** `filament_retraction_length`

**Type:** `[float]`

**Default:** `0.8`

### Example

```json
"filament_retraction_length": ["0.4"]
```

## Travel distance threshold

Only trigger retraction when the travel distance is longer than this threshold

**Key:** `filament_retraction_minimum_travel`

**Type:** `[float]`

**Default:** `2.0`

### Example

```json
"filament_retraction_minimum_travel": ["1.0"]
```

## Retraction Speed

Speed of retractions

**Key:** `filament_retraction_speed`

**Type:** `[float]`

**Default:** `30.0`

### Example

```json
"filament_retraction_minimum_travel": ["25.0"]
```

## Seam gap

In order to reduce the visibility of the seam in a closed loop extrusion, the loop is interrupted and shortened by a specified amount.
This amount can be specified in millimeters or as a percentage of the current extruder diameter. The default value for this parameter is 10%.

**Key:** `filament_seam_gap`

**Type:** `float`, `percent`

**Default:** `10%`

**Min:** `0`

### Example

```json
"filament_seam_gap": "5%"
```

**Note:** There are currently no built-in profiles that use this setting.

## Shrinkage

Enter the shrinkage percentage that the filament will get after cooling (94% if you measure 94mm instead of 100mm). The part will be scaled in xy to compensate. Only the filament used for the perimeter is taken into account.
Be sure to allow enough space between objects, as this compensation is done after the checks.

**Key:** `filament_shrink`

**Type:** `[percent]`

**Default:** `100%`

**Min:** `10`

### Example

```json
"filament_shrink": ["105%"]
```

## Soluble material

Soluble material is commonly used to print support and support interface

**Key:** `filament_soluble`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"filament_soluble": ["1"]
```

## Start G-code

Start G-code when start the printing of this filament

**Key:** `filament_start_gcode`

**Type:** `[string]`

**Default:** ` `

### Example

```json
"filament_start_gcode": ["; filament start gcode\n;right_extruder_material:HS PLA\n"]
```

## Delay after unloading

Time to wait after the filament is unloaded. May help to get reliable toolchanges with flexible materials that may need more time to shrink to original dimensions.

**Key:** `filament_toolchange_delay`

**Type:** `[float]`

**Default:** `0.0`

**Min:** `0`

### Example

```json
"filament_toolchange_delay": ["0"]
```

## Type

The material type of filament

**Key:** `filament_type`

**Type:** `[string]`

**Default:** `PLA`

**Values:**
* `PLA`
* `ABS`
* `ASA`
* `PETG`
* `TPU`
* `PC`
* `PA`
* `PA-CF`
* `PA6-CF`
* `PLA-CF`
* `PET-CF`
* `PETG-CF`
* `PVA`
* `HIPS`
* `PLA-AERO`
* `PPS`
* `PPS-CF`
* `PPA-CF`
* `PPA-GF`

### Example

```json
"filament_type": ["PLA"]
```

## Filament unload time

Time for the printer firmware (or the Multi Material Unit 2.0) to unload a filament during a tool change (when executing the T code). This time is added to the total print time by the G-code time estimator.

**Key:** `filament_unload_time`

**Type:** `[float]`

**Default:** `0.0`

**Min:** `0`

### Example

```json
"filament_unload_time": ["0"]
```

## Unloading speed

Speed used for unloading the filament on the wipe tower (does not affect initial part of unloading just after ramming).

**Key:** `filament_unloading_speed`

**Type:** `[float]`

**Default:** `90.0`

**Min:** `0`

### Example

```json
"filament_unloading_speed": ["100"]
```

## Unloading speed at the start

Speed used for unloading the tip of the filament immediately after ramming.

**Key:** `filament_unloading_speed_start`

**Type:** `[float]`

**Default:** `100.0`

**Min:** `0`

### Example

```json
"filament_unloading_speed_start": ["100"]
```

## Vendor

Vendor of filament. For show only

**Key:** `filament_vendor`

**Type:** `[string]`

**Default:** `(Undefined)`

### Example

```json
"filament_vendor": ["Generic"]
```

## Wipe while retracting

Move nozzle along the last extrusion path when retracting to clean leaked material on nozzle. This can minimize blob when print new part after travel

**Key:** `filament_wipe`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"filament_wipe": ["1"]
```

## Wipe Distance

Discribe how long the nozzle will move along the last path when retracting

**Key:** `filament_wipe_distance`

**Type:** `[float]`

**Default:** `1.0`

**Min:** `0`

### Example

```json
"filament_wipe_distance": ["1.5"]
```

## Z hop when retract

Whenever the retraction is done, the nozzle is lifted a little to create clearance between nozzle and the print. It prevents nozzle from hitting the print when travel move. Using spiral line to lift z can prevent stringing

**Key:** `filament_z_hop`

**Type:** `[float]`

**Default:** `0.4`

### Example

```json
"filament_z_hop": ["0.8"]
```

## Z hop type

Z hop type

**Key:** `filament_z_hop_types`

**Type:** `[enum]`

**Default:** `Normal`

**Values:**
* **Auto**: `Auto Lift`
* **Normal**: `Normal Lift`
* **Slope**: `Slope Lift`
* **Spiral**: `Spiral Lift`

### Example

```json
"filament_z_hop_types": ["Spiral Lift"]
```

## Full fan speed at layer

Fan speed will be ramped up linearly from zero at layer "close_fan_the_first_x_layers" to maximum at layer "full_fan_speed_layer". "full_fan_speed_layer" will be ignored if lower than "close_fan_the_first_x_layers", in which case the fan will be running at maximum allowed speed at layer "close_fan_the_first_x_layers" + 1.

**Key:** `full_fan_speed_layer`

**Type:** `[integer]`

**Default:** `0`

**Max:** `1000`

**Min:** `0`

### Example

```json
"full_fan_speed_layer": ["2"]
```

## Bed temperature

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the High Temp Plate

**Key:** `hot_plate_temp`

**Type:** `[integer]`

**Default:** `45`

**Max:** `300`

**Min:** `0`

### Example

```json
"hot_plate_temp": ["60"]
```

## Initial layer bed temperature

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the High Temp Plate

**Key:** `hot_plate_temp_initial_layer`

**Type:** `[integer]`

**Default:** `45`

**Max:** `300`

### Example

```json
"hot_plate_temp_initial_layer": ["60"]
```

## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `string`

**Default:** `null`

### Example

```json
"inherits": ["fdm_filament_pla"]
```

## Nozzle temperature

Nozzle temperature for layers after the initial one

**Key:** `nozzle_temperature`

**Type:** `[integer]`

**Default:** `200`

**Max:** `max_temp`

**Min:** `0`

### Example

```json
"nozzle_temperature": ["210"]
```

## Initial layer nozzle temperature

Nozzle temperature to print initial layer when using this filament

**Key:** `nozzle_temperature_initial_layer`

**Type:** `[integer]`

**Default:** `200`

**Max:** `max_temp`

**Min:** `0`

### Example

```json
"nozzle_temperature": ["215"]
```

## Max

**Key:** `nozzle_temperature_range_high`

**Type:** `[integer]`

**Default:** `240`

**Max:** `max_temp`

**Min:** `0`

### Example

```json
"nozzle_temperature": ["230"]
```

## Min

**Key:** `nozzle_temperature_range_low`

**Type:** `[integer]`

**Default:** `190`

**Max:** `max_temp`

**Min:** `0`

### Example

```json
"nozzle_temperature": ["180"]
```

## Fan speed for overhang

Force part cooling fan to be this speed when printing bridge or overhang wall which has large overhang degree. Forcing cooling for overhang and bridge can get better quality for these part

**Key:** `overhang_fan_speed`

**Type:** `[integer]`

**Default:** `100`

**Max:** `100`

**Min:** `0`

### Example

```json
"overhang_fan_speed": ["80"]
```

## Cooling overhang threshold

Force cooling fan to be specific speed when overhang degree of printed part exceeds this value. Expressed as percentage which indicides how much width of the line without support from lower layer. 0% means forcing cooling for all outer wall no matter how much overhang degree

**Key:** `overhang_fan_threshold`

**Type:** `[enum]`

**Default:** `95%`

**Values:**
* **0%**: `0%`
* **10%**: `10%`
* **25%**: `25%`
* **50%**: `50%`
* **75%**: `75%`
* **95%**: `95%`

### Example

```json
"overhang_fan_speed": ["95%"]
```

## Pressure advance

Pressure advance(Klipper) AKA Linear advance factor(Marlin)

**Key:** `pressure_advance`

**Type:** `[float]`

**Default:** `0.02`

**Max:** `2`

### Example

```json
"pressure_advance": ["0.025"]
```

## Keep fan always on

If enable this setting, part cooling fan will never be stoped and will run at least at minimum speed to reduce the frequency of starting and stoping

**Key:** `reduce_fan_stop_start_freq`

**Type:** `[boolean]`

**Default:** `null`

### Example

```json
"reduce_fan_stop_start_freq": ["1"]
```

## Required nozzle HRC

Minimum HRC of nozzle required to print the filament. Zero means no checking of nozzle's HRC.

**Key:** `required_nozzle_HRC`

**Type:** `[integer]`

**Default:** `0`

**Max:** `500`

**Min:** `0`

### Example

```json
"required_nozzle_HRC": ["40"]
```

## Slow printing down for better layer cooling

Enable this option to slow printing speed down to make the final layer time not shorter than the layer time threshold in "Max fan speed threshold", so that layer can be cooled for longer time. This can improve the cooling quality for needle and small details

**Key:** `slow_down_for_layer_cooling`

**Type:** `[boolean]`

**Default:** `true`

### Example

```json
"slow_down_for_layer_cooling": ["1"]
```

## Layer time

The printing speed in exported gcode will be slowed down, when the estimated layer time is shorter than this value, to get better cooling for these layers

**Key:** `slow_down_layer_time`

**Type:** `[float]`

**Default:** `5.0`

**Max:** `1000`

**Min:** `0`

### Example

```json
"slow_down_layer_time": ["3"]
```

## Min print speed

The minimum printing speed for the filament when slow down for better layer cooling is enabled, when printing overhangs and when feature speeds are not specified explicitly.

**Key:** `slow_down_min_speed`

**Type:** `[float]`

**Default:** `10.0`

**Min:** `0`

### Example

```json
"slow_down_min_speed": ["10"]
```

## Support interface fan speed

This fan speed is enforced during all support interfaces, to be able to weaken their bonding with a high fan speed.
Set to -1 to disable this override.
Can only be overriden by disable_fan_first_layers.

**Key:** `support_material_interface_fan_speed`

**Type:** `[integer]`

**Default:** `-1`

**Max:** `100`

**Min:** `-1`

### Example

```json
"support_material_interface_fan_speed": ["100"]
```

## Softening temperature

The material softens at this temperature, so when the bed temperature is equal to or greater than it, it's highly recommended to open the front door and/or remove the upper glass to avoid cloggings.

**Key:** `temperature_vitrification`

**Type:** `[integer]`

**Default:** `100`

### Example

```json
"temperature_vitrification": ["80"]
```

## Other layers

Bed temperature for layers except the initial one. Value 0 means the filament does not support to print on the Textured PEI Plate

**Key:** `textured_plate_temp`

**Type:** `[integer]`

**Default:** `45`

**Max:** `300`

**Min:** `0`

### Example

```json
"textured_plate_temp": ["60"]
```

## Initial layer

Bed temperature of the initial layer. Value 0 means the filament does not support to print on the Textured PEI Plate

**Key:** `textured_plate_temp_initial_layer`

**Type:** `[integer]`

**Default:** `45`

**Max:** `300`

**Min:** `0`

### Example

```json
"textured_plate_temp_initial_layer": ["60"]
```

