---
layout: default
title: "Machine"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "Machine"
---

Configuration options for a configuration file with `"type": "machine"`.

## Auxiliary part cooling fan

Enable this option if machine has auxiliary part cooling fan. G-code command: M106 P2 S(0-255).

**Key:** `auxiliary_fan`

**Type:** `Bool`

**Default** `false`

### Example

```json
"auxiliary_fan": false
```


## Show auto-calibration marks

[No documentation provided]

**Key:** `bbl_calib_mark_logo`

**Type:** `Bool`

**Default** `true`

### Example

```json
"bbl_calib_mark_logo": true
```


## Before layer change G-code

This G-code is inserted at every layer change before lifting z

**Key:** `before_layer_change_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"before_layer_change_gcode": "; before layer [layer_num] change\n{if layer_z <= initial_layer_print_height + layer_height * 2}\nM109 T1 S{nozzle_temperature_initial_layer[1]}\nM140 S[bed_temperature_initial_layer_single]\n{else}\nM109 T1 S{nozzle_temperature[1]}\nM140 S{bed_temperature[1]}\n{endif}\n{if (filament_type[0] ==\"PLA\" or filament_type[0] ==\"PETG\")}\n{if layer_z >= initial_layer_print_height + layer_height * 2}\nM106 P2 S150\n{elsif layer_z >= initial_layer_print_height + layer_height * 1}\nM106 P2 S100\n{else}\nM106 P2 S0\n{endif}\n{endif}"
```


## Best object position

Best auto arranging position in range [0,1] w.r.t. bed shape.

**Key:** `best_object_pos`

**Type:** `Point`

**Default** `[0.5, 0.5]`

### Example

```json
"best_object_pos": "0.7x0.5"
```


## Change filament G-code

This gcode is inserted when change filament, including T command to trigger tool change

**Key:** `change_filament_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"change_filament_gcode": "M600\nG1 E0.4 F1500 ; prime after color change"
```


## Cooling tube length

Length of the cooling tube to limit space for cooling moves inside it.

**Key:** `cooling_tube_length`

**Type:** `Float`

**Min:** `0`

**Default** `5.0`

### Example

```json
"cooling_tube_length": 5
```


## Cooling tube position

Distance of the center-point of the cooling tube from the extruder tip.

**Key:** `cooling_tube_retraction`

**Type:** `Float`

**Min:** `0`

**Default** `91.5`

### Example

```json
"cooling_tube_retraction": 30
```


## Default filament profile

Default filament profile when switch to this machine profile

**Key:** `default_filament_profile`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"default_filament_profile": "DeltiQ - PLA - ExtraFill (Fillamentum) @0.25 nozzle"
```


## Default process profile

Default process profile when switch to this machine profile

**Key:** `default_print_profile`

**Type:** `String`

**Default** ``

### Example

```json
"default_print_profile": "0.20mm Standard @Elegoo Neptune4 (0.2 nozzle)"
```


## Deretraction speed

Speed for reloading filament into extruder. Zero means same speed with retraction

**Key:** `deretraction_speed`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"deretraction_speed": [0]
```


## Enable filament ramming

Enable filament ramming

**Key:** `enable_filament_ramming`

**Type:** `Bool`

**Default** `true`

### Example

```json
"enable_filament_ramming": false
```


## Extra loading distance

When set to zero, the distance the filament is moved from parking position during load is exactly the same as it was moved back during unload. When positive, it is loaded further,  if negative, the loading move is shorter than unloading.

**Key:** `extra_loading_move`

**Type:** `Float`

**Default** `-2.0`

### Example

```json
"extra_loading_move": -25
```


## Height to lid

Distance of the nozzle tip to the lid. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_lid`

**Type:** `Float`

**Min:** `0`

**Default** `120`

### Example

```json
"extruder_clearance_height_to_lid": 140
```


## Height to rod

Distance of the nozzle tip to the lower rod. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_rod`

**Type:** `Float`

**Min:** `0`

**Default** `40`

### Example

```json
"extruder_clearance_height_to_rod": 44
```


## Extruder Color

Only used as a visual help on UI

