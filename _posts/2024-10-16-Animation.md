<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #8CEEED;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            color: black; /* Set text color to black */
        }

        #animation-container {
            position: relative;
        }

        canvas {
            display: block;
            margin: 0 auto;
        }
    </style>
</head>

<body>
    <div id="animation-container">
        <canvas id="spriteContainer"> <!-- Within the base div is a canvas. An HTML canvas is used only for graphics. It allows the user to access some basic functions related to the image created on the canvas (including animation) -->
            <img id="dogSprite" src="{{site.baseurl}}/images/pegasus.png">  <!-- change sprite here -->
        </canvas>
        <div id="controls"> <!--basic radio buttons which can be used to check whether each individual animation works -->
            <input type="radio" name="animation" id="idle" checked>
            <label for="idle">Backwards</label><br>
            <input type="radio" name="animation" id="barking">
            <label for="barking">Sideways</label><br>
            <input type="radio" name="animation" id="walking">
            <label for="walking">Forwards</label><br>
        </div>
    </div>
    <script>
        // start on page load
        window.addEventListener('load', function () {
            const canvas = document.getElementById('spriteContainer');
            const ctx = canvas.getContext('2d');
            const SPRITE_WIDTH = 64;  // matches sprite pixel width
            const SPRITE_HEIGHT = 90; // matches sprite pixel height
            const FRAME_LIMIT = 2;  // matches number of frames per sprite row, this code assumes each row is the same

            const SCALE_FACTOR = 5;  // control size of sprite on canvas
            canvas.width = SPRITE_WIDTH * SCALE_FACTOR;
            canvas.height = SPRITE_HEIGHT * SCALE_FACTOR;

            class Dog {
                constructor() {
                    this.image = document.getElementById("dogSprite");
                    this.x = 0;
                    this.y = 0;
                    this.minFrame = 0;
                    this.maxFrame = FRAME_LIMIT;
                    this.frameX = 0;
                    this.frameY = 0;
                }

                // draw dog object
                draw(context) {
                    context.drawImage(
                        this.image,
                        this.frameX * SPRITE_WIDTH,
                        this.frameY * SPRITE_HEIGHT,
                        SPRITE_WIDTH,
                        SPRITE_HEIGHT,
                        this.x,
                        this.y,
                        canvas.width,
                        canvas.height
                    );
                }
                                // update frameX of object
                update() {
                    if (this.frameX < this.maxFrame) {
                        this.frameX++;
                    } else {
                        this.frameX = 0;
                    }
                }
            }
            // dog object
            const dog = new Dog();

            // update frameY of dog object based on radio button selection
            const controls = document.getElementById('controls');
            controls.addEventListener('click', function (event) {
                if (event.target.tagName === 'INPUT') {
                    const selectedAnimation = event.target.id;
                    switch (selectedAnimation) {
                        case 'idle':
                            dog.frameY = 0;
                            break;
                        case 'barking':
                            dog.frameY = 1;
                            break;
                        case 'walking':
                            dog.frameY = 2;
                            break;
                        default:
                            break;
                    }
                }
            });

            function animate() {
                // Clears the canvas to remove the previous frame.
                ctx.clearRect(0, 0, canvas.width, canvas.height);

                // Draws the current frame of the sprite.
                dog.draw(ctx);

                // Updates the `frameX` property to prepare for the next frame in the sprite sheet.
                dog.update();

                // Uses `requestAnimationFrame` to synchronize the animation loop with the display's refresh rate,
                // ensuring smooth visuals.
                setTimeout(function () {
            // Use `requestAnimationFrame` to continue the animation loop
            requestAnimationFrame(animate);
        }, 500 / 5); // Adjust the divisor to set the desired frames per second
    }

    // run 1st animate
    animate();
});
</script>
</body>

</html>
