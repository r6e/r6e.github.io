---
layout: default
title: "Printer"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "Printer"
---

Configuration options for a configuration file with `"type": "machine"`.

## Auxiliary part cooling fan

Enable this option if machine has auxiliary part cooling fan. G-code command: M106 P2 S(0-255).

**Key:** `auxiliary_fan`

**Type:** `boolean`

**Default:** `null`

### Example

```json
"auxiliary_fan": "0"
```

## Bed custom model

**Key:** `bed_custom_model`

**Type:** `string`

**Default:** (empty)

### Example

```json
"bed_custom_model": "printer_bed.stl"
```

**Note:** There are currently no built-in profiles that use this setting.

## Bed custom texture

**Key:** `bed_custom_texture`

**Type:** `string`

**Default:** (empty)

### Example

```json
"bed_custom_texture": "printer_bed.svg" 
```

**Note:** There are currently no built-in profiles that use this setting.

## Bed exclude area

Unprintable area in XY plane. For example, X1 Series printers use the front left corner to cut filament during filament change. The area is expressed as polygon by points in following format: "XxY, XxY, ..."

**Key:** `bed_exclude_area`

**Type:** `[[integer, integer]]`

**Default:** `[[0, 0]]`

### Example

```json
"bed_exclude_area": ["0x0"]
```

## Before layer change G-code

This G-code is inserted at every layer change before lifting z

**Key:** `before_layer_change_gcode`

**Type:** `string`

**Default:** (empty)

### Example

```json
"before_layer_change_gcode": ";BEFORE_LAYER_CHANGE
;[layer_z]
G92 E0
"
```

## Best object position

Best auto arranging position in range [0,1] w.r.t. bed shape.

**Key:** `best_object_pos`

**Type:** `[integer, integer]`

**Default:** `[0.5, 0.5]`

### Example

```json
"best_object_pos": "0.7x0.5"
```

## Change filament G-code

This gcode is inserted when change filament, including T command to trigger tool change

**Key:** `change_filament_gcode`

**Type:** `string`

**Default:** (empty)

### Example

```json
"change_filament_gcode": "M601"
```

**Note:** There are currently no built-in profiles that use this setting.

## Cooling tube length

Length of the cooling tube to limit space for cooling moves inside it.

**Key:** `cooling_tube_length`

**Type:** `float`

**Default:** `5.0`

**Min:** `0`

### Example

```json
"cooling_tube_length": "4.3"
```

**Note:** There are currently no built-in profiles that use this setting.

## Cooling tube position

Distance of the center-point of the cooling tube from the extruder tip.

**Key:** `cooling_tube_retraction`

**Type:** `float`

**Default:** `91.5`

**Min:** `0`

### Example

```json
"cooling_tube_retraction": "59.4"
```

**Note:** There are currently no built-in profiles that use this setting.

## Default process profile

Default process profile when switch to this machine profile

**Key:** `default_print_profile`

**Type:** `string`

**Default:** `null`

### Example

```json
"default_print_profile": "0.20mm Standard @Artillery Genius"
```

## Enable filament ramming

Enable filament ramming

**Key:** `enable_filament_ramming`

**Type:** `boolean`

**Default:** `true`

### Example

```json
"enable_filament_ramming": "0"
```

## Extra loading distance

When set to zero, the distance the filament is moved from parking position during load is exactly the same as it was moved back during unload. When positive, it is loaded further,  if negative, the loading move is shorter than unloading.

**Key:** `extra_loading_move`

**Type:** `float`

**Default:** `-2.0`

### Example

```json
"extra_loading_move": "1.2"
```

**Note:** There are currently no built-in profiles that use this setting.

## Height to lid

Distance of the nozzle tip to the lid. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_lid`

**Type:** `float`

**Default:** `120`

**Min:** `0`

### Example

```json
"extruder_clearance_height_to_lid": "140"
```

## Height to rod

Distance of the nozzle tip to the lower rod. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_rod`

