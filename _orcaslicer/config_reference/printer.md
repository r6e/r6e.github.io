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

## Bed custom model

**Key:** `bed_custom_model`

**Type:** `string`

**Default:** (empty)

## Bed custom texture

**Key:** `bed_custom_texture`

**Type:** `string`

**Default:** (empty)

## Bed exclude area

Unprintable area in XY plane. For example, X1 Series printers use the front left corner to cut filament during filament change. The area is expressed as polygon by points in following format: "XxY, XxY, ..."

**Key:** `bed_exclude_area`

**Type:** `[[integer, integer]]`

**Default:** `[[0, 0]]`

## Before layer change G-code

This G-code is inserted at every layer change before lifting z

**Key:** `before_layer_change_gcode`

**Type:** `string`

**Default:** (empty)

## Best object position

Best auto arranging position in range [0,1] w.r.t. bed shape.

**Key:** `best_object_pos`

**Type:** `[integer, integer]`

**Default:** `[0.5, 0.5]`

## Change filament G-code

This gcode is inserted when change filament, including T command to trigger tool change

**Key:** `change_filament_gcode`

**Type:** `string`

**Default:** (empty)

## Cooling tube length

Length of the cooling tube to limit space for cooling moves inside it.

**Key:** `cooling_tube_length`

**Type:** `float`

**Default:** `5.0`

**Min:** `0`

## Cooling tube position

Distance of the center-point of the cooling tube from the extruder tip.

**Key:** `cooling_tube_retraction`

**Type:** `float`

**Default:** `91.5`

**Min:** `0`

## Default process profile

Default process profile when switch to this machine profile

**Key:** `default_print_profile`

**Type:** `string`

**Default:** `null`

## Enable filament ramming

Enable filament ramming

**Key:** `enable_filament_ramming`

**Type:** `boolean`

**Default:** `true`

## Extra loading distance

When set to zero, the distance the filament is moved from parking position during load is exactly the same as it was moved back during unload. When positive, it is loaded further,  if negative, the loading move is shorter than unloading.

**Key:** `extra_loading_move`

**Type:** `float`

**Default:** `-2.0`

## Height to lid

Distance of the nozzle tip to the lid. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_lid`

**Type:** `float`

**Default:** `120`

**Min:** `0`

## Height to rod

Distance of the nozzle tip to the lower rod. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_height_to_rod`

**Type:** `float`

**Default:** `40`

**Min:** `0`

## Radius

Clearance radius around extruder. Used for collision avoidance in by-object printing.

**Key:** `extruder_clearance_radius`

**Type:** `float`

**Default:** `40`

**Min:** `0`

## Fan kick-start time

Emit a max fan speed command for this amount of seconds before reducing to target speed to kick-start the cooling fan.
This is useful for fans where a low PWM/power may be insufficient to get the fan started spinning from a stop, or to get the fan up to speed faster.
Set to 0 to deactivate.

**Key:** `fan_kickstart`

**Type:** `float`

**Default:** `0`

**Min:** `0`

## Only overhangs

Will only take into account the delay for the cooling of overhangs.

**Key:** `fan_speedup_overhangs`

**Type:** `boolean`

**Default:** `true`

## Fan speed-up time

Start the fan this number of seconds earlier than its target start time (you can use fractional seconds). It assumes infinite acceleration for this time estimation, and will only take into account G1 and G0 moves (arc fitting is unsupported).
It won't move fan comands from custom gcodes (they act as a sort of 'barrier').
It won't move fan comands into the start gcode if the 'only custom start gcode' is activated.
Use 0 to deactivate.

**Key:** `fan_speedup_time`

**Type:** `float`

**Default:** `0`

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

## High extruder current on filament swap

It may be beneficial to increase the extruder motor current during the filament exchange sequence to allow for rapid ramming feed rates and to overcome resistance when loading a filament with an ugly shaped tip.

**Key:** `high_current_on_filament_swap`

**Type:** `boolean`

**Default:** `0`

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

## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `string`

**Default:** `null`