**Key:** `extruder_colour`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"extruder_colour": ["#FCE94F"]
```


## Extruder offset

If your firmware doesn't handle the extruder displacement you need the G-code to take it into account. This option lets you specify the displacement of each extruder with respect to the first one. It expects positive coordinates (they will be subtracted from the XY coordinate).

**Key:** `extruder_offset`

**Type:** `Points`

**Default** `[[0, 0]]`

### Example

```json
"extruder_offset": "0x0,0x0,0x0,0x0,0x0"
```


## Fan kick-start time

Emit a max fan speed command for this amount of seconds before reducing to target speed to kick-start the cooling fan.
This is useful for fans where a low PWM/power may be insufficient to get the fan started spinning from a stop, or to get the fan up to speed faster.
Set to 0 to deactivate.

**Key:** `fan_kickstart`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"fan_kickstart": 0
```


## Only overhangs

Will only take into account the delay for the cooling of overhangs.

**Key:** `fan_speedup_overhangs`

**Type:** `Bool`

**Default** `true`

### Example

```json
"fan_speedup_overhangs": false
```


## Fan speed-up time

Start the fan this number of seconds earlier than its target start time (you can use fractional seconds). It assumes infinite acceleration for this time estimation, and will only take into account G1 and G0 moves (arc fitting is unsupported).

**Key:** `fan_speedup_time`

**Type:** `Float`

**Default** `0`

### Example

```json
"fan_speedup_time": 0
```


## G-code flavor

What kind of gcode the printer is compatible with

**Key:** `gcode_flavor`

**Type:** `Enum`

**Default** `MarlinLegacy`

**Enum values:**


### Example

```json
"gcode_flavor": "repetier"
```


## High extruder current on filament swap

It may be beneficial to increase the extruder motor current during the filament exchange sequence to allow for rapid ramming feed rates and to overcome resistance when loading a filament with an ugly shaped tip.

**Key:** `high_current_on_filament_swap`

**Type:** `Bool`

**Default** `false`

### Example

```json
"high_current_on_filament_swap": false
```


## Host Type

Slic3r can upload G-code files to a printer host. This field must contain the kind of the host.

**Key:** `host_type`

**Type:** `Enum`

**Default** `OctoPrint`

**Enum values:**


### Example

```json
"host_type": "prusalink"
```


## Layer change G-code

This gcode part is inserted at every layer change after lift z

**Key:** `layer_change_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"layer_change_gcode": "; layer num/total_layer_count: {layer_num+1}/[total_layer_count]\nM622.1 S1 ; for prev firware, default turned on\nM1002 judge_flag timelapse_record_flag\nM622 J1\n{if timelapse_type == 0} ; timelapse without wipe tower\nM971 S11 C10 O0\n{elsif timelapse_type == 1} ; timelapse with wipe tower\nG92 E0\nG1 E-[retraction_length] F1800\nG17\nG2 Z{layer_z + 0.4} I0.86 J0.86 P1 F20000 ; spiral lift a little\nG1 X65 Y245 F20000 ; move to safe pos\nG17\nG2 Z{layer_z} I0.86 J0.86 P1 F20000\nG1 Y265 F3000\nM400 P300\nM971 S11 C11 O0\nG92 E0\nG1 E[retraction_length] F300\nG1 X100 F5000\nG1 Y255 F20000\n{endif}\nM623\n; update layer progress\nM73 L{layer_num+1}\nM991 S0 P{layer_num} ;notify layer change"
```


## End G-code

End G-code when finish the whole printing

**Key:** `machine_end_gcode`

**Type:** `String`

**Default** `M104 S0 ; turn off temperature\nG28 X0  ; home X axis\nM84     ; disable motors\n`

### Example

```json
"machine_end_gcode": "G1 E-1 F2100 ; retract\n{if max_layer_z < max_print_height}G1 Z{z_offset+min(max_layer_z+2, max_print_height)} F720 ; Move print head up{endif}\nG1 X178 Y178 F4200 ; park print head\n{if max_layer_z < max_print_height}G1 Z{z_offset+min(max_layer_z+30, max_print_height)} F720 ; Move print head further up{endif}\nG4 ; wait\nM104 S0 ; turn off temperature\nM140 S0 ; turn off heatbed\nM107 ; turn off fan\nM221 S100 ; reset flow\nM900 K0 ; reset LA\nM84 ; disable motors\n; max_layer_z = [max_layer_z]"
```


