---
title: Changing Backgrounds with Classes
description: Easier way for us to change out the game backgrounds using classes and a loadZone
layout: post
type: ccc
courses: {'csse': {'week': 1}}
---

```python
%%js

// Build the parent class
class LoadZone{
    constructor(dimensions, imageSource){
    this.dimensions = "dimensions";
    this.imageSource = "imageSource";
    }

    // Save the characteristics from parent class so we can super later on
    print(){
        console.log(this.dimensions
                    this.imageSource)
    }
}

// Make a child class to extend the LoadZone parent class
class Rug extends LoadZone{
    constructor(dimensions, imageSource){
        super (dimensions, imageSource)
    }
}

// Define the variables
var rugDimensions = "8x10" // Replace with whatever dimension apply
var rugimageSource = "../images/Carpet_Interact.png" // Replace with whatever image applies (3 of ../ for a .md psot)
var rug = new Rug(rugDimensions, rugimageSource)

var loadZones = [rug]; // Use an array to store the animals
for (var loadZone of loadZones) {
    loadZones.print();
}
```

# Notes
- This may not be needed if Nate's collision code works with the intersecting rectangles
- Class mostly comes into play with the rectangles since it can allow us to easily create a list of collision zones that can all be checked at once
- I think the most liekly place where we use this is just holding a list of hitbox properties that will remain consistent 
    - Maybe a parent class for changeBackground hitboxes, maybe a parent class for interaction hitboxes


```python
%%js

// Define the hitbox coordinates and dimensions
const hitboxX = 100; // Replace with the X-coordinate of whatever hitbox we are using 
const hitboxY = 100; // Replace with the Y-coordinate of whatever hitbox we are using
const hitboxWidth = 50; // Replace with the width of whatever hitbox we are using
const hitboxHeight = 50; // Replace with the height of whatever hitbox we are using

// Function to check if the sprite rectangle is inside the hitbox
function isPointInsideHitbox(x, y) {
    return (
        x >= hitboxX &&
        x <= hitboxX + hitboxWidth &&
        y >= hitboxY &&
        y <= hitboxY + hitboxHeight
    );
}

// Function to change the background
function changeBackground(newBackgroundImage) {
    const canvas = document.getElementById('game-canvas');
    canvas.style.backgroundImage = `url(${newBackgroundImage})`;
    // We may need to change other styles such as background dimensions based on our needs
}

// Change accordingly depending on our existing code for collision logic
function handleCollision(spriteX, spriteY) {
    // Check if the sprite's position is inside the hitbox
    if (isPointInsideHitbox(spriteX, spriteY)) {
        // Call the changeBackground function with the new background image URL
        changeBackground('new-background-image.jpg');
    }
}
```


    <IPython.core.display.Javascript object>