## Layer change G-code

This gcode part is inserted at every layer change after lift z

**Key:** `layer_change_gcode`

**Type:** `string`

**Default:** (empty)

## End G-code

End G-code when finish the whole printing

**Key:** `machine_end_gcode`

**Type:** `string`

**Default:** `M104 S0 ; turn off temperature
G28 X0  ; home X axis
M84     ; disable motors
`

## Filament load time

Time to load new filament when switch filament. For statistics only

**Key:** `machine_load_filament_time`

**Type:** `float`

**Default:** `0.0`

**Min:** `0`

## Pause G-code

This G-code will be used as a code for the pause print. User can insert pause G-code in gcode viewer

**Key:** `machine_pause_gcode`

**Type:** `string`

**Default:** (empty)

## Start G-code

Start G-code when start the whole printing

**Key:** `machine_start_gcode`

**Type:** `string`

**Default:** `G28 ; home all axes
G1 Z5 F5000 ; lift nozzle
`

## Filament unload time

Time to unload old filament when switch filament. For statistics only

**Key:** `machine_unload_filament_time`

**Type:** `float`

**Default:** `0.0`

**Min:** `0`

## Manual Filament Change

Enable this option to omit the custom Change filament G-code only at the beginning of the print. The tool change command (e.g., T0) will be skipped throughout the entire print. This is useful for manual multi-material printing, where we use M600/PAUSE to trigger the manual filament change action.

**Key:** `manual_filament_change`

**Type:** `boolean`

**Default:** `null`

## Nozzle HRC

The nozzle's hardness. Zero means no checking for nozzle's hardness during slicing.

**Key:** `nozzle_hrc`

**Type:** `integer`

**Default:** `0`

**Max:** `500`

**Min:** `0`

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

## Nozzle volume

Volume of nozzle between the cutter and the end of nozzle

**Key:** `nozzle_volume`

**Type:** `float`

**Default:** `0.0`

## Filament parking position

Distance of the extruder tip from the position where the filament is parked when unloaded. This should match the value in printer firmware.

**Key:** `parking_pos_retraction`

**Type:** `float`

**Default:** `92.0`

**Min:** `0`

## Hostname, IP or URL

Slic3r can upload G-code files to a printer host. This field should contain the hostname, IP address or URL of the printer host instance. Print host behind HAProxy with basic auth enabled can be accessed by putting the user name and password into the URL in the following format: https://username:password@your-octopi-address/

**Key:** `print_host`

**Type:** `string`

**Default:** (empty)

## Device UI

Specify the URL of your device user interface if it's not same as print_host

**Key:** `print_host_webui`

**Type:** `string`

**Default:** (empty)

## Printable area

**Key:** `printable_area`

**Type:** `[[integer, integer]]`

**Default:** `[[0, 0], [200, 0], [200, 200], [0, 200]]`

## Printable height

Maximum printable height which is limited by mechanism of printer

**Key:** `printable_height`

**Type:** `float`

**Default:** `100.0`

**Max:** `2000`

**Min:** `0`

## Printer type

Type of the printer

**Key:** `printer_model`

**Type:** `string`

**Default:** `null`

## Printer notes

You can put your notes regarding the printer here.

**Key:** `printer_notes`

**Type:** `string`

**Default:** (empty)

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

## Printer technology

Printer technology

**Key:** `printer_technology`

**Type:** `enum`

**Default:** `FFF`

**Values:**
* `FFF`
* `SLA`

## Printer variant

Name of the printer variant. For example, the printer variants may be differentiated by a nozzle diameter.

**Key:** `printer_variant`

**Type:** `string`

**Default:** `null`

## API Key / Password

Slic3r can upload G-code files to a printer host. This field should contain the API Key or the password required for authentication.

**Key:** `printhost_apikey`

**Type:** `string`

**Default:** (empty)

## Authorization Type

**Key:** `printhost_authorization_type`

**Type:** `enum`

**Default:** `key`

**Values:**
* **API key**: `key`
* **HTTP digest**: `user`

