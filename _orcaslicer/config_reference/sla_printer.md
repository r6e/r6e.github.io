---
layout: default
title: "SLA Printer"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Printer"
---

Configuration options for a configuration file for an SLA printer in the `machine` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## Absolute correction

[No documentation provided]

**Key:** `absolute_correction`

**Type:** `Float`

**Default** `0.0`

### Example

```json
"absolute_correction": 2.24
```


## Area fill

[No documentation provided]

**Key:** `area_fill`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"area_fill": 55.31
```


## Bed custom model

[No documentation provided]

**Key:** `bed_custom_model`

**Type:** `String`

**Default** ``

### Example

```json
"bed_custom_model": ""
```


## Bed custom texture

[No documentation provided]

**Key:** `bed_custom_texture`

**Type:** `String`

**Default** ``

### Example

```json
"bed_custom_texture": ""
```


## Display height

[No documentation provided]

**Key:** `display_height`

**Type:** `Float`

**Min:** `1`

**Default** `68.0`

### Example

```json
"display_height": 80.47
```


## Display mirror x

[No documentation provided]

**Key:** `display_mirror_x`

**Type:** `Bool`

**Default** `true`

### Example

```json
"display_mirror_x": true
```


## Display mirror y

[No documentation provided]

**Key:** `display_mirror_y`

**Type:** `Bool`

**Default** `false`

### Example

```json
"display_mirror_y": false
```


## Display orientation

[No documentation provided]

**Key:** `display_orientation`

**Type:** `Enum`

**Default** `sladoPortrait`

**Enum values:**


### Example

```json
"display_orientation": "landscape"
```


## Display pixels X

[No documentation provided]

**Key:** `display_pixels_x`

**Type:** `Int`

**Min:** `100`

**Default** `2560`

### Example

```json
"display_pixels_x": 2154
```


## Display pixels Y

[No documentation provided]

**Key:** `display_pixels_y`

**Type:** `Int`

**Min:** `100`

**Default** `1440`

### Example

```json
"display_pixels_y": 1592
```


## Display width

[No documentation provided]

**Key:** `display_width`

**Type:** `Float`

**Min:** `1`

**Default** `120.0`

### Example

```json
"display_width": 131.86
```


## Elephant foot compensation

Shrink the initial layer on build plate to compensate for elephant foot effect

**Key:** `elefant_foot_compensation`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"elefant_foot_compensation": 4.67
```


## Elefant foot min width

[No documentation provided]

**Key:** `elefant_foot_min_width`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"elefant_foot_min_width": 0.19
```


## Fast tilt time

[No documentation provided]

**Key:** `fast_tilt_time`

**Type:** `Float`

**Min:** `0`

**Default** `5.0`

### Example

```json
"fast_tilt_time": 6.19
```


## Gamma correction

[No documentation provided]

**Key:** `gamma_correction`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `1.0`

### Example

```json
"gamma_correction": 0.91
```


## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `String`

**Default** ``

### Example

```json
"inherits": ""
```


## Max exposure time

[No documentation provided]

**Key:** `max_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `100`

### Example

```json
"max_exposure_time": 103.55
```


## Max initial exposure time

[No documentation provided]

**Key:** `max_initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `150`

### Example

```json
"max_initial_exposure_time": 117.46
```


## Min exposure time

[No documentation provided]

**Key:** `min_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"min_exposure_time": 1.91
```


## Min initial exposure time

[No documentation provided]

**Key:** `min_initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"min_initial_exposure_time": 2.56
```


## Printable area

[No documentation provided]

**Key:** `printable_area`

**Type:** `Points`

**Default** `[[0, 0], [200, 0], [200, 200], [0, 200]]`

### Example

```json
"printable_area": [
    [
      119.36,
      84.75
    ]
  ]
```


## Printable height

Maximum printable height which is limited by mechanism of printer

**Key:** `printable_height`

**Type:** `Float`

**Min:** `0`

**Max:** `2000`

**Default** `100.0`

### Example

```json
"printable_height": 110.26
```


## Printer technology

Printer technology

**Key:** `printer_technology`

**Type:** `Enum`

**Default** `FFF`

**Enum values:**


### Example

```json
"printer_technology": "FFF"
```


## Relative correction

[No documentation provided]

**Key:** `relative_correction`

**Type:** `Floats`

**Min:** `0`

**Default** `[1.0, 1.0]`

### Example

```json
"relative_correction": [
    0.96,
    0.97,
    0.95
  ]
```


## Relative correction x

[No documentation provided]

**Key:** `relative_correction_x`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_x": 0.86
```


## Relative correction y

[No documentation provided]

**Key:** `relative_correction_y`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_y": 0.87
```


## Relative correction z

[No documentation provided]

**Key:** `relative_correction_z`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_z": 1.03
```


## Slow tilt time

[No documentation provided]

**Key:** `slow_tilt_time`

**Type:** `Float`

**Min:** `0`

**Default** `8.0`

### Example

```json
"slow_tilt_time": 9.35
```
