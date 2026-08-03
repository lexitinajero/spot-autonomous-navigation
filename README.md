# Voice Navigation Assistant for Boston Dynamics Spot

Voice-controlled autonomous navigation for the Boston Dynamics Spot robot using GraphNav, NVIDIA Jetson, and natural language voice commands.

## Overview

This project explores natural language interaction for the Boston Dynamics Spot robot. Spoken commands are processed on an NVIDIA Jetson, converted into text, matched to saved GraphNav waypoints, and executed through the Boston Dynamics Spot SDK to autonomously navigate to user-requested destinations.

The current prototype operates on a custom GraphNav map of Sitterson Hall at the University of North Carolina at Chapel Hill. The long-term vision is to develop Spot into an intelligent robotic assistant capable of navigating indoor and outdoor environments through natural language interaction.

---

## Features

### Voice Interface

- Natural language voice commands
- Speech-to-text processing
- Waypoint alias matching
- Hands-free robot interaction

### Navigation

- GraphNav localization
- Autonomous waypoint navigation
- Automatic GraphNav map loading
- Command validation
- Direct movement commands

### Mapping

- Custom GraphNav maps
- Waypoint and edge management
- Named destination database

---

## System Architecture

```text
USB Microphone
      ↓
NVIDIA Jetson
      ↓
Speech-to-Text
      ↓
Command Parser
      ↓
Waypoint & Alias Matching
      ↓
GraphNav Localization
      ↓
Navigation Planner
      ↓
Boston Dynamics Spot
```

---

## Engineering Contributions

My work focused on building the backend pipeline that connects voice input to autonomous robot navigation.

Key contributions included:

- Developing the command parsing and destination matching logic.
- Managing waypoint and edge data used by GraphNav.
- Automating GraphNav map loading and localization.
- Building the backend workflow connecting speech recognition, navigation, and the Spot SDK.
- Designing a modular architecture for future expansion.

---

## Example Commands

```text
take me to upper lobby
go to room 014
take me to outside elevator
go to the hallway
go to the vending machines
take me to the bottom stairs
turn left
turn around
stop
```

---

## Future Work

Future development includes:

- Campus-scale autonomous navigation
- Indoor-to-outdoor route planning
- Google Maps integration
- More intelligent natural language understanding
- Context-aware navigation
- Task-oriented robotic assistance

---

## Repository Notice

> **Source code is not included in this public repository.**
>
> This project was developed within a university robotics research environment and contains research related source code, robot configuration files, GraphNav maps, and infrastructure that are not publicly distributable.
>
> This repository is intended to document the project's architecture and my engineering contributions. I would be happy to discuss the implementation, design decisions, and technical challenges.

---

## Research

This project is being developed in the **Experimental Engineering Lab** at the **University of North Carolina at Chapel Hill**.

Supported by the **UNC Office for Undergraduate Research (OUR)** through an **Accelerated Research Award**.

---

## Acknowledgements

- Experimental Engineering Lab, University of North Carolina at Chapel Hill
- UNC Office for Undergraduate Research
- Boston Dynamics for providing the Spot SDK and GraphNav tools