## Filament load time

Time to load new filament when switch filament. For statistics only

**Key:** `machine_load_filament_time`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"machine_load_filament_time": 17
```


## Maximum acceleration E

Maximum acceleration of E axis

**Key:** `machine_max_acceleration_e`

**Type:** `Floats`

**Min:** `0`

**Default** `[5000.0, 5000.0]`

### Example

```json
"machine_max_acceleration_e": [
    3000,
    800
  ]
```


## Maximum acceleration for extruding

Maximum acceleration for extruding (M204 P)

**Key:** `machine_max_acceleration_extruding`

**Type:** `Floats`

**Min:** `0`

**Default** `[1500.0, 1250.0]`

### Example

```json
"machine_max_acceleration_extruding": [10000]
```


## Maximum acceleration for retracting

Maximum acceleration for retracting (M204 R)

**Key:** `machine_max_acceleration_retracting`

**Type:** `Floats`

**Min:** `0`

**Default** `[1500.0, 1250.0]`

### Example

```json
"machine_max_acceleration_retracting": [
    10000,
    10000
  ]
```


## Maximum acceleration for travel

Maximum acceleration for travel (M204 T), it only applies to Marlin 2

**Key:** `machine_max_acceleration_travel`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0, 0.0]`

### Example

```json
"machine_max_acceleration_travel": "9000,1250"
```


## Maximum acceleration X

Maximum acceleration of X axis

**Key:** `machine_max_acceleration_x`

**Type:** `Floats`

**Min:** `0`

**Default** `[1000.0, 1000.0]`

### Example

```json
"machine_max_acceleration_x": 1500
```


## Maximum acceleration Y

Maximum acceleration of Y axis

**Key:** `machine_max_acceleration_y`

**Type:** `Floats`

**Min:** `0`

**Default** `[1000.0, 1000.0]`

### Example

```json
"machine_max_acceleration_y": [
    2500,
    2500
  ]
```


## Maximum acceleration Z

Maximum acceleration of Z axis

**Key:** `machine_max_acceleration_z`

**Type:** `Floats`

**Min:** `0`

**Default** `[500.0, 200.0]`

### Example

```json
"machine_max_acceleration_z": [
    300,
    200
  ]
```


## Maximum jerk E

Maximum jerk of E axis

**Key:** `machine_max_jerk_e`

**Type:** `Floats`

**Min:** `0`

**Default** `[2.5, 2.5]`

### Example

```json
"machine_max_jerk_e": [
    15,
    4.5
  ]
```


## Maximum jerk X

Maximum jerk of X axis

**Key:** `machine_max_jerk_x`

**Type:** `Floats`

**Min:** `0`

**Default** `[10.0, 10.0]`

### Example

```json
"machine_max_jerk_x": [
    7,
    7
  ]
```


## Maximum jerk Y

Maximum jerk of Y axis

**Key:** `machine_max_jerk_y`

**Type:** `Floats`

**Min:** `0`

**Default** `[10.0, 10.0]`

### Example

```json
"machine_max_jerk_y": "4, 4"
```


## Maximum jerk Z

Maximum jerk of Z axis

**Key:** `machine_max_jerk_z`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.2, 0.4]`

### Example

```json
"machine_max_jerk_z": "0.4, 0.4"
```


## Maximum speed E

Maximum speed of E axis

**Key:** `machine_max_speed_e`

**Type:** `Floats`

**Min:** `0`

**Default** `[120.0, 120.0]`

### Example

```json
"machine_max_speed_e": [
    80,
    80
  ]
```


## Maximum speed X

Maximum speed of X axis

**Key:** `machine_max_speed_x`

**Type:** `Floats`

**Min:** `0`

**Default** `[500.0, 200.0]`

### Example

```json
"machine_max_speed_x": [
    200,
    200
  ]
