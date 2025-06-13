# yzha0873_9103_Joel_E


1. How to Interact with My Code
    When the animation runs, a ghost character automatically appears from the left side every 2 seconds.
    It gradually moves across the bridge toward the central screaming figure. The more time passes, the more ghosts appear, simulating a tense, haunted atmosphere.

2. Animation Technique Details
    2.1  Animation Driver 
        Time-based (using frameCount % 120 === 0 to add one ghost every 2 seconds)
    2.2  Animated Image Properties
        Ghosts are drawn using a custom SVG-to-p5.js converted path
        Position (x, y) changes over time
        Movement speed controlled via object values (speedX, speedY)
        scale() controls character size
    2.3  Why it’s unique
        My animation is driven by time, continuously adding characters and simulating movement to create a more vivid and interconnected narrative between the two figures.
        While the other three team members used Perlin noise and randomness, audio, or user input, my animation uniquely changes the number of elements dynamically.

3. Inspirations & Tools Used
    3.1  Inspired by Studio Ghibli's “No-Face” (Kaonashi) and horror game pacing
    3.2  Character created in Adobe Illustrator → exported to SVG
    3.3  SVG path copied into VS Code → converted using ChatGPT & svg2p5.com
    3.4  p5.js translate(), scale(), bezierVertex() used for drawing
    3.5  Movement logic uses very basic array.push() and loop with position updating

4. Technical Implementation
    4.1  I declared an empty array let ghosts = [] in global scope to store all ghost objects.
    4.2  In draw(), every 120 frames, I used ghosts.push() to add a new object with starting position and speed.
    4.3  Then I used a for loop to move each ghost by updating x and y.
    4.4  I adjusted start points repeatedly to avoid overlap with the scream character.
    4.5  I used basic quad() and line() functions to build a slanted bridge with railings, testing positions manually.

5. Code Reference & Learning Sources
    ChatGPT-prompted SVG to p5 converter
    svg2p5.com
    YouTube BezierVertex Tutorial
    p5.js Reference: translate(), scale(), frameCount


