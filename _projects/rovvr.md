---
title: 'Virtual Control Room'
subtitle: 'Piloting an ROV through virtual reality'
date: 2020-11-10 00:00:00
description:
featured_image: '/images/landing_page/landing_rovvr.PNG'
---

<img src="/images/landing_page/landing_rovvr.PNG" alt="drawing" width="800"/>

<p style="text-align: left;"> This is the view from within the VR headset. Multiple data overlays display different pieces of telemetry data, and the hand on the left is the user's hand within the virtual environment. Live footage from the ROV's front facing cameras are displayed in the headset. </p>

### Overview 

**Timeline:** 2020-2021 Senior Capstone Project in Engineering at Olin College

**Olin Collaborators:** Amy Phung, Cameron Wierzbanowski, Erika Lu, Nathan Shuster, w. Advisor Lynn Andrea Stein

**MBARI Collaborators:** Eric J. Martin, Benjamin Erwin, Kakani Katija, Steven H.D. Haddock

The goal of this project was to prototype a Virtual-Reality (VR) based control room for underwater Remotely Operated Vehicles (ROVs) as a potential upgrade to conventional ROV control rooms with funding from Dassault Systemés. I worked on this project as a senior at Olin College with four other senior students and a faculty advisor. We also collaborated directly with a team of pilots, scientists, and engineers at the Monterey Bay Aquarium Research Insititute (MBARI) to better understand the needs of our prototype's end users. We tested our software with MBARI's MiniROV in their one million liter saltwater test tank facility to create a final prototype capable of displaying real-time stereo-camera footage and telemetry data.

This project has been included in two academic papers: [**A Virtual Reality Video System for Deep Ocean Remotely Operated Vehicles**](https://ieeexplore.ieee.org/document/9705810) in IEEE OCEANS 2021, and [**Catching Jellies in Immersive Virtual Reality: A Comparative Teleoperation Study of ROVs in Underwater Capture Tasks**](https://dl.acm.org/doi/pdf/10.1145/3489849.3489861?casa_token=Ezc_tlWORZIAAAAA:xs6K5VSjgASOTWNQo_sIuj3A8YnmHozHgRg_gRoKoLItcqmYLiOh41BYJ_mA3ODn5zV13H0KstEp) in VRST 2021. We additionally presented the project as a poster , [**Developing a Control Room in Virtual Reality to Improve Underwater Remotely Operated Vehicle Piloting**](https://everardog.github.io/files/mbari_poster.pdf), on its own at CCSCNE 2021.

The first paper details the integration of the virtual reality control room with MBARI's custom 4k fisheye stereo-camera designed specifically for operation on an ROV at extreme depths. The second discusses the results of a user study with ROV pilots that compared the effectiveness of the VR control room to a conventional control room. When pilots used the VR control room as opposed to the conventional control room, they cut their task completion time in half, suggesting this technology is promising for the future of ROV piloting. The poster details at a high level how our control room works and what the benefits are over conventional ROV piloting.

### My Contributions

My technical contributions included writing software for different telemetry data overlays, investigating methods for feeding stereo camera footage into the VR control room, and double checking our computer vision algorithms for dewarping and reprojecting fisheye camera footage. Other contributions included interviewing MBARI stakeholders, writing and organizing technical docs for a clean hand-over of our software to MBARI, and contributing towards external facing documentation.

<!-- ### Further Reading -->

<!-- <a href="https://everardog.github.io/files/mbari_poster.pdf" target="_blank">Overview Poster</a> -->
