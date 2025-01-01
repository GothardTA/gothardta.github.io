---
title: Arduino Laser Data Transfer
featured_image: /images/arduinolaser/overall.jpg
type: page
---
# Quick Info
Not too long ago I heard NASA could transmit a 4K video using lasers to a satellite millions of miles away. I thought that was cool and I wanted to do something similar. I had a couple of Arduinos, laser modules, and photo resistors. I first wanted to send data one way using a single wire (plus ground) to get a working protocol. I then replaced the wire with a laser diode on one end and a photoresistor on the other. I then had a few issues with transfer speed because the photo resistors were too slow. I don't have photodiodes so I used a small solar panel from those outdoor lights you can stick in the ground anywhere. In the end, I could get a bit rate of 5000.

# In Depth
The goal I had in mind for this project was to transmit audio, not beeps, but actual audio. So far, I have found that an Arduino is not even close to being fast enough for this and my laser protocol can't seem to handle faster speeds either. But for now, it's good enough. It uses my custom-made single-wire protocol that is similar to uart but is only one way. There is no error correction, packets, or any other fancy stuff. You can transmit bytes and words. I first got this working using a wire and could use a bit rate of 10000. To go on to anything other than a wire, I needed a way to receive the signal. A laser transmits light and that light can be any brightness. There is also ambient light that the receiver can pick up. I had to make a circuit that only outputs when the laser is on. Since the receiver only sees brightness, I needed a way to figure out when the laser is on. When the laser is on the receiver outputs a little extra power. I used an lm358 to compare the signal received by the receiver to a potentiometer. This allowed me to adjust when the output should be on since the voltage only changes by a small amount.
![](/images/arduinolaser/laserschematic.png)
I tried using a photoresistor but those were too slow. I could only get it working with a bit rate of around 100. I don't have photodiodes so I had to figure something else out. I had a small solar panel from one of those lights you can stick in the ground by your driveway or garden. A solar panel is just a giant photodiode. I hooked it up and it worked, but I had to keep adjusting the potentiometer every minute because the sunlight from my window kept changing. I added a cardboard box with an opening around the solar panel.
![](/images/arduinolaser/overall.jpg)
![](/images/arduinolaser/closeup.jpg)
The picture shows the laser close to the panel but it can work at longer distances. I got it working outside when it was dusk, but during the day, the laser doesn't add a large enough difference to the brightness for it to receive anything. Another hard part is positioning the laser and receiver, one little bump or tape coming loose and then you have to realign it.
# Parts
- 2 Arduinos (or Arduino compatible micro controller)
- 5v laser diode
- photo diode (or mini solar panel in my case)
- LM358
- Potentiometer

# In Conclusion
This was a fun project, I learned about how different data protocols worked and how I could make my own. Although it wasn't what I wanted it to be, it was still cool. I was able to hide the receiver and when a friend was close to it, I pointed the laser at the receiver and it started rickrolling him. In the future, I want to use Raspberry Pi Picos and actual photodiodes to make this faster. I have already experimented with the Pico and getting USB to work on it and hope I can use it to transmit actual audio. But for now, you can send data a very slow speeds, but it's enough to play tones and beeps.

# Code
I wrote the transmitter code and it is available under my [github](https://github.com/GothardTA/arduinolasersong). Everything music-related used code from robsoncouto on his [github](https://github.com/robsoncouto/arduino-songs/tree/master). I don't understand anything related to how music is written or played from sheet music so having their code really helped.