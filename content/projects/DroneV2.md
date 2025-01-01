---
title: Drone V2
featured_image: /images/dronev2/regionals_frame_red.jpg
type: page
---
# Quick Info
This is the continuation of last year's [drone](./dronev1). This time, it's actually good (it's not finished yet). This is for the 2024-25 TSA competition. This year's goal is to be able to pick up little toy dinosaurs or caged dinosaurs. The more you can pick up and transport, the more points you get. The drone flying and picking up the payloads is worth 60 out of the 180 total points. Once again, documentation is two-thirds of your score. This page is still a work in progress as this year's drone is still in progress, but so far it's already better than last year's. I recommend at least skimming over the [page](./dronev1) for last year's drone to get a better understanding of this year's.

# So what changed?
A lot! The entire design has changed and so have the parts! I have a goal to model every part, at least to the right size so that I know everything will fit.
![](/images/dronev2/newdronedesign_regionals.png)

## New design choices
Last year's frame had some problems... Detachable arms? A wire cover? A claw that required servo motors to be melted to the frame? This was awful. To be fair though, I had only taken an Intro to Engineering class that only briefly went over Solidworks. I didn't know how to make to best design decisions for an engineering project. I did learn a lot last year though and have taken many ideas into a new design. I did this from scratch because I realized the old frame had a lot of weird design choices and I didn't like how I made it. I also prioritized making sure everything fit right. No more melting and drilling holes into the frame, it just works. This also means I have a lot of frames printed that only have minor differences, but I think this is better.

## The main frame
The new frame is one piece, no more melting arms onto the square base. It's also smaller, only 6.87 inches (174.5 mm) across and 9.23 inches (234.5 mm) diagonal. I can be printed on almost every 3D printer in one piece. The holes for the motors have also been changed so that the wires point toward the center. I also added quite a few holes to be able to add expansions to the base frame. I have ideas for a propeller guard, but some of these holes are currently used for zip ties and other pieces of the whole frame. I also moves the onboard flight controller to the top of the board so that I can make the battery cage smaller.
![](/images/dronev2/newframe_regionals.png)

## The battery cage
I still kept the battery cage because it makes it easy to attach a claw to the bottom. Inside the cage is room for the battery as well as the receiver. The design only looks different from last year's but still has the same purpose.

## The Claw
We still need a claw and I quite like the design I made last year. This time I tried to make it better suited for picking up toy dinosaurs by their head. I don't think I did a good job though. This is still very much a work in progress. I also added a mount for the servo motors so that they aren't just melted to the frame this time.

## New and changed parts
There are only a few parts we kept from last year's drone. Last year's drone was big and had big parts. I don't want big parts, I want a smaller drone. We have smaller motors, batteries, and ESCs. The motors are 2300KV and are smaller than our previous motors. The battery is now a 1500mAh 3S lipo. And all four ESCs were replaced by a 4 in 1 ESC. Sadly, since this is being constructed and tested after March 2024, we will need a remote ID transmitter. I want to make the drone light enough (<250 grams) to not need it, but I don't know if that will happen ☹️.

# Does it work?
It does! It still needs some configurating, but it already works.

## An important consideration
There are many regulations when it comes to flying drones. Our drone has to comply with FAA regulations or we could get fined. Remote ID is now required for drones weighing over 250 grams (ours is around 500 grams) so our drone does have a remote ID module. The airspace our drone was flown in allowed drone flight with no restrictions, but always check with your local authority. We have followed all safety and FAA regulations when flying our drone. I am not a legal expert, nothing I say is legal advice. I take no liability or responsibility for the actions you do. Always check with a lawyer or your local authority to get a complete understanding of if what you're doing is legal.

## Test flights
So far we have done two test flights. The first was successful showing off that the new parts work and that it can fly. (The person recording had an old iPhone so the quality is awful)
![](/images/dronev2/first_flight.png)
This flight only went a couple of feet off the ground, but it still flew and was stable. We have done one other flight since then and it was both successful and unfortunate. The person controlling the drone this time full throttled the motors and turned it to the right.
![](/images/dronev2/itgoesup.png)
![](/images/dronev2/itgoesdown.png)
The drone hit the brick pillar in front of my school and crashed. Luckily only the frame broke so we only had to print a new one.
![](/images/dronev2/drone_crash_1.png)

# Final Parts List
So far, here are the parts used for this drone
- ReadyToSky 2300KV motors (4x)
	- Higher speed
	- Works good with our 3S lipo
- SpeedyBee F405 V4 & 55A 4in1 ESC
	- Betaflight has so many configuration options for this
	- We can configure the ESCs as well and the ESC board is the same size as the flight control board
- FrSky X8R 8-16 Channel Receiver (might be discontinued)
	- Had no problems, we used SBUS to receive our signal
- FrSky X9D transmitter (Discontinued)
	- OpenTX configurator was very annoying, or maybe that's because you can only find info about the pro version of this transmitter. This is the non pro version
- 12g Servos (2x)
	- Used for the claw
	- I had to hook these directly to the X8R receiver module
- 5 Inch tri Propellers (4x)
	- They worked
- Ruko R111 FAA compliant remote id module
	- Required to be FAA compliant ☹️
- Tenergy Lipo battery charger
	- Any lipo battery charger works
	- I chose this one so that we can charge other batteries for other projects as well
- 3D Printer with PLA or ABS plastic

# The Competition
So far my team and I have done the regional competition, the important state competition isn't for a couple months.

## The regional competition
Our drone was flying by this competition but the solder joint for the negative battery connector came off. It was destined to break, the ESC board has a big heat sink on it that instantly cools solder as soon as it touches it. This shows the board can handle the heat of the ESCs but also means it's hard to solder to. Because of this stupid issue, we couldn't fly the drone. We were still confident that our documentation could pull us through, but it didn't. The judge had never judged the drone competition so he didn't fully understand what to do. Only one other team's drone flew (even though they didn't put the net down and it almost hit someone four times) and so the judge said that only one team would place. Only that team got an award and 2nd and 3rd place didn't get anything. We later found out that we got 5th place, but I don't agree with that. For the state competition, these issues will be fixed and I hope to get top three. (Knock on wood)

## The state competition
You'll have to wait until after February 2025 when I (hopefully) update this page.