**Type:** `float`

**Default:** `40`

**Min:** `0`

### Example

```json
"extruder_clearance_height_to_rod": "36"
```

## Extruder clearance radius

Clearance radius around extruder. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_radius`

**Type:** `float`

**Default:** `40`

**Min:** `0`

### Example

```json
"extruder_clearance_radius": "45"
```

## Fan kick-start time

Emit a max fan speed command for this amount of seconds before reducing to target speed to kick-start the cooling fan.
This is useful for fans where a low PWM/power may be insufficient to get the fan started spinning from a stop, or to get the fan up to speed faster.
Set to 0 to deactivate.

**Key:** `fan_kickstart`

**Type:** `float`

**Default:** `0`

**Min:** `0`

### Example

```json
"fan_kickstart": "0.2"
```

## Fan speedup only on overhangs

Will only take into account the delay for the cooling of overhangs.

**Key:** `fan_speedup_overhangs`

**Type:** `boolean`

**Default:** `true`

### Example

```json
"fan_speedup_overhangs": "0"
```

## Fan speed-up time

Start the fan this number of seconds earlier than its target start time (you can use fractional seconds). It assumes infinite acceleration for this time estimation, and will only take into account G1 and G0 moves (arc fitting is unsupported).
It won't move fan comands from custom gcodes (they act as a sort of 'barrier').
It won't move fan comands into the start gcode if the 'only custom start gcode' is activated.
Use 0 to deactivate.

**Key:** `fan_speedup_time`

**Type:** `float`

**Default:** `0`

### Example

```json
"fan_speedup_time": "0.5"
```

## G-code flavor

What kind of gcode the printer is compatible with

**Key:** `gcode_flavor`

**Type:** `enum`

**Default:** `marlin`

**Values:**
* **Marlin(legacy)**: `marlin`
* **Klipper**: `klipper`
* **RepRapFirmware**: `reprapfirmware`
* **RepRap/Sprinter**: `reprapsprinter`
* **Repetier**: `repetier`
* **Teacup**: `teacup`
* **MakerWare (MakerBot)**: `makerware`
* **Marlin 2**: `marlin2`
* **Sailfish (MakerBot)**: `sailfish`
* **Mach3/LinuxCNC**: `mach3`
* **Machinekit**: `machinekit`
* **Smoothie**: `smoothie`
* **No extrusion**: `no-extrusion`

### Example

```json
"gcode_flavor": "marlin"
```

## High extruder current on filament swap

It may be beneficial to increase the extruder motor current during the filament exchange sequence to allow for rapid ramming feed rates and to overcome resistance when loading a filament with an ugly shaped tip.

**Key:** `high_current_on_filament_swap`

**Type:** `boolean`

**Default:** `0`

### Example

```json
"high_current_on_filament_swap": 
```

## Host Type

Slic3r can upload G-code files to a printer host. This field must contain the kind of the host.

**Key:** `host_type`

**Type:** `enum`

**Default:** `octoprint`

**Values:**
* **PrusaLink**: `prusalink`
* **PrusaConnect**: `prusaconnect`
* **Octo/Klipper**: `octoprint`
* **Duet**: `duet`
* **FlashAir**: `flashair`
* **AstroBox**: `astrobox`
* **Repetier**: `repetier`
* **MKS**: `mks`

### Example

```json
"host_type": "prusalink"
```

## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `string`

**Default:** `null`

### Example

```json
"inherits": "fdm_machine_common"
```

## Layer change G-code

This gcode part is inserted at every layer change after lift z

**Key:** `layer_change_gcode`

**Type:** `string`

**Default:** (empty)

### Example

```json
"layer_change_gcode": ";AFTER_LAYER_CHANGE
;[layer_z]"
```

## End G-code

End G-code when finish the whole printing

**Key:** `machine_end_gcode`

**Type:** `string`

**Default:** `M104 S0 ; turn off temperature
G28 X0  ; home X axis
M84     ; disable motors
`

### Example

```json
"machine_end_gcode": "; BIQU BX Default End Gcode\nG91;Relative positioning\nG1 E-2 F2700;Retract a bit\nG1 E-2 Z0.2 F2400;Retract a bit more and raise Z\nG1 X5 Y5 F3000;Wipe out\nG1 Z10;Raise Z by 10mm\nG90;Return to absolute positioning\nG1 X0 Y{machine_depth};TaDaaaa\nM106 S0;Turn-off fan\nM104 S0;Turn-off hotend\nM140 S0;Turn-off bed\nM84 X Y E;Disable all steppers but Z"
```

## Filament load time

Time to load new filament when switch filament. For statistics only

**Key:** `machine_load_filament_time`

**Type:** `float`

**Default:** `0.0`

**Min:** `0`

### Example

```json
"machine_load_filament_time": "17"
```

## Pause G-code

This G-code will be used as a code for the pause print. User can insert pause G-code in gcode viewer

**Key:** `machine_pause_gcode`

**Type:** `string`

**Default:** (empty)

### Example

```json
"machine_pause_gcode": "M400 U1
"
```

## Start G-code

Start G-code when start the whole printing

**Key:** `machine_start_gcode`

**Type:** `string`

**Default:** `G28 ; home all axes
G1 Z5 F5000 ; lift nozzle
`

### Example

```json
"machine_start_gcode": "; Initial setups
G90 ; use absolute coordinates
M83 ; extruder relative mode
M900 K0.12 ; K factor
M900 W[line_width] H[layer_height] D[filament_diameter]
M200 D0 ; disable volumetric e
M220 S100 ; reset speed factor to 100%
M221 S100 ; reset extrusion rate to 100%

