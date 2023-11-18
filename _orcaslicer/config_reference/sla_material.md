---
layout: default
title: "SLA Material"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Material"
---

Configuration options for a configuration file in the `sla_materials` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## Material cost

Material cost

**Key:** `bottle_cost`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"bottle_cost": 4.45
```


## Bottle volume

Bottle volume

**Key:** `bottle_volume`

**Type:** `Float`

**Min:** `50`

**Default** `1000.0`

### Example

```json
"bottle_volume": 887.6
```


## Bottle weight

Bottle weight

**Key:** `bottle_weight`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"bottle_weight": 0.85
```


## Compatible machine

[No documentation provided]

**Key:** `compatible_printers`

**Type:** `Strings`

**Default** `[]`

### Example

```json

```


## Compatible machine condition

A boolean expression using the configuration values of an active printer profile. If this expression evaluates to true, this profile is considered compatible with the active printer profile.

**Key:** `compatible_printers_condition`

**Type:** `String`

**Default** ``

### Example

```json
"compatible_printers_condition": "printer_model==\"PHOTON MONO SE"
```


## Compatible process profiles

[No documentation provided]

**Key:** `compatible_prints`

**Type:** `Strings`

**Default** `[]`

### Example

```json

```


## Compatible process profiles condition

A boolean expression using the configuration values of an active print profile. If this expression evaluates to true, this profile is considered compatible with the active print profile.

**Key:** `compatible_prints_condition`

**Type:** `String`

**Default** ``

### Example

```json
"compatible_prints_condition": "layer_height == 0.1"
```


## Default SLA material profile

Default material profile associated with the current printer profile. On selection of the current printer profile, this material profile will be activated.

**Key:** `default_sla_material_profile`

**Type:** `String`

**Default** ``

### Example

```json

```


## Exposure time

Exposure time

**Key:** `exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `10`

### Example

```json
"exposure_time": 1.2
```


## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `String`

**Default** ``

### Example

```json
"inherits": "*common 0.035*"
```


## Initial exposure time

Initial exposure time

**Key:** `initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `15`

### Example

```json
"initial_exposure_time": 50
```


## Initial layer height

Initial layer height

**Key:** `initial_layer_height`

**Type:** `Float`

**Min:** `0`

**Default** `0.3`

### Example

```json
"initial_layer_height": 0.1
```


## Material color

This is only used in the user interface as a visual help.

**Key:** `material_colour`

**Type:** `String`

**Default** `#29B2B2`

### Example

```json
"material_colour": "#3AD200"
```


## Correction for expansion

Correction for expansion

**Key:** `material_correction`

**Type:** `Floats`

**Min:** `0`

**Default** `[1.0, 1.0, 1.0]`

### Example

```json
"material_correction": "1,1,1"
```


## Correction for expansion in X axis

Correction for expansion in X axis

**Key:** `material_correction_x`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_correction_x": 1.22
```


## Correction for expansion in Y axis

Correction for expansion in Y axis

**Key:** `material_correction_y`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_correction_y": 1.18
```


## Correction for expansion in Z axis

Correction for expansion in Z axis

**Key:** `material_correction_z`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_correction_z": 0.82
```


## Material density

Material density

**Key:** `material_density`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_density": 0.94
```


## Print speed

A slower printing profile might be necessary when using materials with higher viscosity or with some hollowed parts. It slows down the tilt movement and adds a delay before exposure.

**Key:** `material_print_speed`

**Type:** `Enum`

**Default** `slamsFast`

**Enum values:**


### Example

```json
"material_print_speed": "slow"
```


## SLA material type

SLA material type

**Key:** `material_type`

**Type:** `String`

**Default** `Tough`

**Enum values:**


### Example

```json
"material_type": "Plant-Based"
```


## Material vendor

[No documentation provided]

**Key:** `material_vendor`

**Type:** `String`

**Default** ``

### Example

```json
"material_vendor": "Peopoly"
```


## Name

[No documentation provided]

**Key:** `name`

**Type:** `String`

**Default** ``

### Example

```json
"name": "MakerJuice Labs Standard Red @0.025"
```
