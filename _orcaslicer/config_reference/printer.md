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

**Type:** `Bool`

**Default** `false`

### Example

```json
"auxiliary_fan": false
```


## Bed exclude area

[No documentation provided]

**Key:** `bed_exclude_area`

**Type:** `Points`

**Default** `[0, 0]`

### Example

```json
"bed_exclude_area": [
    [
      2.0,
      2.4
    ],
    [
      0.83,
      4.7
    ],
    [
      0.42,
      2.41
    ]
  ]
```


## Before layer change G-code

This G-code is inserted at every layer change before lifting z

**Key:** `before_layer_change_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"before_layer_change_gcode": ""
```


## Best object position

Best auto arranging position in range [0,1] w.r.t. bed shape.

**Key:** `best_object_pos`

**Type:** `Point`

**Default** `[0.5, 0.5]`

### Example

```json
"best_object_pos": [
    0.6,
    0.57
  ]
```


## Change filament G-code

This gcode is inserted when change filament, including T command to trigger tool change

**Key:** `change_filament_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"change_filament_gcode": ""
```


## Cooling tube length

Length of the cooling tube to limit space for cooling moves inside it.

**Key:** `cooling_tube_length`

**Type:** `Float`

**Min:** `0`

**Default** `5.0`

### Example

```json
"cooling_tube_length": 3.79
```


## Cooling tube position

Distance of the center-point of the cooling tube from the extruder tip.

**Key:** `cooling_tube_retraction`

**Type:** `Float`

**Min:** `0`

**Default** `91.5`

### Example

```json
"cooling_tube_retraction": 80.62
```


## Default process profile

Default process profile when switch to this machine profile

**Key:** `default_print_profile`

**Type:** `String`

**Default** ``

### Example

```json
"default_print_profile": ""
```


## Enable filament ramming

Enable filament ramming

**Key:** `enable_filament_ramming`

**Type:** `Bool`

**Default** `true`

### Example

```json
"enable_filament_ramming": true
```


## Extra loading distance

When set to zero, the distance the filament is moved from parking position during load is exactly the same as it was moved back during unload. When positive, it is loaded further,  if negative, the loading move is shorter than unloading.

**Key:** `extra_loading_move`

**Type:** `Float`

**Default** `-2.0`

### Example

```json
"extra_loading_move": -1.63
```


## Height to lid

Distance of the nozzle tip to the lid. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_lid`

**Type:** `Float`

**Min:** `0`

**Default** `120`

### Example

```json
"extruder_clearance_height_to_lid": 136.72
```


## Height to rod

Distance of the nozzle tip to the lower rod. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_rod`

**Type:** `Float`

**Min:** `0`

**Default** `40`

### Example

```json
"extruder_clearance_height_to_rod": 40.14
```


## Radius

Clearance radius around extruder. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_radius`

**Type:** `Float`

**Min:** `0`

**Default** `40`

### Example

```json
"extruder_clearance_radius": 45.47
```


## Fan kick-start time

[No documentation provided]

**Key:** `fan_kickstart`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"fan_kickstart": 4.82
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


## Fan speedup time

[No documentation provided]

**Key:** `fan_speedup_time`

**Type:** `Float`

**Default** `0`

### Example

```json
"fan_speedup_time": 1.69
```


## G-code flavor

What kind of gcode the printer is compatible with

**Key:** `gcode_flavor`

**Type:** `Enum`

**Default** `MarlinLegacy`

**Enum values:**


### Example

```json
"gcode_flavor": "marlin2"
```


## High extruder current on filament swap

It may be beneficial to increase the extruder motor current during the filament exchange sequence to allow for rapid ramming feed rates and to overcome resistance when loading a filament with an ugly shaped tip.

**Key:** `high_current_on_filament_swap`

**Type:** `Bool`

**Default** `false`

### Example

```json
"high_current_on_filament_swap": true
```


## Host Type

Slic3r can upload G-code files to a printer host. This field must contain the kind of the host.

**Key:** `host_type`

**Type:** `Enum`

**Default** `OctoPrint`

**Enum values:**


### Example

```json
"host_type": "flashair"
```


## Layer change G-code

This gcode part is inserted at every layer change after lift z

**Key:** `layer_change_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"layer_change_gcode": ""
```


## Machine end gcode

End G-code when finish the whole printing

**Key:** `machine_end_gcode`

**Type:** `String`

**Default** `M104 S0 ; turn off temperature\nG28 X0  ; home X axis\nM84     ; disable motors\n`

### Example

```json
"machine_end_gcode": ""
```


## Machine load filament time

Time to load new filament when switch filament. For statistics only

**Key:** `machine_load_filament_time`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"machine_load_filament_time": 1.02
```


## Pause G-code

This G-code will be used as a code for the pause print. User can insert pause G-code in gcode viewer

**Key:** `machine_pause_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"machine_pause_gcode": ""
```


## Machine start gcode

Start G-code when start the whole printing

**Key:** `machine_start_gcode`

**Type:** `String`

**Default** `G28 ; home all axes\nG1 Z5 F5000 ; lift nozzle\n`

### Example

```json
"machine_start_gcode": ""
```


## Machine unload filament time

Time to unload old filament when switch filament. For statistics only

