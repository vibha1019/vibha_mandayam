---
layout: base
title: Student Home 
image: /images/mario_animation.png
description: Home Page
hide: true
---

# Welcome to AP Computer Science Principles

<img src="{{ site.baseurl }}/images/purple.png" style="width: 80%; max-width: 800px; border-radius: 15px; box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);">

<div style="background-color: #da95f5; padding: 20px; border-radius: 15px;">
  <h2 style="color: black;">AP CSP Students  Click Here!</h2>
  <p style="color: black;"> To properly prepare and excell in this class, there are many resources avaialable to you. Click on the button below ! </p>
  <button onclick="window.location.href='https://apcentral.collegeboard.org/courses/ap-computer-science-principles';">College Board!</button>
</div>

<p> </p>
<div style="background-color: #da95f5; padding: 20px; border-radius: 15px;">
  <h2 style="color: black;">Programming Help</h2>
  <a href="https://www.w3schools.com/css/">
    <button class="block"><b>CSS Help</b></button>
  </a>
  <p> </p>
  <a href="https://www.w3schools.com/html/">
    <button class="block"><b>HTML Help</b></button>
  </a>

  <p style="color: black;"> Use the links above to navigate to the programming language of your choosing! </p>
</div>

<p> </p>

<style>
  /* Ensure the 'Games' button is a big rounded square with a purple background */
  .games-menu {
    display: inline-block;
    background-color: #da95f5 !important; /* Purple background */
    padding: 15px 30px;
    border-radius: 25px;
    color: black !important; /* Text color */
    font-size: 18px;
    text-align: center;
    cursor: pointer;
    text-decoration: none;
  }

  /* Dropdown menu container */
  .dropdown-menu {
    display: none;
    position: absolute;
    background-color: #da95f5 !important; /* Purple background */
    border-radius: 10px;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    padding: 10px;
    top: 100%;
    left: 0;
    z-index: 1000;
  }

  /* Dropdown menu links */
  .dropdown-menu a {
    display: block;
    color: black !important; /* Text color */
    padding: 10px;
    text-decoration: none;
    border-radius: 5px;
    font-size: 16px;
  }

  /* Dropdown menu link hover effect */
  .dropdown-menu a:hover {
    background-color: #C8A2C8 !important; /* Hover background color */
    color: black !important; /* Hover text color */
  }

  /* Show dropdown menu when 'Games' button is clicked */
  .games-menu.active + .dropdown-menu {
    display: block;
  }
</style>

<!-- Add this HTML to your index.md file where you want the menu to appear -->
<div class="dropdown">
  <a href="#" class="games-menu">Games</a>
  <div class="dropdown-menu">
    <a href="https://vibha1019.github.io/vibha_mandayam/navigation/calculator.html">Calculator</a>
    <a href="https://vibha1019.github.io/vibha_mandayam/navigation/cookie_clicker.html">Cookie Clicker</a>
    <a href="https://vibha1019.github.io/vibha_mandayam/navigation/snake.html">Snake Game</a>
    <a href="https://vibha1019.github.io/vibha_mandayam/navigation/binary_calculator.html">Binary Calculator</a>
    <a href="https://vibha1019.github.io/bc_game/index.html"> Bulls and Cows Game</a>
  </div>
</div>

<script>
  // Toggle dropdown menu visibility
  document.querySelector('.games-menu').addEventListener('click', function(e) {
    e.preventDefault();
    this.classList.toggle('active');
  });
</script>




<p> </p>
<table style="background-color: #da95f5;">
    <tr>
        <td><a href="{{site.baseurl}}/github/pages/planning">Planning Notebook</a></td>
        <td><a href="{{site.baseurl}}/github/pages/javacell">Java Cell Notebook</a></td>
        <td><a href="{{site.baseurl}}/github/pages/frontendhacks">Front End Hacks Notebook</a></td>
    </tr>
</table>


