---
layout: default
title: "SLA Material"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Material"
---

Configuration options for a configuration file in the `sla_materials` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## Bottle cost

[No documentation provided]

**Key:** `bottle_cost`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"bottle_cost": 1.45
```


## Bottle volume

[No documentation provided]

**Key:** `bottle_volume`

**Type:** `Float`

**Min:** `50`

**Default** `1000.0`

### Example

```json
"bottle_volume": 818.28
```


## Bottle weight

[No documentation provided]

**Key:** `bottle_weight`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"bottle_weight": 1.12
```


## Compatible machine

[No documentation provided]

**Key:** `compatible_printers`

**Type:** `Strings`

**Default** `[]`

### Example

```json
"compatible_printers": [""]
```


## Compatible machine condition

A boolean expression using the configuration values of an active printer profile. If this expression evaluates to true, this profile is considered compatible with the active printer profile.

**Key:** `compatible_printers_condition`

**Type:** `String`

**Default** ``

### Example

```json
"compatible_printers_condition": ""
```


## Compatible process profiles

[No documentation provided]

**Key:** `compatible_prints`

**Type:** `Strings`

**Default** `[]`

### Example

```json
"compatible_prints": [""]
```


## Compatible process profiles condition

A boolean expression using the configuration values of an active print profile. If this expression evaluates to true, this profile is considered compatible with the active print profile.

**Key:** `compatible_prints_condition`

**Type:** `String`

**Default** ``

### Example

```json
"compatible_prints_condition": ""
```


## Default sla material profile

[No documentation provided]

**Key:** `default_sla_material_profile`

**Type:** `String`

**Default** ``

### Example

```json
"default_sla_material_profile": ""
```


## Exposure time

[No documentation provided]

**Key:** `exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `10`

### Example

```json
"exposure_time": 10.05
```


## Initial exposure time

[No documentation provided]

**Key:** `initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `15`

### Example

```json
"initial_exposure_time": 18.14
```


## Initial layer height

[No documentation provided]

**Key:** `initial_layer_height`

**Type:** `Float`

**Min:** `0`

**Default** `0.3`

### Example

```json
"initial_layer_height": 0.25
```


## Material colour

[No documentation provided]

**Key:** `material_colour`

**Type:** `String`

**Default** `#29B2B2`

### Example

```json
"material_colour": ""
```


## Material correction

[No documentation provided]

**Key:** `material_correction`

**Type:** `Floats`

**Min:** `0`

**Default** `[1.0, 1.0, 1.0]`

### Example

```json
"material_correction": [
    0.89,
    0.75,
    0.9
  ]
```


## Material correction x

[No documentation provided]

**Key:** `material_correction_x`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_correction_x": 0.86
```


## Material correction y

[No documentation provided]

**Key:** `material_correction_y`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_correction_y": 1.01
```


## Material correction z

[No documentation provided]

**Key:** `material_correction_z`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_correction_z": 0.88
```


## Material density

[No documentation provided]

**Key:** `material_density`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"material_density": 1.1
```


## Material print speed

[No documentation provided]

**Key:** `material_print_speed`

**Type:** `Enum`

**Default** `slamsFast`

**Enum values:**


### Example

```json
"material_print_speed": "slow"
```


## Material type

[No documentation provided]

**Key:** `material_type`

**Type:** `String`

**Default** `Tough`

**Enum values:**


### Example

```json
"material_type": ""
```


## Material vendor

[No documentation provided]

**Key:** `material_vendor`

**Type:** `String`

**Default** ``

### Example

```json
"material_vendor": ""
```
