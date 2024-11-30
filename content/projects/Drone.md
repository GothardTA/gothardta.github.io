---
title: Drone V1
---
# Quick Info
This is a UAV drone primarily built by me with the help from my friends. This drone was built for the Technology Student Association (TSA) competition. The goal of this competition was to be able to fly through obstacles while transporting payloads. The more payloads you transported successfully, the more points you get. The counts toward your overall placement against other teams. This drone was built during the 2023-2024 school year and semi-finaled at the Colorado state competition in 2024.

## The drone's development history - our initial parts
 This all started as an idea, a thought, a cool concept. But I never would have though I'd get this far. One of my friends helping with this project found a $20 drone and controller combo at a garage sale. It was sold as 'not tested', and that was later proven, some of the parts weren't the best. After taking it apart and looking at the individual pieces, we found out that the parts were from ~2012.
 
### The onboard flight controller
The $20 drone came with a flight controller, it was old but we didn't want to get a new one. We had to use some older software to get it working. This software was LibrePilot. While it looked new and supported everything the flight controller had to offer, it had some bugs. We got everything configured using this software and it mostly worked... (why does it full ... when the controller is ... ?!)

### The battery
It didn't come with a battery to start with so we knew we had to get one quick. We didn't know what kind of battery to get, "they all use lipo, we should probably use that". But wait, there are different cell counts, c ratings (still don't really care about that) capacities, etc. We looked at our components, the minimum was a 2s and the max was a 6s. We though a 6s would be good as it gives the highest voltage.

### The motors
The motors it came with had a number on it, '980 kv', what's a kv? Turns out (from what I found) this means these motors are lower speed and higher torque. The choice to get a 6s battery was actually a good decision because it allowed us to use smaller props while still being able to fly. We didn't want to buy newer motors either so we kept these. "If it ain't broke, don't fix it" - every engineer
### The motor esc's
The original drone also had escs with it. Just plug the pwm wire into the flight controller and the power wires into the battery and your good. We had to make a bus bar, if you could call it that. It worked though, so I don't care if it looks a little sketchy.

### The controller and receiver
The controller with the original drone was ok. It was included in the original $20 purchase with a nice case for it. It worked with the receiver as well and had no problems. It has sbus support so we could use just three wires to receive all eight channels. Just 5V, ground, and data wires to the flight controller. Along with dog teeth marks on one of the antennas, this worked good. 