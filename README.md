3D Karaoke 2026 Remix
Project Overview
This repository contains the original source code for 3D Karaoke, an interactive installation by G.H. Hovagimyan. The project explores the intersection of telepresence, digital "voice throwing," and real-time 3D mapping.

Historical Provenance
Development (2012): Originally conceived and developed during an artist residency at the Pixel Palace at Tyneside Cinema, Newcastle upon Tyne, UK. Supported by D6: Culture in Transit.

Exhibition (2013): Featured in the Convention Habit or Custom exhibition at The NewBridge Project, Newcastle.

US Premiere (2014): Presented at Harvestworks Digital Media Arts Center, New York City. The Harvestworks presentation showcased the system's ability to create a "social sculpture" through participant interaction and 3D point-cloud visualization.

The 2026 Remix serves as a digital preservation effort to migrate this Kinect V1 / Processing 2.0 environment into a modern framework compatible with Apple Silicon and Lidar technology.

Technical Specs (Legacy)
Original Engine: Processing 2.0

Depth Sensing: Dual Xbox 360 Kinects (Model 1414) via SimpleOpenNI.

Interaction: Real-time 360-degree point-cloud mapping with synchronized MP3 playback and scrolling lyrical overlays.

2026 Development Roadmap
1. Processing 4 Migration
Target: Processing 4.x (Native Apple Silicon support).

Task: Remove dependencies on legacy .jnilib / .dll libraries. Refactor the core P3D render loop for compatibility with modern Java environments.

2. Depth-Sensing Port (Kinect to Lidar)
The Goal: Decouple the software from the original Kinect hardware.

Target Hardware: * iOS/iPad Lidar (via OSC/WebSockets).

OAK-D or Azure Kinect for fixed installations.

Task: Create a modular input class to feed a generic DepthPixel array into the main sketch.

3. GPU Optimization
Task: Offload point-cloud vertex manipulation to GLSL Shaders to ensure 60fps performance on M1/M2/M3 integrated GPUs.

How to Contribute
Clone: git clone https://github.com/ghovagimyan/3D-Karaoke-2026.git

Explore: See the /legacy_v1 folder for the original code used at Pixel Palace and Harvestworks.

Collaborate: Open an issue to claim a specific porting task (e.g., "Shaders," "Lidar Input," or "P4 Refactor").

License
Source code is released under GPLv3.
Note: This repository is for software logic and historical documentation only. High-fidelity environment assets for the 2026 installation are maintained in a separate private archive.
