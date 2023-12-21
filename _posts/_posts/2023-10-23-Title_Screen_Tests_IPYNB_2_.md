---
title: Title Screen Animation Tests
description: Testing the looping of the Title Screen
layout: post
type: ccc
courses: {'versions': {'week': 1}}
comments: False
---

```python
%%html

<html>
<head>
    <title>GIF Switcher</title>
</head>
<body>
    <button id="showGifButton">Start Animation</button>
    <img id="gifImage" style="display: none;">
    
    <script>
        const gif1 = "{{ site.baseurl }}/images/pokemortloop1.gif"; // First loop with title animation
        const gif2 = "{{ site.baseurl }}/images/pokemortloop2.gif"; // Second loop with standstill title and only clouds moving

        const gifImage = document.getElementById("gifImage");
        const showGifButton = document.getElementById("showGifButton");

        showGifButton.addEventListener("click", function() {
            gifImage.src = gif1;
            gifImage.style.display = "block";
            showGifButton.disabled = true;
            
            setTimeout(function() {
                gifImage.src = gif2;
            }, 11100); // Switch to the second GIF after 12 seconds
        });
    </script>
</body>
</html>



```



<html>
<head>
    <title>GIF Switcher</title>
</head>
<body>
    <button id="showGifButton">Start Animation</button>
    <img id="gifImage" style="display: none;">

    <script>
        const gif1 = "{{ site.baseurl }}/images/pokemortloop1.gif"; // First loop with title animation
        const gif2 = "{{ site.baseurl }}/images/pokemortloop2.gif"; // Second loop with standstill title and only clouds moving

        const gifImage = document.getElementById("gifImage");
        const showGifButton = document.getElementById("showGifButton");

        showGifButton.addEventListener("click", function() {
            gifImage.src = gif1;
            gifImage.style.display = "block";
            showGifButton.disabled = true;

            setTimeout(function() {
                gifImage.src = gif2;
            }, 11100); // Switch to the second GIF after 12 seconds
        });
    </script>
</body>
</html>