```


## Maximum speed Y

Maximum speed of Y axis

**Key:** `machine_max_speed_y`

**Type:** `Floats`

**Min:** `0`

**Default** `[500.0, 200.0]`

### Example

```json
"machine_max_speed_y": [
    200,
    200
  ]
```


## Maximum speed Z

Maximum speed of Z axis

**Key:** `machine_max_speed_z`

**Type:** `Floats`

**Min:** `0`

**Default** `[12.0, 12.0]`

### Example

```json
"machine_max_speed_z": [
    5,
    12
  ]
```


## Minimum speed for extruding

Minimum speed for extruding (M205 S)

**Key:** `machine_min_extruding_rate`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0, 0.0]`

### Example

```json
"machine_min_extruding_rate": 0
```


## Minimum travel speed

Minimum travel speed (M205 T)

**Key:** `machine_min_travel_rate`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0, 0.0]`

### Example

```json
"machine_min_travel_rate": [0]
```


## Pause G-code

This G-code will be used as a code for the pause print. User can insert pause G-code in gcode viewer

**Key:** `machine_pause_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"machine_pause_gcode": "M400 U1"
```


## Start G-code

Start G-code when start the whole printing

**Key:** `machine_start_gcode`

**Type:** `String`

**Default** `G28 ; home all axes\nG1 Z5 F5000 ; lift nozzle\n`

### Example

```json
"machine_start_gcode": "G90 ; use absolute coordinates\nM83 ; extruder relative mode\nM104 S[nozzle_temperature_initial_layer] ; set extruder temp\nM140 S[bed_temperature_initial_layer_single] ; set bed temp\nM190 S[bed_temperature_initial_layer_single] ; wait for bed temp\nM109 S[nozzle_temperature_initial_layer] ; wait for extruder temp\nG28 ; home all\nG1 Z2 F240\nG1 X2 Y10 F3000\nG1 Z0.28 F240\nG92 E0\nG1 Y190 E15 F1500 ; intro line\nG1 X2.3 F5000\nG92 E0\nG1 Y10 E15 F1200 ; intro line\nG92 E0"
```


## Filament unload time

Time to unload old filament when switch filament. For statistics only

**Key:** `machine_unload_filament_time`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"machine_unload_filament_time": 0
```


## Manual Filament Change

Enable this option to omit the custom Change filament G-code only at the beginning of the print. The tool change command (e.g., T0) will be skipped throughout the entire print. This is useful for manual multi-material printing, where we use M600/PAUSE to trigger the manual filament change action.

**Key:** `manual_filament_change`

**Type:** `Bool`

**Default** `false`

### Example

```json
"manual_filament_change": true
```


## Layer height (max)

The largest printable layer height for extruder. Used tp limits the maximum layer hight when enable adaptive layer height

**Key:** `max_layer_height`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0]`

### Example

```json
"max_layer_height": [0.36]
```


## Layer height (min)

The lowest printable layer height for extruder. Used tp limits the minimum layer hight when enable adaptive layer height

**Key:** `min_layer_height`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.07]`

### Example

```json
"min_layer_height": 0.025
```


## Nozzle HRC

The nozzle's hardness. Zero means no checking for nozzle's hardness during slicing.

**Key:** `nozzle_hrc`

**Type:** `Int`

**Min:** `0`

**Max:** `500`

**Default** `0`

### Example

```json
"nozzle_hrc": 0
```


## Nozzle type

The metallic material of nozzle. This determines the abrasive resistance of nozzle, and what kind of filament can be printed

**Key:** `nozzle_type`

**Type:** `Enum`

**Default** `Undefine`

**Enum values:**


### Example

```json
"nozzle_type": "undefine"
```


## Nozzle volume

Volume of nozzle between the cutter and the end of nozzle

**Key:** `nozzle_volume`

**Type:** `Float`

**Default** `0.0`

### Example

```json
"nozzle_volume": 32
```


## Filament parking position

Distance of the extruder tip from the position where the filament is parked when unloaded. This should match the value in printer firmware.

