---
title: Interactive Elements Base Code
description: Baseline code for us to add interactive elements into the game
type: game
layout: post
courses: {'versions': {'week': 0}}
---

```python
%%html
<img id="carpet" src="../images/Carpet_Interact.png" alt="Interactive Carpet">
<div id="message-box"></div>
const interactiveImage = document.getElementById("interactive-image");

// Add a keydown event listener to the document
document.addEventListener("keydown", function (event) {
  // Check if the pressed key is "e"
  if (event.key === "e") {
    // Call the function to perform the image action
     displayMessage("E key was pressed!");
  }
});
function displayMessage(message) {
  // Set the content of the message box to the provided message
  messageBox.textContent = message;
}

```


<img id="carpet" src="../images/Carpet_Interact.png" alt="Interactive Carpet">
<div id="message-box"></div>
const interactiveImage = document.getElementById("interactive-image");

// Add a keydown event listener to the document
document.addEventListener("keydown", function (event) {
  // Check if the pressed key is "e"
  if (event.key === "e") {
    // Call the function to perform the image action
     displayMessage("E key was pressed!");
  }
});
function displayMessage(message) {
  // Set the content of the message box to the provided message
  messageBox.textContent = message;
}



# Notes
- Obviously this can't be copied line for line every time we need an interactive element
- Will need to edit what begins the interaction and what the output is depending on situation
- This is a good baseline to use whenever we want to create an interactive element on one of our backgrounds
