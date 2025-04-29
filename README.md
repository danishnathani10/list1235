# Twin.Bot & Jump Metaverse

## Project Overview

This document covers two projects: **Twin.Bot** and **Jump Metaverse**.

## **TwinBot**

![TwinBot1](https://i.imgur.com/zQ2EKtp.png)
AI Agents in Metaverse
![TwinBot2](https://i.imgur.com/M9SudR6.png) 
![TwinBot3](https://i.imgur.com/y511nTa.png)

### Short Summary
* TwinBot is an **AI-powered chatbot** experience that utilizes conversational interfaces to engage users.
* **3D rendered animated humanoid** characters are used for bots.
* Companies use this for day-to-day tasks where a human talks to another human.

### Techniques and Technologies Used
* Frontend was made using **Unity 3D Engine** & backend was done on Python and APIs were hosted on AWS.
* Humanoid bots creation was automated using **AvatarSDK**. A system where we just upload the image of the human agent and the 3D model of the bot looking similar to them gets generated.
* For conversations, we needed 2 things Text-to-speech (TTS) & Speech-to-text (STT) - for this, we used **Google Cloud**'s services and also integrated multi-language support for flexibility (this feature showed why AI agent was more useful than a human).

### High-Level Architecture Overview
* **Components**: Frontend (Unity), Backend (Python), Conversational AI Models
* **Interactions**: User input → Frontend → Backend → Conversational AI → Response
* **Technology Stack**: C#, JavaScript, Python, AWS, MongoDB
* **System Boundaries**: User interactions → TwinBot → Response

### Key Challenges and Solutions
* **Designing Conversational Flow**: Implemented a **state-based system** to handle different user interactions and respond accordingly.
* **Look & Feel**: The requirement was to make everything look **realistic**. So to solve this, we used custom shaders & used post-processing to make shadows, shaders, etc; just made sure to make everything look very real and also made sure it wasn't too heavy on devices.
* **Performance Optimization**: Used .gltf 3D models instead of .fbx, main reason - **gltf** model is very lightweight and is very quick to download and appear on screen.

### UX/UI Considerations
* Simple interface - **only 2 buttons** - settings and speak, so that people find it very easy to use.
* After settings were clicked, multiple options were shown like language, graphics, and going back to the bot selection menu.

### Demo Video (Click on image to play)
* Android app demo
[![TwinBot - Android app demo](https://img.youtube.com/vi/VZ8gKm2fiUA/0.jpg)](https://youtu.be/VZ8gKm2fiUA)
* Our client - Qore Bank using it on their kiosks (web app)
[![TwinBot - Our client - Qore Bank using it on their kiosks (web app)](https://img.youtube.com/vi/gG9kfGlFLuI/0.jpg)](https://youtu.be/gG9kfGlFLuI)

## **Jump Metaverse**

![JM1](https://i.imgur.com/1vDRbp3.png) ![JM2](https://i.imgur.com/4EjVDXS.png") ![JM3](https://i.imgur.com/xMJMztV.png)

### Short Summary
* Jump Metaverse is an **immersive experience of virtual worlds** in which users represented by avatars interact, in 3D and focused on social and professional connection.
* The USP of Jump is **AvatarSDK** - used to create 3D models of people just from their 1 picture and boom they are there interacting in the metaverse.
* Use of **AI agents** by world creators to **sell their products**.

### Techniques and Technologies Used
* Built on **Unity 3D Engine**, same for backend in Python and APIs hosted on AWS.
* **AvatarSDK** used for custom avatars.
* For multiplayer, we used **Mirror Networking** and for the metaverse worlds, for compression - we used **Unity's asset bundles** and for hosting - we used **AWS S3**.

### High-Level Architecture Overview
* **Components**: Frontend (Unity), Backend (Python), Multiplayer syncing, Server hosting & World Loading
* **Interactions**: User input → Frontend → Backend → 3D Element → Logic → Response
* **Technology Stack**: C#, JavaScript, Python, MongoDB, AWS S3, AWS Lightsail
* **System Boundaries**: User interactions → Jump Metaverse → Immersive experience

### Key Challenges and Solutions
* **Syncing of data**: In multiplayer development, often this happens - player data (location or looks & style or animations) is **not synced via server** on multiple machines.
* **Lighting**: When the player goes from 1 map to another, the lighting needs to be changed instantly. Was easy to fix by adding **custom lighting data** in each map's compressed asset bundles data before uploading it to the server.

### UX/UI Considerations
* **Minimalistic** looking modern UI (*pressing M for MapList and clicking which map to load*).
* For UX - Interactive 3D elements respond to user inputs (*check Twin.Bot integration in Jump video for this*).

### Demo Video (Click on image to play)
* WebGL app demo
[![Jump Demo](https://img.youtube.com/vi/jH1TJk3UvF0/0.jpg)](https://youtu.be/jH1TJk3UvF0)
* Talking to Twin.Bots in Qore Metaverse
[![Jump Demo](https://img.youtube.com/vi/plhwuNNX5J0/0.jpg)](https://youtu.be/plhwuNNX5J0)

## **Live Projects**
* **TwinBot**: https://danish-nathani-portfolio.framer.ai/twinbot
* **Jump Metaverse**: https://danish-nathani-portfolio.framer.ai/jumpmetaverse
