# ENEL-500-Lock2A
[![](https://utfs.io/f/nGnSqDveMsqxOuwi360k5fKEn2LbBoPAuZ6XMTHDcNJ0QiG1)](https://www.youtube.com/watch?v=Ajn6Fx0ZqqU)
A project to create an dynamic object tracking UAV! Far more etailed project information can be found here: https://symposium.foragerone.com/capstone-design-fair-2026/presentations/78618

## Project Goals
- Full stack drone integration for stable and reliable autonomous flight
- Design and or create auxilary hardware to support the autonomous detection and tracking of objectcs
- Learn a lot!

## Design Process
Capstone for us spans approximately 8 months, so there is more time compared to some other projects. This project was worked on in phases, first was to get the drone flying manually, then flying comfrotably autonomously, then flying with the rest of the system. To get the drone flying manually, I had to create a new 2s2p battery harness. Then to connect things to our new autopilot, I had to recrimp and reroute the various connectors. For autonomous flight, the main line of work was PID tuning, as without it our drone would be very unstable. For integration with the rest of the system, I had to design parts to fix things to the drone. One of the important things was to create a mount where the camera would always point down. Geolocation became unfathomably difficult when also needing to account for camera pitch/roll/yaw, so we needed a physical solution. Taking inspiration from self levelling cup mounts, I made a 2 axis balancing gimbal.

<div align="center">
  <img src="https://github.com/user-attachments/assets/1af676aa-5291-4afa-ba1a-4b0126efb5a8" width="300" alt="Early drone">
  <p>Early iteration of the drone</p>
</div>

## Challenges and Lessons Learned
As an electrical engineer with a minor in computer engineering, my coursework doesn't have any overlap with the work done for this. Thanks to my experience with SUAV (The Schulich Unmanned Aerial Vehicle design team) and over my internship working with drones, I have worked plenty with drones. The difference here is that I was the sole hardware person, so it was up to me get the drone flying. Without a dedicated mechanical or power team to defer to, I had to develop a broad skillset.

<div align="center">
  <img src="https://github.com/user-attachments/assets/07941d62-28ab-4f6b-a40a-e05c913846db" width="300" alt="Me">
  <p>Making connectors!</p>
</div>


One of the most significant lessons learned were the tradeoffs in hardware vs software complexity. Initially, geolocating objects from a moving drone required complex coordinate transformations to account for the drone’s pitch and roll. By designing a passive, 2 axis gravity leveled gimbal, I simplified the system requirements significantly. This physical solution removed the need for software compensation, reducing the system load and increasing the overall reliability of the tracking data.

<div align="center">
  <img src="https://github.com/user-attachments/assets/26e0b75a-6567-4ed3-9175-67ea15645a14" width="300" alt="Mount">
  <p>Camera mount on drone</p>
</div>

## Skills Learned/Practiced:
Hardware:
- Battery harness creation with EC5 connectors (very hard wow)
- Managing power delivery from batteries to various avionics
- Testing systems for reliability

<div align="center">
  <img src="https://github.com/user-attachments/assets/6285c5eb-6e7e-4e84-af09-deef0f73dae1" width="300" alt="EC5 grrrrrr.....">
  <p>A vice wasn't enough to get the EC5 connectors in</p>
</div>

Fusion 360:
- Working with print in place components
- Using assemblies to check clearances between integrated components
- Working quick and iterating on designs

Slicing/3D Printing:
- Set up Klipper on a Raspberry Pi for my Ender 3 S1-Pro so I can do things over Wifi
- Using slicing to make quick test prints for tolerances (tolerances of course who couldn't forget about dealing with tolerances)
- Making dove tail joints to integrate components without screws or glue
- DON'T TOUCH THE METAL PLATE THE OIL FROM HUMAN SKIN MAKES PRINTS NOT STICK

<div align="center">
  <img src="https://github.com/user-attachments/assets/fd396098-168b-4868-b7b1-15e67bf86f3b" width="300" alt="Don't touch plate">
  <p>Bad bed adhesion wow......</p>
</div>


DaVinci Resolve:
- Using preset text and transitions
