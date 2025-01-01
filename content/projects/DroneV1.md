---
title: Drone V1
featured_image: /images/dronev1/drone_competition_2024.png
type: page
---
# Quick Info
This is a UAV drone primarily built by me with the help of my friends. This drone was built for the Technology Student Association (TSA) competition. The goal of this competition was to be able to fly through obstacles while transporting payloads. The more payloads you transport successfully, the more points you get. This is worth 60 out of the 180 points to place teams. The other 120 points are from your documentation. This drone was built during the 2023-2024 school year and semi-final at the Colorado state competition in 2024.

# The drone's development history - our initial parts
This all started as an idea, a thought, a cool concept. But I never would have though I'd get this far. One of my friends helping with this project found a $20 drone and controller combo at a garage sale. It was sold as 'not tested', and that was later proven, some of the parts weren't the best. After taking it apart and looking at the individual pieces, I found out that the parts were from ~2012.
 
## The onboard flight controller
The $20 drone came with a flight controller, it was old but we didn't want to get a new one. We had to use some older software to get it working. This software was LibrePilot. While it looked new and supported everything the flight controller had to offer, it had some bugs. We got everything configured using this software and it mostly worked... (why does it full ... when the controller is ... ?!)

## The battery
It didn't come with a battery to start with so we knew we had to get one quick. I didn't know what kind of battery to get and neither did my friends. "They all use lipo, we should probably use that". But wait, there are different cell counts, c ratings, capacities, etc. We looked at our components, the minimum was a 2s and the max was a 6s. We thought a 6s would be good as it gives the highest voltage. And as we know, the bigger it is, the better it is. (nope)

## The motors
The motors it came with had a number on it, '980KV', what's a KV? Turns out (from what I found) that this means these motors have lower speed and higher torque. The choice to get a 6s battery was actually a good decision because it allowed us to use smaller props while still being able to fly. We didn't want to buy newer motors either so we kept these.
![](/images/dronev1/og_980kvmotors.jpg)
## The motor ESCs
The original drone also had ESCs with it. An ESC is a device that can convert the normal DC battery voltage to a weird kind of three-phase AC voltage. It can change the frequency of the AC to change the speed. Just plug the PWM wire into the flight controller and the power wires into the battery and you're good. I had to make a bus bar if you could call it that. It worked though, so I don't care if it looks a little sketchy.
![](/images/dronev1/og_esc.jpg)
## The controller and receiver
The controller with the original drone was ok. It was included in the original $20 purchase and included a nice case for it. It worked with the receiver and had no problems. It has sbus support so we could use just three wires to receive all eight channels. Just 5V, ground, and data wires to the flight controller. Even to this day, we have had no problems with the controller or receiver itself. With dog teeth marks on one of the antennas, this worked great. 

