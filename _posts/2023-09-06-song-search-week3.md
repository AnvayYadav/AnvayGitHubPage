---
toc: true
comments: false
layout: post
title: Spotify song search
description: This post covers my plans for week 2
type: hacks
courses: { compsci: {week: 3} }
---

### PBL Unit 1 / Week 0

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Recommendation System</title>
</head>
<body>
    <h1>Music Recommendation System</h1>

    <!-- User input -->
    <label for="userInput">Enter your music taste:</label>
    <input type="text" id="userInput" placeholder="e.g., your favorite genre or artist">
    <button onclick="getTopArtists()">Get Top Artists</button>

    <!-- Recommended artists -->
    <h2>Recommended Artists</h2>
    <ul id="recommendedArtists">
        <!-- Recommended artists will be displayed here -->
    </ul>

    <script>
        const apiKey = 24bbe3c7852fb05ab05a444bd291bf92;

        async function getTopArtists() {
            const userInput = document.getElementById("userInput").value;
            const recommendedArtists = document.getElementById("recommendedArtists");
            recommendedArtists.innerHTML = '';

            if (userInput) {
                const apiUrl = `https://ws.audioscrobbler.com/2.0/?method=artist.search&artist=${userInput}&api_key=${apiKey}&format=json`;

                try {
                    const response = await fetch(apiUrl);
                    const data = await response.json();

                    if (data.results.artistmatches && data.results.artistmatches.artist.length > 0) {
                        const artists = data.results.artistmatches.artist;
                        artists.forEach(artist => {
                            const listItem = document.createElement("li");
                            listItem.textContent = artist.name;
                            recommendedArtists.appendChild(listItem);
                        });
                    } else {
                        recommendedArtists.innerHTML = '<p>No artists found for this input.</p>';
                    }
                } catch (error) {
                    console.error("Error fetching data:", error);
                    recommendedArtists.innerHTML = '<p>An error occurred while fetching data. Please try again later.</p>';
                }
            } else {
                recommendedArtists.innerHTML = '<p>Please enter a music taste (e.g., your favorite genre or artist).</p>';
            }
        }
    </script>

</body>
</html>
