---
layout: page
title: About
permalink: /about/
---
<div style="background-color:#da95f5; border-radius: 15px; padding: 10px; margin: 10px 0; color: black; font-family: 'Arial', sans-serif;">
<p style="color: black;"> My name is Vibha Mandayam and I am a sophomore at Del Norte High School. I am interested in computers and can't wait to learn more in this class! </p>
</div>


## Things About Me
<div style="background-color: #da95f5; border-radius: 15px; padding: 10px; margin: 10px 0; color: black; font-family: 'Roboto', sans-serif;">
  <p style="color: black;">I love to bake!🧑‍🍳</p>
  <p style="color: black;">I enjoy reading mystery novels 🕵️📖</p>
  <p style="color: black;">My favorite place is the beach 🏖️</p>
  <p style="color: black;">I have played the piano for 10 years 🎹</p>
  <p style="color: black;">Swimming is my favorite sport 🏊‍♀️</p>
</div>

## Programming Languages I am Currently Learning 

<comment>
Logos are made using Wikipedia images
</comment>

<style>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
    }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for coding languages
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var coding_languages = [
        {"logo": "c/c3/Python-logo-notext.svg", "description": "Python"},
        {"logo": "9/99/Unofficial_JavaScript_logo_2.svg", "description": "JavaScript"},
        {"logo": "6/61/HTML5_logo_and_wordmark.svg", "description": "HTML"},
        {"logo": "d/d5/CSS3_logo_and_wordmark.svg", "description": "CSS"},
    ];

    // 3b. Build grid items inside of our container for each row of data
    for (const language of coding_languages) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the logo
        var img = document.createElement("img");
        img.src = http_source + language.logo; // concatenate the source and logo
        img.alt = language.description + " Logo"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = language.description; // extract the description

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

<div style="text-align: center; margin-top: 20px;">
    <img src="https://docs.google.com/drawings/d/e/2PACX-1vQVRanGxsjYlU_dlZvHuuu_76MLIOqTAGBSSeT4AHFB60ZGs80awgc43acBLcFOZuKv8WLTIsFIq1b-/pub?w=960&amp;h=720" alt="Alt Text" style="border-radius: 10px; max-width: 100%;">
</div>

<script src="https://utteranc.es/client.js"
        repo="vibha1019/vibha_mandayam_2025"
        issue-term="pathname"
        theme="preferred-color-scheme"
        crossorigin="anonymous"
        async>
</script> 