**Key:** `parking_pos_retraction`

**Type:** `Float`

**Min:** `0`

**Default** `92.0`

### Example

```json
"parking_pos_retraction": 92
```


## Hostname, IP or URL

Slic3r can upload G-code files to a printer host. This field should contain the hostname, IP address or URL of the printer host instance. Print host behind HAProxy with basic auth enabled can be accessed by putting the user name and password into the URL in the following format: https://username:password@your-octopi-address/

**Key:** `print_host`

**Type:** `String`

**Default** ``

### Example

```json

```


## Device UI

Specify the URL of your device user interface if it's not same as print_host

**Key:** `print_host_webui`

**Type:** `String`

**Default** ``

### Example

```json

```


## Printer type

Type of the printer

**Key:** `printer_model`

**Type:** `String`

**Default** ``

### Example

```json
"printer_model": "SV05"
```


## Printer notes

You can put your notes regarding the printer here.

**Key:** `printer_notes`

**Type:** `String`

**Default** ``

### Example

```json
"printer_notes": "Don't remove the following keywords! These keywords are used in the \"compatible printer\" condition of the print and filament profiles to link the particular print and filament profiles to this printer profile.nPRINTER_VENDOR_CREALITYnPRINTER_MODEL_SERMOOND1"
```


## Printer settings id

[No documentation provided]

**Key:** `printer_settings_id`

**Type:** `String`

**Default** ``

### Example

```json
"printer_settings_id": "Sovol"
```


## Printer structure

The physical arrangement and components of a printing device

**Key:** `printer_structure`

**Type:** `Enum`

**Default** `Undefine`

**Enum values:**


### Example

```json
"printer_structure": "i3"
```


## Printer variant

Name of the printer variant. For example, the printer variants may be differentiated by a nozzle diameter.

**Key:** `printer_variant`

**Type:** `String`

**Default** ``

### Example

```json
"printer_variant": 0.8
```


## API Key / Password

OrcaSlicer can upload G-code files to a printer host. This field should contain the API Key or the password required for authentication.

**Key:** `printhost_apikey`

**Type:** `String`

**Default** ``

### Example

```json

```


## Authorization Type

[No documentation provided]

**Key:** `printhost_authorization_type`

**Type:** `Enum`

**Default** `KeyPassword`

**Enum values:**


### Example

```json
"printhost_authorization_type": "key"
```


## HTTPS CA File

Custom CA certificate file can be specified for HTTPS OctoPrint connections, in crt/pem format. If left blank, the default OS CA certificate repository is used.

**Key:** `printhost_cafile`

**Type:** `String`

**Default** ``

### Example

```json

```


## Printer password

[No documentation provided]

**Key:** `printhost_password`

**Type:** `String`

**Default** ``

### Example

```json

```


## Printer port

[No documentation provided]

**Key:** `printhost_port`

**Type:** `String`

**Default** ``

### Example

```json

```


## Ignore HTTPS certificate revocation checks

Ignore HTTPS certificate revocation checks in case of missing or offline distribution points. One may want to enable this option for self signed certificates if connection fails.

**Key:** `printhost_ssl_ignore_revoke`

**Type:** `Bool`

**Default** `false`

### Example

```json
"printhost_ssl_ignore_revoke": false
```


## Printer username

[No documentation provided]

**Key:** `printhost_user`

**Type:** `String`

**Default** ``

### Example

```json

```


## Purge in prime tower

Purge remaining filament into prime tower

**Key:** `purge_in_prime_tower`

**Type:** `Bool`

**Default** `true`

### Example

```json
"purge_in_prime_tower": false
```


## Retract amount before wipe

The length of fast retraction before wipe, relative to retraction length

**Key:** `retract_before_wipe`

**Type:** `Percents`

**Nullable:** true

**Default** `[100]`

### Example

```json
"retract_before_wipe": "100%,100%"
```


## Retraction length (toolchange)

When retraction is triggered before changing tool, filament is pulled back by the specified amount (the length is measured on raw filament, before it enters the extruder).

**Key:** `retract_length_toolchange`

**Type:** `Floats`