<p> </p>
<table style="background-color: #da95f5;">
    <tr>
        <td><a href="{{site.baseurl}}/github/pages/3_3_hacks">3.3 Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/3_5_hacks">3.5 Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/3_1_hacks">3.1 Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/3_4_hacks">3.4 Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/3_8_hacks">3.8 Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/3_10_hacks">3.10 Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/3_2_hacks">3.2 Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/3_10B_hacks">3.10B Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/sprint_2"> Big Idea 3</a></td>  
    </tr>
</table>

<p> </p>
<table style="background-color: #da95f5;">
    <tr>
        <td><a href="{{site.baseurl}}/sprint_3_team_plan">Sprint 3 Team Plan</a></td>
        <td><a href="{{site.baseurl}}/sprint_3_review_ticket">Sprint 1-3 Review Ticket</a></td>
        <td><a href="{{site.baseurl}}/natm_reflection"> N@tM Team Presentation</a></td>
        <td><a href="{{site.baseurl}}/program_function"> Program Function & Purpose </a></td>
    </tr>
</table>


<p> </p>
<table style="background-color: #da95f5;">
    <tr>
        <td><a href="{{site.baseurl}}/test_corrections">Test Corrections</a></td>
        <td><a href="{{site.baseurl}}/panel_reflection">Student Panel Reflection</a></td>
        <td><a href="{{site.baseurl}}/sprint5">CPT Blog</a></td>
        <td><a href="{{site.baseurl}}/aws">AWS Blog</a></td>
    </tr>
</table>

<p> </p>
<table style="background-color: #da95f5;">
    <tr>
        <td><a href="{{site.baseurl}}//mcq_final">2020 MCQ Final Notes</a></td>
        <td><a href="{{site.baseurl}}/docse">5 Points DOCSE</a></td>
        <td><a href="{{site.baseurl}}/project_feature">Project Feature</a></td>
        <td><a href="{{site.baseurl}}/overall_reflection">Overall Reflection</a></td>
    </tr>
</table>

<p> </p>
<table style="background-color: #da95f5;">
    <tr>
        <td><a href="{{site.baseurl}}/ppr">PPR Blog</a></td>
        <td><a href="{{site.baseurl}}/github/pages/digital_divide">Digital Divide Hacks</a></td>
        <td><a href="{{site.baseurl}}/computing_bias">Computing Bias HW</a></td>
        <td><a href="{{site.baseurl}}/crowdsourcing">Crowdsourcing HW</a></td>
        <td><a href="{{site.baseurl}}/ethical">Legal and Ethical Concerns HW</a></td>
         <td><a href="{{site.baseurl}}/binarysearch">Binary Search HW</a></td>
    </tr>
</table>

<p> </p>
<table style="background-color: #da95f5;">
    <tr>
        <td><a href="{{site.baseurl}}/cyberpanelnotes">CyberCeo Blog</a></td>
    </tr>
</table>
<!-- Liquid:  statements -->

<!--- Concatenation of site URL to frontmatter image  --->
{% assign sprite_file = site.baseurl | append: page.image %}
<!--- Has is a list variable containing mario metadata for sprite --->
{% assign hash = site.data.mario_metadata %}  
<!--- Size width/height of Sprit images --->
{% assign pixels = 256 %}

<!--- HTML for page contains <p> tag named "Mario" and class properties for a "sprite"  -->

<p id="mario" class="sprite"></p>

<!--- Embedded Cascading Style Sheet (CSS) rules, 
        define how HTML elements look 
--->
<style>

  /*CSS style rules for the id and class of the sprite...
  */
  .sprite {
    height: {{pixels}}px;
    width: {{pixels}}px;
    background-image: url('{{sprite_file}}');
    background-repeat: no-repeat;
  }

  /*background position of sprite element
  */
  #mario {
    background-position: calc({{animations[0].col}} * {{pixels}} * -1px) calc({{animations[0].row}} * {{pixels}}* -1px);
  }
</style>

