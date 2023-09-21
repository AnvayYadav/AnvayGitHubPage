---
toc: true
comments: false
layout: post
title: Car racing game
description: Explain logic behind our work this week
type: tangibles
courses: { compsci: {week: 3} }
---

### PBL Unit 1 / Week 3

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Car Racing Game</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
        }
        canvas {
            background: #333;
            display: block;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <canvas id="gameCanvas"></canvas>

    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');

        const carWidth = 50;
        const carHeight = 100;
        let carX = (canvas.width - carWidth) / 2;
        const carSpeed = 5;

        function drawCar() {
            ctx.fillStyle = 'red';
            ctx.fillRect(carX, canvas.height - carHeight, carWidth, carHeight);
        }

        function updateGameArea() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            drawCar();

            requestAnimationFrame(updateGameArea);
        }

        document.addEventListener('keydown', (event) => {
            switch (event.key) {
                case 'ArrowLeft':
                    carX -= carSpeed;
                    break;
                case 'ArrowRight':
                    carX += carSpeed;
                    break;
            }
        });

        updateGameArea();
    </script>
</body>
</html>

