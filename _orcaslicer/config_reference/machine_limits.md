---
layout: default
title: "Machine Limits"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "Machine Limits"
---

Configuration options for a configuration file with `"type": "machine"`.


## Machine max acceleration e

Maximum acceleration of E axis

**Key:** `machine_max_acceleration_e`

**Type:** `Floats`

**Min:** `0`

**Default** `[5000.0, 5000.0]`

### Example

```json
"machine_max_acceleration_e": [
    4051.38,
    4101.1,
    4050.57,
    4146.04,
    4133.92
  ]
```


## Machine max acceleration extruding

Maximum acceleration for extruding (M204 P)

**Key:** `machine_max_acceleration_extruding`

**Type:** `Floats`

**Min:** `0`

**Default** `[1500.0, 1250.0]`

### Example

```json
"machine_max_acceleration_extruding": [
    1191.49,
    1457.28
  ]
```


## Machine max acceleration retracting

Maximum acceleration for retracting (M204 R)

**Key:** `machine_max_acceleration_retracting`

**Type:** `Floats`

**Min:** `0`

**Default** `[1500.0, 1250.0]`

### Example

```json
"machine_max_acceleration_retracting": [
    1223.98,
    1238.96,
    1152.2
  ]
```


## Machine max acceleration travel

Maximum acceleration for travel (M204 T), it only applies to Marlin 2

**Key:** `machine_max_acceleration_travel`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0, 0.0]`

### Example

```json
"machine_max_acceleration_travel": [
    4.88,
    3.34,
    1.61
  ]
```


## Machine max acceleration x

Maximum acceleration of X axis

**Key:** `machine_max_acceleration_x`

**Type:** `Floats`

**Min:** `0`

**Default** `[1000.0, 1000.0]`

### Example

```json
"machine_max_acceleration_x": [
    784.75
  ]
```


## Machine max acceleration y

Maximum acceleration of Y axis

**Key:** `machine_max_acceleration_y`

**Type:** `Floats`

**Min:** `0`

**Default** `[1000.0, 1000.0]`

### Example

```json
"machine_max_acceleration_y": [
    967.11,
    817.56
  ]
```


## Machine max acceleration z

Maximum acceleration of Z axis

**Key:** `machine_max_acceleration_z`

**Type:** `Floats`

**Min:** `0`

**Default** `[500.0, 200.0]`

### Example

```json
"machine_max_acceleration_z": [
    407.26,
    417.83,
    271.21,
    386.66,
    282.68
  ]
```


## Machine max jerk e

Maximum jerk of E axis

**Key:** `machine_max_jerk_e`

**Type:** `Floats`

**Min:** `0`

**Default** `[2.5, 2.5]`

### Example

```json
"machine_max_jerk_e": [
    1.97,
    2.03,
    2.07
  ]
```


## Machine max jerk x

Maximum jerk of X axis

**Key:** `machine_max_jerk_x`

**Type:** `Floats`

**Min:** `0`

**Default** `[10.0, 10.0]`

### Example

```json
"machine_max_jerk_x": [
    8.69,
    8.37,
    8.32,
    8.22
  ]
```


## Machine max jerk y

Maximum jerk of Y axis

**Key:** `machine_max_jerk_y`

**Type:** `Floats`

**Min:** `0`

**Default** `[10.0, 10.0]`

### Example

```json
"machine_max_jerk_y": [
    8.7,
    9.86,
    9.27,
    8.74
  ]
```


## Machine max jerk z

Maximum jerk of Z axis

**Key:** `machine_max_jerk_z`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.2, 0.4]`

### Example

```json
"machine_max_jerk_z": [
    0.33,
    0.36,
    0.27,
    0.27,
    0.28
  ]
```


## Machine max speed e

Maximum speed of E axis

**Key:** `machine_max_speed_e`

**Type:** `Floats`

**Min:** `0`

**Default** `[120.0, 120.0]`

### Example

```json
"machine_max_speed_e": [
    114.55,
    90.31,
    115.91,
    104.29
  ]
```


## Machine max speed x

Maximum speed of X axis

**Key:** `machine_max_speed_x`

**Type:** `Floats`

**Min:** `0`

**Default** `[500.0, 200.0]`

### Example

```json
"machine_max_speed_x": [
    305.48,
    266.53,
    377.18
  ]
```


## Machine max speed y

Maximum speed of Y axis

**Key:** `machine_max_speed_y`

**Type:** `Floats`

**Min:** `0`

**Default** `[500.0, 200.0]`

### Example

```json
"machine_max_speed_y": [
    308.46,
    427.11,
    432.62,
    416.41
  ]
```


## Machine max speed z

Maximum speed of Z axis

**Key:** `machine_max_speed_z`

**Type:** `Floats`

**Min:** `0`

**Default** `[12.0, 12.0]`

### Example

```json
"machine_max_speed_z": [
    10.78,
    9.02,
    11.27,
    10.19,
    9.66
  ]
```


## Machine min extruding rate

Minimum speed for extruding (M205 S)

**Key:** `machine_min_extruding_rate`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0, 0.0]`

### Example

```json
"machine_min_extruding_rate": [
    2.17,
    1.67,
    0.29,
    3.57,
    3.98
  ]
```


## Machine min travel rate

Minimum travel speed (M205 T)

**Key:** `machine_min_travel_rate`

**Type:** `Floats`

**Min:** `0`

**Default** `[0.0, 0.0]`

### Example

```json
"machine_min_travel_rate": [
    4.82,
    1.89,
    4.23
  ]
```
