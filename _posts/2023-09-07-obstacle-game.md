---
toc: true
comments: false
layout: post
title: Obstacle game
description: This is a game with obstacles
type: tangibles
courses: { compsci: {week: 3} }
---

### PBL Unit 1 / Week 0

<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Obstacle Game with Timer</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
        }
        #game-container {
            width: 400px;
            height: 400px;
            margin: 0 auto;
            border: 1px solid #000;
            position: relative;
        }
        #player {
            width: 50px;
            height: 50px;
            background-color: blue;
            position: absolute;
            bottom: 0;
        }
        .obstacle {
            width: 20px;
            height: 20px;
            background-color: red;
            position: absolute;
        }
        #timer {
            position: absolute;
            top: 10px;
            right: 10px;
        }
    </style>
</head>
<body>
    <div id="game-container">
        <div id="player"></div>
    </div>
    <div id="timer">Time: 0s</div>

    <script>
        const gameContainer = document.getElementById('game-container');
        const player = document.getElementById('player');
        const timerElement = document.getElementById('timer');
        let playerPosition = 0;
        let startTime = null;
        let endTime = null;

        function movePlayer(direction) {
            if (direction === 'left' && playerPosition > 0) {
                playerPosition -= 10;
            } else if (direction === 'right' && playerPosition < 350) {
                playerPosition += 10;
            }

            player.style.left = playerPosition + 'px';
        }

        document.addEventListener('keydown', function (event) {
            if (event.key === 'ArrowLeft') {
                movePlayer('left');
            } else if (event.key === 'ArrowRight') {
                movePlayer('right');
            }
        });

        function createObstacle() {
            const obstacle = document.createElement('div');
            obstacle.className = 'obstacle';
            const randomPosition = Math.floor(Math.random() * 380);
            obstacle.style.left = randomPosition + 'px';
            gameContainer.appendChild(obstacle);

            const obstacleInterval = setInterval(function () {
                const currentTop = parseInt(obstacle.style.top) || 0;
                obstacle.style.top = (currentTop + 10) + 'px';

                if (currentTop > 400) {
                    clearInterval(obstacleInterval);
                    gameContainer.removeChild(obstacle);
                }

                if (
                    currentTop + 20 >= 400 &&
                    playerPosition + 50 > parseInt(obstacle.style.left) &&
                    playerPosition < parseInt(obstacle.style.left) + 20
                ) {
                    clearInterval(timerInterval);
                    endTime = new Date().getTime();
                    const survivalTime = (endTime - startTime) / 1000;
                    alert('Game Over! You survived: ' + survivalTime.toFixed(2) + 's');
                    location.reload(); // Reload the game to restart
                }
            }, 50);
        }

        // Create multiple obstacles at the same time
        function createMultipleObstacles() {
            for (let i = 0; i < 3; i++) { // Create 3 obstacles simultaneously
                createObstacle();
            }
        }

        // Create obstacles every 2 seconds
        setInterval(createMultipleObstacles, 2000);

        // Start the timer when the game starts
        startTime = new Date().getTime();
        const timerInterval = setInterval(function () {
            const currentTime = new Date().getTime();
            const elapsedTime = (currentTime - startTime) / 1000;
            timerElement.textContent = 'Time: ' + elapsedTime.toFixed(2) + 's';
        }, 10);
    </script>
</body>
</html>