; Set the heating
M190 S[bed_temperature_initial_layer_single] ; wait for bed to heat up
M104 S[nozzle_temperature_initial_layer] ; start nozzle heating but don't wait

; Home
G1 Z3 F3000 ; move z up little to prevent scratching of surface
G28 ; home all axes
G1 X3 Y3 F5000 ; move to corner of the bed to avoid ooze over centre

; Wait for final heating
M109 S[nozzle_temperature_initial_layer] ; wait for the nozzle to heat up
M190 S[bed_temperature_initial_layer_single] ; wait for the bed to heat up

;Auto bed Leveling
@BEDLEVELVISUALIZER
G29 ; ABL T
M420 S1 Z3 ; reload and fade mesh bed leveling until it reach 3mm Z

; Return to prime position, Prime line routine
G92 E0 ; Reset Extruder
G1 Z3 F3000 ; move z up little to prevent scratching of surface
G1 X10 Y.5 Z0.25 F5000.0 ; Move to start position
G1 X100 Y.5 Z0.25 F1500.0 E15 ; Draw the first line
G1 X100 Y.2 Z0.25 F5000.0 ; Move to side a little
G1 X10 Y.2 Z0.25 F1500.0 E30 ; Draw the second line
G92 E0 ; Reset Extruder
M221 S{if layer_height<0.075}100{else}95{endif}"
```

## Filament unload time

Time to unload old filament when switch filament. For statistics only

**Key:** `machine_unload_filament_time`

**Type:** `float`

**Default:** `0.0`

**Min:** `0`

### Example

```json
"machine_unload_filament_time": "28"
```

## Manual Filament Change

Enable this option to omit the custom Change filament G-code only at the beginning of the print. The tool change command (e.g., T0) will be skipped throughout the entire print. This is useful for manual multi-material printing, where we use M600/PAUSE to trigger the manual filament change action.

**Key:** `manual_filament_change`

**Type:** `boolean`

**Default:** `null`

### Example

```json
"manual_filament_change":  "1"
```

## Nozzle HRC

The nozzle's hardness. Zero means no checking for nozzle's hardness during slicing.

**Key:** `nozzle_hrc`

**Type:** `integer`

**Default:** `0`

**Max:** `500`

**Min:** `0`

### Example

```json
"nozzle_hrc": "20"
```

## Nozzle type

The metallic material of nozzle. This determines the abrasive resistance of nozzle, and what kind of filament can be printed

**Key:** `nozzle_type`

**Type:** `enum`

**Default:** `undefine`

**Values:**
* **Undefine**: `undefine`
* **Hardened steel**: `hardened_steel`
* **Stainless steel**: `stainless_steel`
* **Brass**: `brass`

### Example

```json
"nozzle_type": "brass"
```

## Nozzle volume

Volume of nozzle between the cutter and the end of nozzle

**Key:** `nozzle_volume`

**Type:** `float`

**Default:** `0.0`

### Example

```json
"nozzle_volume": "107"
```

## Filament parking position

Distance of the extruder tip from the position where the filament is parked when unloaded. This should match the value in printer firmware.

**Key:** `parking_pos_retraction`

**Type:** `float`

**Default:** `92.0`

**Min:** `0`

### Example

```json
"parking_pos_retraction": "91.2"
```

**Note:** There are currently no built-in profiles that use this setting.

## Hostname, IP or URL

Slic3r can upload G-code files to a printer host. This field should contain the hostname, IP address or URL of the printer host instance. Print host behind HAProxy with basic auth enabled can be accessed by putting the user name and password into the URL in the following format: https://username:password@your-octopi-address/

**Key:** `print_host`

**Type:** `string`

**Default:** (empty)

### Example

```json
"print_host": "192.168.1.202"
```

## Device UI

Specify the URL of your device user interface if it's not same as print_host

**Key:** `print_host_webui`

**Type:** `string`

**Default:** (empty)

### Example

```json
"print_host_webui": "http://192.168.1.202"
```

## Printable area

**Key:** `printable_area`

**Type:** `[[integer, integer]]`

**Default:** `[[0, 0], [200, 0], [200, 200], [0, 200]]`

### Example

```json
"printable_area": ["0x0","300x0","300x300","0x300"]
```

## Printable height

Maximum printable height which is limited by mechanism of printer

**Key:** `printable_height`

**Type:** `float`

**Default:** `100.0`

**Max:** `2000`

**Min:** `0`

### Example

```json
"printable_height": "400"
```

## Printer model

Type of the printer

**Key:** `printer_model`

**Type:** `string`

**Default:** `null`

### Example

```json
"printer_model": "Vzbot 330 AWD"
```

## Printer notes

You can put your notes regarding the printer here.

**Key:** `printer_notes`

**Type:** `string`

**Default:** (empty)

### Example

```json
"printer_notes": "Don't remove the following keywords! These keywords are used in the \"compatible printer\" condition of the print and filament profiles to link the particular print and filament profiles to this printer profile.
PRINTER_VENDOR_PRUSA3D
PRINTER_MODEL_MK3
"
```

## Printer structure

The physical arrangement and components of a printing device

**Key:** `printer_structure`

**Type:** `enum`

**Default:** `undefine`

**Values:**
* **Undefine**: `undefine`
* **CoreXY**: `corexy`
* **I3**: `i3`
* **Hbot**: `hbot`
* **Delta**: `delta`

### Example

```json
"printer_structure": "corexy"
```

## Printer technology

Printer technology

**Key:** `printer_technology`

**Type:** `enum`

**Default:** `FFF`

**Values:**
* `FFF`
* `SLA`

### Example

```json
"printer_technology": "FFF"
```

## Printer variant

Name of the printer variant. For example, the printer variants may be differentiated by a nozzle diameter.

**Key:** `printer_variant`

**Type:** `string`

**Default:** `null`

### Example

```json
"printer_variant": "0.4"
```

## API Key / Password

Slic3r can upload G-code files to a printer host. This field should contain the API Key or the password required for authentication.

**Key:** `printhost_apikey`

**Type:** `string`

**Default:** (empty)

### Example

```json
"printhost_apikey": "2089ed2024b1499963b5e8b892103a977f17d3c572b0cface466bd7536402e18"
```

## Authorization Type

**Key:** `printhost_authorization_type`

**Type:** `enum`

**Default:** `key`

**Values:**
* **API key**: `key`
* **HTTP digest**: `user`

### Example

```json
"printhost_authorization_type": "key"
```

## HTTPS CA File

Custom CA certificate file can be specified for HTTPS OctoPrint connections, in crt/pem format. If left blank, the default OS CA certificate repository is used.

**Key:** `printhost_cafile`

**Type:** `string`

**Default:** (empty)

### Example

```json
"printhost_cafile": "some_authority.ca"
```

## Password

**Key:** `printhost_password`

**Type:** `string`

**Default:** (empty)

### Example

```json
"printhost_password": "changeme!"
```

## Printer host port

Port used to connect to the printer

**Key:** `printhost_port`

**Type:** `string`

**Default:** (empty)

### Example

```json
"printhost_port": "8080"
```

## Ignore HTTPS certificate revocation checks

Ignore HTTPS certificate revocation checks in case of missing or offline distribution points. One may want to enable this option for self signed certificates if connection fails.

**Key:** `printhost_ssl_ignore_revoke`

**Type:** `boolean`

**Default:** `null`

### Example

```json
"printhost_ssl_ignore_revoke": "0"
```

## User

**Key:** `printhost_user`

**Type:** `string`

**Default:** (empty)

### Example

```json
"printhost_user": "printeruser"
```

## Purge in prime tower

Purge remaining filament into prime tower

**Key:** `purge_in_prime_tower`

**Type:** `boolean`

**Default:** `true`

### Example

```json
"purge_in_prime_tower": "0"
```

## Z-hop on surfaces

Enforce Z Hop behavior. This setting is impacted by the above settings (Only lift Z above/below).

**Key:** `retract_lift_enforce`

**Type:** `[enum]`

**Default:** `All Surfaces`

**Values:**
* **All Surfaces**: `All Surfaces`
* **Top Only**: `Top Only`
* **Bottom Only**: `Bottom Only`
* **Top and Bottom**: `Top and Bottom`

### Example

```json
"retract_lift_enforce": "Top Only"
```

**Note:** There are currently no built-in profiles that use this setting.

## Scan first layer

Enable this to enable the camera on printer to check the quality of first layer

**Key:** `scan_first_layer`

**Type:** `boolean`

**Default:** `null`

### Example

```json
"scan_first_layer": "0"
```

## Supports silent mode

Whether the machine supports silent mode in which machine use lower acceleration to print

**Key:** `silent_mode`

**Type:** `boolean`

**Default:** `null`

### Example

```json
"silent_mode": "0"
```

## Single Extruder Multi Material

Use single nozzle to print multi filament

**Key:** `single_extruder_multi_material`

**Type:** `boolean`

**Default:** `true`

### Example

```json
"single_extruder_multi_material": "1"
```

## Support air filtration

Enable this if printer support air filtration
G-code command: M106 P3 S(0-255)

**Key:** `support_air_filtration`

**Type:** `boolean`

**Default:** `true`

### Example

```json
"support_air_filtration": "1"
```

## Support control chamber temperature

This option is enabled if machine support controlling chamber temperature
G-code command: M141 S(0-255)

**Key:** `support_chamber_temp_control`

**Type:** `boolean`

**Default:** `true`

### Example

```json
"support_chamber_temp_control": "1"
```

## Custom G-code

This G-code will be used as a custom code

**Key:** `template_custom_gcode`

**Type:** `string`

**Default:** (empty)

### Example

```json
"template_custom_gcode": ""
```

## G-code thumbnail sizes

Picture sizes to be stored into a .gcode and .sl1 / .sl1s files, in the following format: "XxY, XxY, ..."

**Key:** `thumbnails`

**Type:** `[[integer, integer]]`

**Default:** `[[300, 300]]`

### Example

```json
"thumbnails": ["160x120"]
```

## Format of G-code thumbnails

Format of G-code thumbnails: PNG for best quality, JPG for smallest size, QOI for low memory firmware

**Key:** `thumbnails_format`

**Type:** `enum`

**Default:** `PNG`

**Values:**
* `PNG`
* `JPG`
* `QOI`
* `BTT TFT`

### Example

```json
"thumbnails_format":  "jpg"
```

## Time cost

The printer cost per hour

**Key:** `time_cost`

**Type:** `float`

**Default:** `0`

**Min:** `0`

### Example

```json
"time_cost": "0.03"
```

## Time lapse G-code

**Key:** `time_lapse_gcode`

**Type:** `string`

**Default:** (empty)

### Example

```json
"time_lapse_gcode": "{if !spiral_mode && print_sequence != \"by object\"}
;===================== date: 20230922 =====================
; timelapse gcode
; don't support timelapse gcode in spiral_mode and by object sequence for I3 structure printer
M622.1 S1 ; for prev firware, default turned on
M1002 judge_flag timelapse_record_flag
M622 J1
G92 E0
G17
G2 Z{layer_z + 0.4} I0.86 J0.86 P1 F20000 ; spiral lift a little
G1 Z{max_layer_z + 0.4}
G1 X0 Y{first_layer_center_no_wipe_tower[1]} F18000 ; move to safe pos
G1 X-13.0 F3000 ; move to safe pos
M400 P300
M971 S11 C11 O0
G92 E0
G1 X0 F18000
M623