<!--- Embedded executable code--->
<script>
  ////////// convert YML hash to javascript key:value objects /////////

  var mario_metadata = {}; //key, value object
  {% for key in hash %}  

  var key = "{{key | first}}"  //key
  var values = {} //values object
  values["row"] = {{key.row}}
  values["col"] = {{key.col}}
  values["frames"] = {{key.frames}}
  mario_metadata[key] = values; //key with values added

  {% endfor %}

  ////////// game object for player /////////

  class Mario {
    constructor(meta_data) {
      this.tID = null;  //capture setInterval() task ID
      this.positionX = 0;  // current position of sprite in X direction
      this.currentSpeed = 0;
      this.marioElement = document.getElementById("mario"); //HTML element of sprite
      this.pixels = {{pixels}}; //pixel offset of images in the sprite, set by liquid constant
      this.interval = 100; //animation time interval
      this.obj = meta_data;
      this.marioElement.style.position = "absolute";
    }

    animate(obj, speed) {
      let frame = 0;
      const row = obj.row * this.pixels;
      this.currentSpeed = speed;

      this.tID = setInterval(() => {
        const col = (frame + obj.col) * this.pixels;
        this.marioElement.style.backgroundPosition = `-${col}px -${row}px`;
        this.marioElement.style.left = `${this.positionX}px`;

        this.positionX += speed;
        frame = (frame + 1) % obj.frames;

        const viewportWidth = window.innerWidth;
        if (this.positionX > viewportWidth - this.pixels) {
          document.documentElement.scrollLeft = this.positionX - viewportWidth + this.pixels;
        }
      }, this.interval);
    }

    startWalking() {
      this.stopAnimate();
      this.animate(this.obj["Walk"], 3);
    }

    startRunning() {
      this.stopAnimate();
      this.animate(this.obj["Run1"], 6);
    }

    startPuffing() {
      this.stopAnimate();
      this.animate(this.obj["Puff"], 0);
    }

    startCheering() {
      this.stopAnimate();
      this.animate(this.obj["Cheer"], 0);
    }

    startFlipping() {
      this.stopAnimate();
      this.animate(this.obj["Flip"], 0);
    }

    startResting() {
      this.stopAnimate();
      this.animate(this.obj["Rest"], 0);
    }

    stopAnimate() {
      clearInterval(this.tID);
    }
  }

  const mario = new Mario(mario_metadata);

  ////////// event control /////////

  window.addEventListener("keydown", (event) => {
    if (event.key === "ArrowRight") {
      event.preventDefault();
      if (event.repeat) {
        mario.startCheering();
      } else {
        if (mario.currentSpeed === 0) {
          mario.startWalking();
        } else if (mario.currentSpeed === 3) {
          mario.startRunning();
        }
      }
    } else if (event.key === "ArrowLeft") {
      event.preventDefault();
      if (event.repeat) {
        mario.stopAnimate();
      } else {
        mario.startPuffing();
      }
    }
  });

  //touch events that enable animations
  window.addEventListener("touchstart", (event) => {
    event.preventDefault(); // prevent default browser action
    if (event.touches[0].clientX > window.innerWidth / 2) {
      // move right
      if (currentSpeed === 0) { // if at rest, go to walking
        mario.startWalking();
      } else if (currentSpeed === 3) { // if walking, go to running
        mario.startRunning();
      }
    } else {
      // move left
      mario.startPuffing();
    }
  });

  //stop animation on window blur
  window.addEventListener("blur", () => {
    mario.stopAnimate();
  });

  //start animation on window focus
  window.addEventListener("focus", () => {
     mario.startFlipping();
  });

  //start animation on page load or page refresh
  document.addEventListener("DOMContentLoaded", () => {
    // adjust sprite size for high pixel density devices
    const scale = window.devicePixelRatio;
    const sprite = document.querySelector(".sprite");
    sprite.style.transform = `scale(${0.2 * scale})`;
    mario.startResting();
  });

</script>


