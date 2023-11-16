---
layout: default
title: "Machine Limits"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "Machine Limits"
---

Configuration options for a configuration file with `"type": "machine"`.


## Maximum acceleration E

Maximum acceleration of E axis

**Key:** `machine_max_acceleration_e`

**Type:** `Floats`

**Min:** `0`

**Default** `[5000.0, 5000.0]`

### Example

```json
"machine_max_acceleration_e": [
    4874.85,
    4684.16
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
"machine_max_acceleration_extruding": [
    1153.28,
    1039.11
  ]
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
    1365.46,
    1390.95
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
"machine_max_acceleration_travel": [
    3.01,
    0.09
  ]
```


## Maximum acceleration X

Maximum acceleration of X axis

**Key:** `machine_max_acceleration_x`

**Type:** `Floats`

**Min:** `0`

**Default** `[1000.0, 1000.0]`

### Example

```json
"machine_max_acceleration_x": [
    985.0,
    895.75
  ]
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
    966.69,
    822.93
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
    406.84,
    376.46
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
    1.99,
    2.29
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
    9.92,
    7.51
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
"machine_max_jerk_y": [
    8.92,
    9.01
  ]
```


## Maximum jerk Z

Maximum jerk of Z axis

**Key:** `machine_max_jerk_z`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.2, 0.4]`

### Example

```json
"machine_max_jerk_z": [
    0.33,
    0.31
  ]
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
    100.42,
    98.58
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
    316.84,
    313.76
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
    378.28,
    434.89
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
    11.65,
    9.1
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
"machine_min_extruding_rate": [
    4.86,
    4.74
  ]
```


## Minimum travel speed

Minimum travel speed (M205 T)

**Key:** `machine_min_travel_rate`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0, 0.0]`

### Example

```json
"machine_min_travel_rate": [
    2.4,
    4.88
  ]
```
