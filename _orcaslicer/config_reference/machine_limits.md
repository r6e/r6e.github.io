---
layout: default
title: "Machine Limits"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "Machine Limits"
---

Configuration options used in multiple places, but usually `"type": "printer"`

## Maximum acceleration for extruding

Maximum acceleration for extruding (M204 P)

**Key:** `machine_max_acceleration_extruding`

**Type:** `[float]`

**Default:** `[1500.0, 1250.0]`

**Min:** `0`

## Maximum acceleration for retracting

Maximum acceleration for retracting (M204 R)

**Key:** `machine_max_acceleration_retracting`

**Type:** `[float]`

**Default:** `[1500.0, 1250.0]`

**Min:** `0`

## Maximum acceleration for travel

Maximum acceleration for travel (M204 T), it only applies to Marlin 2

**Key:** `machine_max_acceleration_travel`

**Type:** `[float]`

**Default:** `[0.0, 0.0]`

**Min:** `0`

## Maximum acceleration X

Maximum acceleration of the X axis

**Key:** `machine_max_acceleration_x`

**Type:** `[float]`

**Default:** `[1000.0, 1000.0]`

**Min:** `0`

## Maximum acceleration Y

Maximum acceleration of the Y axis

**Key:** `machine_max_acceleration_y`

**Type:** `[float]`

**Default:** `[1000.0, 1000.0]`

**Min:** `0`

## Maximum acceleration Z

Maximum acceleration of the Z axis

**Key:** `machine_max_acceleration_z`

**Type:** `[float]`

**Default:** `[500.0, 200.0]`

**Min:** `0`

## Maximum acceleration E

Maximum acceleration of the E axis

**Key:** `machine_max_acceleration_e`

**Type:** `[float]`

**Default:** `[5000.0, 5000.0]`

**Min:** `0`

## Maximum jerk X

Maximum jerk of the X axis

**Key:** `machine_max_jerk_x`

**Type:** `[float]`

**Default:** `[10.0, 10.0]`

**Min:** `0`

## Maximum jerk Y

Maximum jerk of the Y axis

**Key:** `machine_max_jerk_y`

**Type:** `[float]`

**Default:** `[10.0, 10.0]`

**Min:** `0`

## Maximum jerk Z

Maximum jerk of the Z axis

**Key:** `machine_max_jerk_z`

**Type:** `[float]`

**Default:** `[0.2, 0.4]`

**Min:** `0`

## Maximum jerk E

Maximum jerk of the E axis

**Key:** `machine_max_jerk_e`

**Type:** `[float]`

**Default:** `[2.5, 2.5]`

**Min:** `0`

## Maximum speed X

Maximum speed of the X axis

**Key:** `machine_max_speed_x`

**Type:** `[float]`

**Default:** `[500.0, 200.0]`

**Min:** `0`

## Maximum speed Y

Maximum speed of the Y axis

**Key:** `machine_max_speed_y`

**Type:** `[float]`

**Default:** `[500.0, 200.0]`

**Min:** `0`

## Maximum speed Z

Maximum speed of the Z axis

**Key:** `machine_max_speed_z`

**Type:** `[float]`

**Default:** `[12.0, 12.0]`

**Min:** `0`

## Maximum speed E

Maximum speed of the E axis

**Key:** `machine_max_speed_e`

**Type:** `[float]`

**Default:** `[120.0, 120.0]`

**Min:** `0`

## Minimum speed for extruding

Minimum speed for extruding (M205 S)

**Key:** `machine_min_extruding_rate`

**Type:** `[float]`

**Default:** `[0.0, 0.0]`

**Min:** `0`

## Minimum travel speed

Minimum travel speed (M205 T)

**Key:** `machine_min_travel_rate`

**Type:** `[float]`

**Default:** `[0.0, 0.0]`

**Min:** `0`