## HTTPS CA File

Custom CA certificate file can be specified for HTTPS OctoPrint connections, in crt/pem format. If left blank, the default OS CA certificate repository is used.

**Key:** `printhost_cafile`

**Type:** `string`

**Default:** (empty)

## Password

**Key:** `printhost_password`

**Type:** `string`

**Default:** (empty)

## Printer

Name of the printer

**Key:** `printhost_port`

**Type:** `string`

**Default:** (empty)

## Ignore HTTPS certificate revocation checks

Ignore HTTPS certificate revocation checks in case of missing or offline distribution points. One may want to enable this option for self signed certificates if connection fails.

**Key:** `printhost_ssl_ignore_revoke`

**Type:** `boolean`

**Default:** `null`

## User

**Key:** `printhost_user`

**Type:** `string`

**Default:** (empty)

## Purge in prime tower

Purge remaining filament into prime tower

**Key:** `purge_in_prime_tower`

**Type:** `boolean`

**Default:** `true`

## On surfaces

Enforce Z Hop behavior. This setting is impacted by the above settings (Only lift Z above/below).

**Key:** `retract_lift_enforce`

**Type:** `[enum]`

**Default:** `All Surfaces`

**Values:**
* **All Surfaces**: `All Surfaces`
* **Top Only**: `Top Only`
* **Bottom Only**: `Bottom Only`
* **Top and Bottom**: `Top and Bottom`

## Scan first layer

Enable this to enable the camera on printer to check the quality of first layer

**Key:** `scan_first_layer`

**Type:** `boolean`

**Default:** `null`

## Supports silent mode

Whether the machine supports silent mode in which machine use lower acceleration to print

**Key:** `silent_mode`

**Type:** `boolean`

**Default:** `null`

## Single Extruder Multi Material

Use single nozzle to print multi filament

**Key:** `single_extruder_multi_material`

**Type:** `boolean`

**Default:** `true`

## Support air filtration

Enable this if printer support air filtration
G-code command: M106 P3 S(0-255)

**Key:** `support_air_filtration`

**Type:** `boolean`

**Default:** `true`

## Support control chamber temperature

This option is enabled if machine support controlling chamber temperature
G-code command: M141 S(0-255)

**Key:** `support_chamber_temp_control`

**Type:** `boolean`

**Default:** `true`

## Custom G-code

This G-code will be used as a custom code

**Key:** `template_custom_gcode`

**Type:** `string`

**Default:** (empty)

## G-code thumbnails

Picture sizes to be stored into a .gcode and .sl1 / .sl1s files, in the following format: "XxY, XxY, ..."

**Key:** `thumbnails`

**Type:** `[[integer, integer]]`

**Default:** `[[300, 300]]`

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

## Time cost

The printer cost per hour

**Key:** `time_cost`

**Type:** `float`

**Default:** `0`

**Min:** `0`

## Time lapse G-code

**Key:** `time_lapse_gcode`

**Type:** `string`

**Default:** (empty)

## upward compatible machine

**Key:** `upward_compatible_machine`

**Type:** `[string]`

**Default:** `null`

## Use firmware retraction

This experimental setting uses G10 and G11 commands to have the firmware handle the retraction. This is only supported in recent Marlin.

**Key:** `use_firmware_retraction`

**Type:** `boolean`

**Default:** `null`

## Use relative E distances

Relative extrusion is recommended when using "label_objects" option.Some extruders work better with this option unckecked (absolute extrusion mode). Wipe tower is only compatible with relative mode. It is always enabled on BambuLab printers. Default is checked

**Key:** `use_relative_e_distances`

**Type:** `boolean`

**Default:** `true`

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

## Z offset

This value will be added (or subtracted) from all the Z coordinates in the output G-code. It is used to compensate for bad Z endstop position: for example, if your endstop zero actually leaves the nozzle 0.3mm far from the print bed, set this to -0.3 (or fix your endstop).

**Key:** `z_offset`

**Type:** `float`

**Default:** `0`