## The propellers
The original garage sale drone had props, but after an initial motor test, we no longer have them (I'll get to that). With the higher torque motors, we decided to go for six-inch props with a higher pitch. These worked well, but you have to find higher-quality ones. In the end, we got decent propellers, but the ones we started with were flimsy and weren't good.
![](/images/dronev1/props.jpg)

# Now onto the frame
Since this was for TSA, we had to follow the rules of the competition. They outline the UAV as having a fully open-source frame and design. So with that knowledge, I designed one. My basic Onshape skills led me to a design that had some initial 3D prints that didn't work. But eventually, it led to this. This frame was our final design for the 2023-24 competition.
![](/images/dronev1/drone_v1_frame.png)
It had detachable arms so that any 3D printer could print it. This later had a shortcoming when our main point of failure was the weak thin arms. Inside the 'cage' is where the battery, receiver, and onboard flight controller are held. You can't see it in this view, but there is no mounting point for the onboard flight controller. This might have caused instability, but who knows. ¯\\_(ツ)_/¯

# Test Flights
We had done so many test flights before the competition, but we still couldn't get it working quite right by the competition. We tried so many times, but our slowly improving drone knowledge could only take us so far before we had another setback.

## An important consideration
There are many regulations when it comes to flying drones. Our drone has to comply with FAA regulations or we could get fined. Remote ID was introduced after this drone was constructed so we did not have one, but future drones will need to have it if it's flown outside. The airspace our drone was flown in allowed drone flight with no restrictions, but always check with your local authority. We have followed all safety and FAA regulations when flying our drone. I am not a legal expert, nothing I say is legal advice. I take no liability or responsibility for the actions you do. Always check with a lawyer or your local authority to get a complete understanding of if what you're doing is legal.

## Our first test 'flight'
Our very first test flight consisted of us shoving all of the parts into the frame just to see if it could fly. Wires were hanging out but we zip-tied them to the frame so they wouldn't get hit by the propellers. We were inside and just wanted to see if the motors spun (with the props on 🤦‍♂️). While the motors did spin up, a major flaw in our configuration resulted in the props disintegrating into a thousand pieces and the frame into multiple pieces. When the controller is turned off, the onboard flight controller thinks it should full throttle the motors resulting in a destroyed drone. I reprinted the frame and tried to make sure the onboard flight controller was configured properly, but I just couldn't find what I was looking for. Later on, an incident made us have to buy a new onboard flight controller anyway. The incident was that someone from another class shorted the board.

## The many unsuccessful flights
After the first 'flight' we would make a change, test it, and it wouldn't work. Did you know that the motors are supposed to spin a certain way? Did you know that you have to configure the receiver? Did you know... you get it. There were a countless number of things I had no clue about. I had to do constant research about how to do something properly about every little thing. What's a PID loop? AAAAAAAAAAHHHHHH.

## A 'successful' flight
IT FINALLY FLEW. It may have had a little drift and may have crashed, but IT FLEW. 
![](/images/dronev1/flight1.png)
![](/images/dronev1/flight1_closeup.png)
![](/images/dronev1/almost_crash.png)
![](/images/dronev1/crash.png)
It did shortly crash though and caused us to have to melt the arms back together and get new props (In the last image, you can kind of see an arm not attached). But it flew, and that made me happy. After months of work and finally seeing what it could do, I felt fulfilled. I didn't care that it crashed, I was way more confident that I could make it better now.

## One more test
The day before we left for the state competition, we flew it one last time. It went up and back down without a crash so we thought it was good.

# Final Part List
The parts used changed throughout our process because the first choice wasn't always the best. And some other things broke that you can't buy anymore so we had to get different parts.
- Afro Opto 30A ESC (Discontinued)
	- Uses PWM for control, works good for our use
- SunnySky 980KV Motors (4x)
	- High torque, low speed
	- Never realized they are meant for 3-4s lipos, (we had a 6s)
- SpeedyBee F405 V4 (w/o esc stack)
	- Betaflight has so many configuration options for this
	- Worked really well, especially for being under $40
- FrSky X8R 8-16 Channel Receiver (might be discontinued)
	- Had no problems, we used SBUS to receive our signal
- FrSky X9D transmitter (Discontinued)
	- OpenTX configurator was very annoying, or maybe that's because you can only find info about the pro version of this transmitter. This is the non pro version
- 12g Servos (2x)
	- Used for the claw
	- I had to hook these directly to the X8R receiver module
- 6 Inch 6045 Propellers (4x)
	- They worked
- Tenergy Lipo battery charger
	- Any lipo battery charger works
	- I chose this one so that we can charge other batteries for other projects as well
- Some thicker wire
	- Speaker wire seemed to work (I want to say it was 20awg)
- 3D Printer with PLA or ABS plastic

# The Competition
The competition was fun, we stayed overnight and enjoyed many fun activities. We signed up for the very first time to present our drone but when we got there, nothing was set up. A theme of this year's competition was disorganization. The people supposed to set up the drone cage and tables quit the day before. Me and my friends helped them set up the two drone cages along with the judging tables. And a few hours later, we could present. We gave a judge our documentation and another judge inspected our drone to make sure it was safe. He told us to attach the propellers but not the battery. We put it inside the test flight cage where we could make sure everything worked before the actual competition. It Went up and into the netting, twice. (If I had a picture I would show it, but my amazing camera skills resulted in a drone flying outside the camera view). I determined that we couldn't complete the actual competition but I still wanted to show the judges our design decisions and the claw I designed.

## Our placement
I wasn't confident and neither was my team. We didn't even have a flying drone. A few hours later I talked with my teacher and he mentioned we semi-finaled. In a somewhat casual way, he just mentioned to me that we made the top 12. I told the rest of my friends and they were excited but also curious. How did we semi-final with a non-flying drone when a third of the score was based on it flying?! It turns out that our documentation was very good. It had engineered drawings, wiring schematics (although hand drawn), and various details about our drone.
![](/images/dronev1/drone-finalv1.png)
(The school name and my friends names are blurred because I don't want to reveal them)
![](/images/dronev1/wiring_schematic.jpg)

# Final remarks
This was a very fun and (mostly) rewarding project. I have never worked on anything drone-related, let alone fly one. This was probably my biggest learning experience. Trying to get all the pieces to fit together to make something that can fly and pick something up was very difficult and I couldn't have done it without the help of my friends and teachers. I don't want to stop with this project though. It didn't successfully fly for this year's competition, but next year, it will fly. As of writing this, I have already started on next year's drone. You can find more about it [here](./Dronev2). My team and I have discussed how we were all surprised about what we had done with this project. But one thing was clear, It was kind of a mess.
We focused on getting it to fly ignoring design problems that made it harder for us. If you want to build a drone, do a lot of research and don't be afraid of problems. Try to make sure your design fits your needs, and if it doesn't you'll learn what to improve on. Don't settle as we did on a design that had to be constantly physically modified. We really should've printed new frames with our design modifications instead of melting a bunch of plastic, drilling new holes, sanding the frame, etc. I hope you've learned something because I know I did. Thank you for reading!