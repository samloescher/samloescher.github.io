---
layout: post
title:  Autonomous vehicle
date:   2014-04-17
author: Sam Loescher
categories: academic
---

![Mouse](/images/mouse/mouse.jpg){: .center-image }

The mouse design challenge is a project run by the University of Bath which enables students to engage in practical control implementations. The task is to design a small “mouse” vehicle which can complete one loop of the track by sensing a current carrying wire.

## Brief

In small teams of 3 or 4, design a “mouse” which is capable of following a wire carrying a 1A, 20 KHz AC current. The total track length is 20m and the mouse should follow the wire using inductors to sense the magnetic field associated with the wire. The end goal is to complete one loop of the track, in the fastest time possible.

![Brief](/images/mouse/mouse_track.jpg){: .center-image }

## Design

For the design, we chose a digital approach to drive motors with a PWM wave. We chose the PIC16F873A as this was ample in size and speed for what was required. The digital control was a state machine controlled by the two sensors(inductors) at the front of the mouse.

![Sensors](/images/mouse/mouse_sensors.jpg){: .center-image }

After we saw a reasonable performance, we added in more complex features to take advantage of known features of the track. For example the long straight we could exploit by accelerating if the error signal was consistently small. Another add on we made to the mouse was another sensor underneath, such that after using hard acceleration to get up the ramp, it would detect when it reached the top and stop accelerating.

![Booster](/images/mouse/mouse_booster.jpg){: .center-image }

## Race day

We were allowed 3 attempts to get the fastest time around the track, and while in testing we were seeing sub 16 seconds. The first attempt was very successful and achieved a fast speed through the first corners of the track. However upon entering the straight, there was a fairly large oscillatory error causing the mouse not to accelerate. Nevertheless it still managed to reach the ramp and safely complete the lap in 20.55 seconds, scoring 9th overall which we are very pleased with. The second and third attempts unfortunately didn't improve on this time and had we managed to reproduce the times we saw in testing, we would have been in the top 3.

___

Code : Available on request only, due to possibility of plagiarism for future students