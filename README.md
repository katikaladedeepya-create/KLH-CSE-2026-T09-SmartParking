# KLH-CSE-2026-T09-SmartParking
The Smart Parking Slot Availability and Entry Control System is an IoT-based solution for easy parking. Sensors detect slot status, while controller counts spaces and controls the entry gate. The gate opens when a slot is available and stays closed when the parking area is full. It can later use sensors, a microcontroller, display, and gate system.
# Design and Simulation of a Smart Parking Slot Availability and Entry Control System

## Project Overview

The Smart Parking Slot Availability and Entry Control System is a simple IoT-based approach designed to make parking easier, faster, and more organized.

The system detects whether parking slots are occupied or available using sensors. A controller reads the sensor states, counts the available parking spaces, and uses this information to control the entry gate. If at least one parking slot is available, the gate is allowed to open. If all parking slots are occupied, the gate remains closed and the system indicates that the parking area is full.

The project is initially designed as a simulation and can later be implemented using sensors, a microcontroller, a display, and a gate mechanism.

---

## Project Objectives

- Detect whether each parking slot is occupied.
- Display available and occupied parking slots clearly.
- Check parking availability before allowing vehicle entry.
- Open the entry gate only when a valid parking space is available.
- Reduce unnecessary waiting and searching for parking.
- Improve parking-space utilization.
- Provide a foundation for an IoT-based real-world parking system.

---

## Team Members

| S.No | Team Member Name | Registration / ID Number |
|------|------------------|--------------------------|
| 1 |  |  <Dedeepya>    |     | <2620030578> |
| 2 |  |    <Hasini>    |        | <2620030565> |
| 3 |  | <Siddharath>    |    | <2620030575> |
| 4 |  | <Sriram Karan>  |    | <2620030521> |

---

## Supervisor

**Supervisor Name:** <Supervisor Name>

---

## Abstract

The Smart Parking Slot Availability and Entry Control System is designed to automate parking-space monitoring and vehicle entry control. The system uses sensors to detect whether individual parking slots are occupied or available. A controller continuously reads the sensor states and calculates the number of free parking spaces.

When a vehicle reaches the entrance, the system checks the availability of parking spaces. If at least one slot is free, the entry gate is opened. If all slots are occupied, the gate remains closed and the system indicates that the parking area is full.

The proposed system can initially be tested through simulation before being implemented using physical components such as IR or ultrasonic sensors, Arduino or ESP32, a servo motor, and an LCD or LED display. The system can help reduce unnecessary waiting, manual checking, and searching for parking spaces.

The project provides a simple foundation for a smart parking solution that can later be expanded with features such as mobile notifications, vehicle identification, online booking, digital payments, cloud monitoring, and usage analytics.

---

## System Architecture

The proposed system follows the sequence:

Sensors → Controller → Decision → Display / Gate

### Main Components

1. **Parking Slot Sensors**
   - Detect whether each parking slot is occupied or available.

2. **Microcontroller / Control Logic**
   - Reads sensor states.
   - Counts available parking slots.
   - Makes the entry decision.

3. **Availability Display**
   - Displays the number of available slots.
   - Shows the parking status.

4. **Entry Gate**
   - Opens when parking space is available.
   - Remains closed when the parking area is full.

---

## Working Principle

The controller repeatedly reads the states of all parking slot sensors.

For simulation:

- `0` / `LOW` can represent one parking state.
- `1` / `HIGH` can represent the other parking state.

The controller counts the available parking spaces.

### Entry Control Logic

```text
Vehicle reaches entrance
        ↓
Read slot states
        ↓
Count available slots
        ↓
Is available slot > 0?
      /       \
    YES        NO
     ↓          ↓
Open Gate    Keep Gate Closed
     ↓          ↓
Vehicle       Wait / FULL
Parks
     ↓
Update Slot Status