**Key:** `machine_unload_filament_time`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"machine_unload_filament_time": 4.7
```


## Manual Filament Change

[No documentation provided]

**Key:** `manual_filament_change`

**Type:** `Bool`

**Default** `false`

### Example

```json
"manual_filament_change": false
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
"nozzle_volume": 1.56
```


## Filament parking position

Distance of the extruder tip from the position where the filament is parked when unloaded. This should match the value in printer firmware.

**Key:** `parking_pos_retraction`

**Type:** `Float`

**Min:** `0`

**Default** `92.0`

### Example

```json
"parking_pos_retraction": 93.28
```


## Hostname, IP or URL

Slic3r can upload G-code files to a printer host. This field should contain the hostname, IP address or URL of the printer host instance. Print host behind HAProxy with basic auth enabled can be accessed by putting the user name and password into the URL in the following format: https://username:password@your-octopi-address/

**Key:** `print_host`

**Type:** `String`

**Default** ``

### Example

```json
"print_host": ""
```


## Device UI

Specify the URL of your device user interface if it's not same as print_host

**Key:** `print_host_webui`

**Type:** `String`

**Default** ``

### Example

```json
"print_host_webui": ""
```


## Printer type

Type of the printer

**Key:** `printer_model`

**Type:** `String`

**Default** ``

### Example

```json
"printer_model": ""
```


## Printer notes

You can put your notes regarding the printer here.

**Key:** `printer_notes`

**Type:** `String`

**Default** ``

### Example

```json
"printer_notes": ""
```


## Printer structure

The physical arrangement and components of a printing device

**Key:** `printer_structure`

**Type:** `Enum`

**Default** `Undefine`

**Enum values:**


### Example

```json
"printer_structure": "hbot"
```


## Printer variant

Name of the printer variant. For example, the printer variants may be differentiated by a nozzle diameter.

**Key:** `printer_variant`

**Type:** `String`

**Default** ``

### Example

```json
"printer_variant": ""
```


## API Key / Password

Slic3r can upload G-code files to a printer host. This field should contain the API Key or the password required for authentication.

**Key:** `printhost_apikey`

**Type:** `String`

**Default** ``

### Example

```json
"printhost_apikey": ""
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
"printhost_cafile": ""
```


## Printhost password

[No documentation provided]

**Key:** `printhost_password`

**Type:** `String`

**Default** ``

### Example

```json
"printhost_password": ""
```


## Printhost port

Name of the printer

**Key:** `printhost_port`

**Type:** `String`

**Default** ``

### Example

```json
"printhost_port": ""
```


## Ignore HTTPS certificate revocation checks

Ignore HTTPS certificate revocation checks in case of missing or offline distribution points. One may want to enable this option for self signed certificates if connection fails.

**Key:** `printhost_ssl_ignore_revoke`

**Type:** `Bool`

**Default** `false`

### Example

```json
"printhost_ssl_ignore_revoke": true
```


## Printhost user

[No documentation provided]

**Key:** `printhost_user`

**Type:** `String`

**Default** ``

### Example

```json
"printhost_user": ""
```


## Purge in prime tower

Purge remaining filament into prime tower

**Key:** `purge_in_prime_tower`

**Type:** `Bool`

**Default** `true`

### Example

```json
"purge_in_prime_tower": true
```


## Retract lift enforce

Enforce Z Hop behavior. This setting is impacted by the above settings (Only lift Z above/below).

**Key:** `retract_lift_enforce`

**Type:** `Enums`

**Nullable:** true

**Default** `["RetractLiftEnforceType ::rletAllSurfaces"]`

**Enum values:**


### Example

```json
"retract_lift_enforce": [
    "Bottom Only"
  ]
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
"silent_mode": false
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
"support_air_filtration": true
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
"template_custom_gcode": ""
```


## G-code thumbnails

Picture sizes to be stored into a .gcode and .sl1 / .sl1s files, in the following format: \"XxY, XxY, ...\"

**Key:** `thumbnails`

**Type:** `Points`

**Default** `[300, 300]`

### Example

```json
"thumbnails": [
    [
      300,
      301
    ],
    [
      303,
      302
    ],
    [
      304,
      302
    ]
  ]
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
"time_cost": 4.7
```


## Time lapse G-code

[No documentation provided]

**Key:** `time_lapse_gcode`

**Type:** `String`

**Default** ``

### Example

```json
"time_lapse_gcode": ""
```


## upward compatible machine

[No documentation provided]

**Key:** `upward_compatible_machine`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"upward_compatible_machine": [
    "",
    "",
    "",
    ""
  ]
```


## Use firmware retraction

This experimental setting uses G10 and G11 commands to have the firmware handle the retraction. This is only supported in recent Marlin.

**Key:** `use_firmware_retraction`

**Type:** `Bool`

**Default** `false`

### Example

```json
"use_firmware_retraction": false
```


## Use relative E distances

Relative extrusion is recommended when using \"label_objects\" option.Some extruders work better with this option unckecked (absolute extrusion mode). Wipe tower is only compatible with relative mode. It is always enabled on BambuLab printers. Default is checked

**Key:** `use_relative_e_distances`

**Type:** `Bool`

**Default** `true`

### Example

```json
"use_relative_e_distances": true
```


## Z hop types

Z hop type

**Key:** `z_hop_types`

**Type:** `Enums`

**Nullable:** true

**Default** `["Normal"]`

**Enum values:**


### Example

```json
"z_hop_types": [
    "Auto Lift",
    "Slope Lift"
  ]
```


## Z offset

This value will be added (or subtracted) from all the Z coordinates in the output G-code. It is used to compensate for bad Z endstop position: for example, if your endstop zero actually leaves the nozzle 0.3mm far from the print bed, set this to -0.3 (or fix your endstop).

**Key:** `z_offset`

**Type:** `Float`

**Default** `0`

### Example

```json
"z_offset": 0.38
```
