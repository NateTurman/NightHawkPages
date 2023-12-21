---
title: Music Test
description: First MP3 added
layout: post
type: ccc
courses: {'versions': {'week': 1}}
comments: False
---

```python
%%html 

<head>
    <!-- Add background music and control button -->
    <audio id="backgroundMusic" loop autoplay>
        <source src="{{ site.baseurl }}/images/plug2919.mp3" type="audio/mpeg">
    </audio>

    <button id="audioControlButton">Toggle Music</button>
</head>

<html>
    <div class="gameWrapper">
        <!-- Your existing code... -->
    </div>
</html>

<script>
    // Get the audio element and the control button by their IDs
    const backgroundMusic = document.getElementById("backgroundMusic");
    const audioControlButton = document.getElementById("audioControlButton");

    // Function to toggle the audio (play/pause)
    function toggleAudio() {
        if (backgroundMusic.paused) {
            backgroundMusic.play();
        } else {
            backgroundMusic.pause();
        }
    }

    // Add a click event listener to the control button
    audioControlButton.addEventListener("click", toggleAudio);
</script>
```
