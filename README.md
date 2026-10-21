# spot voice navigation ₊˚⊹♡

voice-controlled autonomous navigation for Boston Dynamics Spot, built with GraphNav, NVIDIA Jetson, and the Spot SDK.

my summer research project at UNC–Chapel Hill! i worked on getting Spot to take spoken directions, match them to places on a saved map, and navigate there.

## about the project ✧

the current prototype uses a custom GraphNav map of Sitterson Hall. commands are processed on an NVIDIA Jetson, converted into text, and matched to saved destinations.

the goal is to make asking Spot to go somewhere feel more natural, starting with places like “the vending machines” or “room 014.” eventually, i’d love to expand this beyond Sitterson and have him navigate around campus.

## what he can do ♡

| part | what it handles |
| --- | --- |
| voice input | speech-to-text processing and hands-free commands |
| destination matching | connects different names for a place to its saved waypoint |
| navigation | loads the GraphNav map, localizes Spot, and navigates to the requested waypoint |
| command validation | checks the requested destination before navigation |
| direct movement | supports commands like turning and stopping |
| mapping | uses custom maps with saved waypoints, edges, and named destinations |

## how it works

a USB microphone picks up the command, and the Jetson converts it to text. the command parser identifies the destination and checks it against saved waypoint names and aliases.

from there, the system loads the GraphNav map, localizes Spot, and sends the navigation request through the Spot SDK.

## what i built ⋆｡°

my work focused on the backend connecting voice input to navigation:

- wrote the command parsing and destination matching logic
- managed the waypoint and edge data used by GraphNav
- automated map loading and localization
- connected speech recognition, command validation, and navigation through the Spot SDK
- organized the code so new commands and destinations could be added later

## things you can ask him

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

## where i’d like to take this ⊹

there’s still more i’d like to explore:

- navigating longer routes around campus
- moving between indoor and outdoor spaces
- exploring Google Maps integration
- understanding more ways of phrasing a request
- using context to interpret commands
- helping with tasks beyond getting from one place to another

## about this repo

this public repo documents the project and my contributions. **source code isn’t included** because the research code, robot configuration files, GraphNav maps, and lab infrastructure aren’t publicly distributable.

i’m happy to talk through the implementation, design decisions, and challenges along the way!

## research + acknowledgements ♡

developed in the **Experimental Engineering Lab at UNC–Chapel Hill**, with support from the **UNC Office for Undergraduate Research** through an **Accelerated Research Award**.

thank you to the Experimental Engineering Lab and UNC OUR for supporting this work, and to Boston Dynamics for the Spot SDK and GraphNav tools.

˚₊‧꒰ა ♡ ໒꒱‧₊˚
