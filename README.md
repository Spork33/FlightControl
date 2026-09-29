# System Overview

## Objective

Collect relevant flight data aboard an RC aircraft and transmit the data
wirelessly to a ground station.

## Aircraft System

The aircraft uses a SpeedyBee F405 Wing Mini running ArduPlane.

ArduPlane is responsible for reading sensors, processing flight
information, logging data, and generating MAVLink telemetry.

## Project Criteria

The system is intended to provide:

- Battery level
- Battery temperature
- Power draw
- Altitude
- Airspeed
- General temperature
- GPS position
- IMU data
- Microcontroller
- Wireless communication

Additional measurements include:

- Ground proximity
- Angle of attack

Angle of attack is the dynamic angle between the wing's chord line
and the relative wind.

## Measurements Covered by the Wing Mini

The SpeedyBee F405 Wing Mini already provides hardware that can be
used for several of the project requirements:

- Battery voltage sensing
- Current sensing
- Barometer
- IMU
- Microcontroller
- Wireless capability

These capabilities reduce the amount of additional hardware required
for the telemetry system.

## External Sensors Required

The following measurements require additional sensors or hardware:

- GPS position
- Airspeed
- Battery temperature
- General / ambient temperature
- Ground proximity
- Angle of attack

### GPS

An external GPS module will be used to determine the aircraft's
position during flight.

### Airspeed

An external airspeed sensor and pitot tube will be used to measure
the aircraft's airspeed.

### Temperature

External temperature sensing will be required for battery temperature
and general ambient temperature.

### Ground Proximity

An external range sensor will be required to determine the aircraft's
distance from the ground.

### Angle of Attack

An external or custom sensor will be required to measure the angle
between the wing's chord line and the relative airflow.

## Telemetry

ArduPlane generates MAVLink telemetry from the available flight data.

The telemetry system will transmit MAVLink data wirelessly from the
aircraft to the ground station.

## Ground Station

The ground station consists of:

- Wireless receiver
- Computer
- Mission Planner

Mission Planner will initially be used to display and record telemetry.

## Data Flow

Built-In Sensors + External Sensors
|
v
SpeedyBee F405 Wing Mini
|
v
ArduPlane
|
v
MAVLink
|
v
Wireless Transmission
|
v
Ground Station
|
v
Mission Planner