**Default** `[10.0]`

### Example

```json
"retract_length_toolchange": [
    2,
    2
  ]
```


## Only lift Z above

If you set this to a positive value, Z lift will only take place above the specified absolute Z.

**Key:** `retract_lift_above`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"retract_lift_above": 0.4
```


## Only lift Z below

If you set this to a positive value, Z lift will only take place below the specified absolute Z.

**Key:** `retract_lift_below`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"retract_lift_below": [299]
```


## Enforce z-hop behavior

Enforce Z Hop behavior. This setting is impacted by the above settings (Only lift Z above/below).

**Key:** `retract_lift_enforce`

**Type:** `Enums`

**Nullable:** true

**Default** `["AllSurfaces"]`

**Enum values:**


### Example

```json
"retract_lift_enforce": ["All Surfaces"]
```


## Extra length on restart

When the retraction is compensated after the travel move, the extruder will push this additional amount of filament. This setting is rarely needed.

**Key:** `retract_restart_extra`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.0]`

### Example

```json
"retract_restart_extra": [0]
```


## Extra length on restart

When the retraction is compensated after changing tool, the extruder will push this additional amount of filament.

**Key:** `retract_restart_extra_toolchange`

**Type:** `Floats`

**Default** `[0.0]`

### Example

```json
"retract_restart_extra_toolchange": 0
```


## Retract when change layer

Force a retraction when changes layer

**Key:** `retract_when_changing_layer`

**Type:** `Bools`

**Nullable:** true

**Default** `[false]`

### Example

```json
"retract_when_changing_layer": [false]
```


## Retraction length

Some amount of material in extruder is pulled back to avoid ooze during long travel. Set zero to disable retraction

**Key:** `retraction_length`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.8]`

### Example

```json
"retraction_length": [4]
```


## Travel distance threshold

Only trigger retraction when the travel distance is longer than this threshold

**Key:** `retraction_minimum_travel`

**Type:** `Floats`

**Nullable:** true

**Default** `[2.0]`

### Example

```json
"retraction_minimum_travel": [2]
```


## Retraction Speed

Speed of retractions

**Key:** `retraction_speed`

**Type:** `Floats`

**Nullable:** true

**Default** `[30.0]`

### Example

```json
"retraction_speed": [25]
```


## Scan first layer

Enable this to enable the camera on printer to check the quality of first layer

**Key:** `scan_first_layer`

**Type:** `Bool`

**Default** `false`

### Example

```json
"scan_first_layer": false
```


## Supports silent mode

Whether the machine supports silent mode in which machine use lower acceleration to print

**Key:** `silent_mode`

**Type:** `Bool`

**Default** `false`

### Example

```json
"silent_mode": true
```


## Single Extruder Multi Material

Use single nozzle to print multi filament

**Key:** `single_extruder_multi_material`

**Type:** `Bool`

**Default** `true`

### Example

```json
"single_extruder_multi_material": false
```


## Support air filtration

Enable this if printer support air filtration\nG-code command: M106 P3 S(0-255)

**Key:** `support_air_filtration`

**Type:** `Bool`

**Default** `true`

### Example

```json
"support_air_filtration": false
```


## Support control chamber temperature

This option is enabled if machine support controlling chamber temperature\nG-code command: M141 S(0-255)

**Key:** `support_chamber_temp_control`

**Type:** `Bool`

**Default** `true`

### Example

```json
"support_chamber_temp_control": false
```


## Custom G-code

This G-code will be used as a custom code

**Key:** `template_custom_gcode`

**Type:** `String`

**Default** ``

### Example

```json

```


## G-code thumbnails

Picture sizes to be stored into a .gcode and .sl1 / .sl1s files, in the following format: "XxY, XxY, ..."

**Key:** `thumbnails`

**Type:** `Points`

**Default** `[[300, 300]]`

### Example

```json

```


## Format of G-code thumbnails

Format of G-code thumbnails: PNG for best quality, JPG for smallest size, QOI for low memory firmware

**Key:** `thumbnails_format`

**Type:** `Enum`

**Default** `PNG`

**Enum values:**


