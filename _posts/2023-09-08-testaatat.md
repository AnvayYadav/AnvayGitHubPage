---
toc: true
comments: false
layout: post
title: Immsersive VR experience
description: This is a test
type: tangibles
courses: { compsci: {week: 3} }
---

### PBL Unit 1 / Week 0


<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-teleport-controls@4.0.1/dist/aframe-teleport-controls.min.js"></script>
</head>
<body>
    <a-scene>
        <!-- VR Camera with Teleport Controls and WASD Movement Controls -->
        <a-entity camera look-controls wasd-controls position="0 1.6 0" teleport-controls="cameraRig: #cameraRig"></a-entity>

        <!-- Camera Rig (Required for Teleport Controls) -->
        <a-entity id="cameraRig">
            <a-entity id="head" camera="userHeight: 1.6" position="0 0 0"></a-entity>
            <a-entity id="left-hand" teleport-controls="hand: left; button: grip" raycaster="objects: .teleportable"></a-entity>
            <a-entity id="right-hand" teleport-controls="hand: right; button: grip" raycaster="objects: .teleportable"></a-entity>
        </a-entity>

        <!-- Red Cube with Text -->
        <a-entity class="teleportable" position="0 1 -3">
            <a-box position="0 0 0" rotation="0 45 0" color="red"></a-box>
            <a-text value="We love Cs" align="center" position="0 1 0" scale="2 2 2" color="white"></a-text>
            <a-text value="Anvay and Srini CSP project" align="center" position="0 2 0" scale="1 1 1" color="yellow"></a-text>
            <a-text value="This VR experience is set up with two main code blocks. One block was for camera movement, which allows us to create a truly immersive VR experience. The other code block was used for objects, object position, and object/text properties." align="center" position="-2 3 0" scale="1 1 1" color="blue"></a-text>
            <a-text value="When adding text, you have options to align the text, the color, the position, and the scale. The scale determines how big the text is, the position helps move around the text on the VR plane, and the color helps determine the color of text." align="center" position="3 3 0" scale="1 1 1" color="blue"></a-text>
        </a-entity>

        <!-- Ground Plane -->
        <a-plane position="0 0 0" rotation="-90 0 0" width="10" height="10" color="#ccc"></a-plane>

        <!-- Letter "C" -->
        <a-entity class="teleportable" position="-1 1 -3">
            <a-box position="0 0 0" color="blue" depth="0.1" height="1" width="1"></a-box>
        </a-entity>

        <!-- Letter "S" -->
        <a-entity class="teleportable" position="0 1 -3">
            <a-box position="0 0 0" color="green" depth="0.1" height="1" width="1"></a-box>
        </a-entity>

        <!-- Letter "P" -->
        <a-entity class="teleportable" position="1 1 -3">
            <a-box position="0 0 0" color="red" depth="0.1" height="1" width="1"></a-box>
        </a-entity>
    </a-scene>
</body>
</html>

