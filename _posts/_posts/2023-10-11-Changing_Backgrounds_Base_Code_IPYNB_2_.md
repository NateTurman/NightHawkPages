---
title: Changing Backgrounds Base Code
description: Base code that we can use to change the backdrop of our game via interactive elements (carpet, doors, invsible, etc.)
courses: {'versions': {'week': 0}}
type: game
layout: post
---

```python
%%html
<img id="game-background" src="../images/InitialBackdrop.png" width="384" height="576">
function changeBackground(element, newBackground) {
    element.setAttribute("src","../images/NewBackdrop.png");
    element.setAttribute("width","384")
    element.setAttribute("height","576")

}

// Example use
const backgroundElement = document.getElementById("game-background");
const newBackgroundImage = "../images/NewBackdrop.png"; // Change to the path of your new .png image

// Call the function to change the background
changeBackground(backgroundElement, newBackgroundImage);
// Function to change background on "e" key press
        function handleKeyPress(event) {
            if (event.key === "e") {
                changeBackground(backgroundElement, newBackgroundImage);
            }
        }

        // Add event listener to the document
        document.addEventListener("keydown", handleKeyPress);

```


<img id="game-background" src="../images/InitialBackdrop.png" width="384" height="576">
function changeBackground(element, newBackground) {
    element.setAttribute("src","../images/NewBackdrop.png");
    element.setAttribute("width","384")
    element.setAttribute("height","576")

}

// Example use
const backgroundElement = document.getElementById("game-background");
const newBackgroundImage = "../images/NewBackdrop.png"; // Change to the path of your new .png image

// Call the function to change the background
changeBackground(backgroundElement, newBackgroundImage);
// Function to change background on "e" key press
        function handleKeyPress(event) {
            if (event.key === "e") {
                changeBackground(backgroundElement, newBackgroundImage);
            }
        }

        // Add event listener to the document
        document.addEventListener("keydown", handleKeyPress);


