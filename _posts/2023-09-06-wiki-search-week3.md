---
toc: true
comments: false
layout: post
title: Wikipedia search
description: This post covers my plans for week 2
type: hacks
courses: { compsci: {week: 3} }
---

### PBL Unit 1 / Week 0

<html>
<head>
    <title>Wikipedia Search</title>
</head>
<body>
    <h1>Wikipedia Search</h1>
    <input type="text" id="searchInput" placeholder="Enter your search term">
    <button onclick="searchWikipedia()">Search</button>
    <div id="searchResults"></div>

 <script>
        function searchWikipedia() {
            const apiKey = "24bbe3c7852fb05ab05a444bd291bf92";
            const searchTerm = document.getElementById("searchInput").value;
            const url = `https://en.wikipedia.org/w/api.php?action=query&format=json&list=search&srsearch=${searchTerm}&utf8=&origin=*&api_key=${apiKey}`;

            fetch(url)
                .then(response => response.json())
                .then(data => {
                    const results = data.query.search;
                    const searchResults = document.getElementById("searchResults");
                    searchResults.innerHTML = "";

                    if (results.length === 0) {
                        searchResults.innerHTML = "<p>No results found.</p>";
                    } else {
                        results.forEach(result => {
                            const title = result.title;
                            const snippet = result.snippet;
                            const pageLink = `https://en.wikipedia.org/wiki/${encodeURIComponent(title)}`;

                            const resultItem = document.createElement("div");
                            resultItem.innerHTML = `
                                <h2><a href="${pageLink}" target="_blank">${title}</a></h2>
                                <p>${snippet}</p>
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