### Example

```json
"thumbnails_format": "JPG"
```


## Time cost

The printer cost per hour

**Key:** `time_cost`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"time_cost": 1.46
```


## Time lapse G-code

[No documentation provided]

**Key:** `time_lapse_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"time_lapse_gcode": ";===================== date: 20230922 =====================\n{if !spiral_mode && print_sequence != \"by object\"}\n; don't support timelapse gcode in spiral_mode and by object sequence for I3 structure printer\nM622.1 S1 ; for prev firware, default turned on\nM1002 judge_flag timelapse_record_flag\nM622 J1\nG92 E0\nG17\nG2 Z{layer_z + 0.4} I0.86 J0.86 P1 F20000 ; spiral lift a little\nG1 Z{max_layer_z + 0.4}\nG1 X0 Y{first_layer_center_no_wipe_tower[1]} F18000 ; move to safe pos\nG1 X-13.0 F3000 ; move to safe pos\nM400 P300\nM971 S11 C11 O0\nG92 E0\nG1 X0 F18000\nM623\n\n; enable nozzle clog detect at 3rd layer\n{if layer_num == 2}\n  M400\n  G90\n  M83\n  M204 S5000\n  G0 Z2 F4000\n  G0 X-6 Y170 F20000\n  M400 P200\n  G39 S1\n  G0 Z2 F4000\n  G0 X90 Y90 F30000\n{endif}\n{endif}\n"
```


## upward compatible machine

[No documentation provided]

**Key:** `upward_compatible_machine`

**Type:** `Strings`

**Default** `[]`

### Example

```json
"upward_compatible_machine": [
    "Bambu Lab P1S 0.4 nozzle",
    "Bambu Lab X1 0.4 nozzle",
    "Bambu Lab X1 Carbon 0.4 nozzle",
    "Bambu Lab X1E 0.4 nozzle"
  ]
```


## Use firmware retraction

This experimental setting uses G10 and G11 commands to have the firmware handle the retraction. This is only supported in recent Marlin.

**Key:** `use_firmware_retraction`

**Type:** `Bool`

**Default** `false`

### Example

```json
"use_firmware_retraction": true
```


## Use relative E distances

Relative extrusion is recommended when using "label_objects" option.Some extruders work better with this option unckecked (absolute extrusion mode). Wipe tower is only compatible with relative mode. It is always enabled on BambuLab printers. Default is checked

**Key:** `use_relative_e_distances`

**Type:** `Bool`

**Default** `true`

### Example

```json
"use_relative_e_distances": false
```


## Wipe while retracting

Move nozzle along the last extrusion path when retracting to clean leaked material on nozzle. This can minimize blob when print new part after travel

**Key:** `wipe`

**Type:** `Bools`

**Nullable:** true

**Default** `[false]`

### Example

```json
"wipe": [false]
```


## Wipe Distance

Discribe how long the nozzle will move along the last path when retracting

**Key:** `wipe_distance`

**Type:** `Floats`

**Nullable:** true

**Min:** `0`

**Default** `[1.0]`

### Example

```json
"wipe_distance": [0.2]
```


## Z hop when retract

Whenever the retraction is done, the nozzle is lifted a little to create clearance between nozzle and the print. It prevents nozzle from hitting the print when travel move. Using spiral line to lift z can prevent stringing

**Key:** `z_hop`

**Type:** `Floats`

**Nullable:** true

**Default** `[0.4]`

### Example

```json
"z_hop": [0.25]
```


## Z hop type

Z hop type

**Key:** `z_hop_types`

**Type:** `Enums`

**Nullable:** true

**Default** `["Normal"]`

**Enum values:**


### Example

```json
"z_hop_types": "Normal Lift"
```


## Z offset

This value will be added (or subtracted) from all the Z coordinates in the output G-code. It is used to compensate for bad Z endstop position: for example, if your endstop zero actually leaves the nozzle 0.3mm far from the print bed, set this to -0.3 (or fix your endstop).

**Key:** `z_offset`

**Type:** `Float`

**Default** `0`

### Example

```json
"z_offset": 0
```