{if layer_num == 2}
  M400
  G90
  M83
  M204 S5000
  G0 Z2 F4000
  G0 X-6 Y170 F20000
  M400 P200
  G39 S1
  G0 Z2 F4000
  G0 X90 Y90 F30000
{endif}

{endif}
"
```

## upward compatible machine

**Key:** `upward_compatible_machine`

**Type:** `[string]`

**Default:** `null`

### Example

```json
"upward_compatible_machine": ["Bambu Lab P1S 0.2 nozzle","Bambu Lab P1P 0.2 nozzle","Bambu Lab X1 0.2 nozzle","Bambu Lab X1 Carbon 0.2 nozzle","Bambu Lab X1E 0.2 nozzle"]
```

## Use firmware retraction

This experimental setting uses G10 and G11 commands to have the firmware handle the retraction. This is only supported in recent Marlin.

**Key:** `use_firmware_retraction`

**Type:** `boolean`

**Default:** `null`

### Example

```json
"use_firmware_retraction": "1"
```

## Use relative E distances

Relative extrusion is recommended when using "label_objects" option.Some extruders work better with this option unckecked (absolute extrusion mode). Wipe tower is only compatible with relative mode. It is always enabled on BambuLab printers. Default is checked

**Key:** `use_relative_e_distances`

**Type:** `boolean`

**Default:** `true`

### Example

```json
"use_relative_e_distances": "1"
```

## Z hop type

Z hop type

**Key:** `z_hop_types`

**Type:** `[enum]`

**Default:** `Normal`

**Values:**
* **Auto**: `Auto Lift`
* **Normal**: `Normal Lift`
* **Slope**: `Slope Lift`
* **Spiral**: `Spiral Lift`

### Example

```json
"z_hop_types": ["Auto Lift"]
```

## Z offset

This value will be added (or subtracted) from all the Z coordinates in the output G-code. It is used to compensate for bad Z endstop position: for example, if your endstop zero actually leaves the nozzle 0.3mm far from the print bed, set this to -0.3 (or fix your endstop).

**Key:** `z_offset`

**Type:** `float`

**Default:** `0`

### Example

```json
"z_offset":  "0.25"
```

