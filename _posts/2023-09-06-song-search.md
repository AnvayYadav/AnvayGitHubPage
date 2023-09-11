---
toc: true
comments: false
layout: post
title: Song Search
description: This post covers my plans for week 2
type: hacks
courses: { compsci: {week: 3} }
---

### PBL Unit 1 / Week 0

<html>
<head>
    <title>Song Search by Genre</title>
</head>
<body>
    <h1>Song Search by Genre</h1>
    <input type="text" id="genreInput" placeholder="Enter a genre">
    <button onclick="searchSongsByGenre()">Search</button>
    <div id="searchResults"></div>

    <script>
        function searchSongsByGenre() {
            const apiKey = "3b9fb4fd5125c0570f8e8039520d162a";
            const genre = document.getElementById("genreInput").value;
            const url = `https://ws.audioscrobbler.com/2.0/?method=tag.gettoptracks&tag=${encodeURIComponent(genre)}&api_key=${apiKey}&format=json`;

            fetch(url)
                .then(response => response.json())
                .then(data => {
                    const tracks = data.tracks.track;
                    const searchResults = document.getElementById("searchResults");
                    searchResults.innerHTML = "";

                    if (tracks.length === 0) {
                        searchResults.innerHTML = "<p>No results found for this genre.</p>";
                    } else {
                        tracks.forEach(track => {
                            const name = track.name;
                            const artist = track.artist.name;

                            const resultItem = document.createElement("div");
                            resultItem.innerHTML = `
                                <h2>${name}</h2>
                                <p>Artist: ${artist}</p>
                            `;
                            searchResults.appendChild(resultItem);
                        });
                    }
                })
                .catch(error => {
                    console.error(error);
                    document.getElementById("searchResults").innerHTML = "<p>An error occurred while fetching data.</p>";
                });
        }
    </script>
</body>
</html>
