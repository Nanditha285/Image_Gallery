# Ex.07 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
gallery.html
```
% load static %}

<!DOCTYPE html>
<html>
<head>
<title>Interactive Image Gallery</title>

<style>
body{
    text-align:center;
    font-family:Arial;
}

img{
    width:500px;
    height:300px;
    border-radius:10px;
}

button{
    padding:10px 20px;
    margin:10px;
}
</style>

</head>

<body>

<h1>Interactive Image Gallery</h1>

<img id="gallery" src="{% static 'images/img1.jpg' %}">

<br>

<button onclick="prevImage()">Previous</button>
<button onclick="nextImage()">Next</button>

<script>

let images = [
"{% static 'images/image.png' %}",
"{% static 'images/image2.png' %}",
"{% static 'images/image3.png' %}",
"{% static 'images/image4.png' %}",
"{% static 'images/image5.png' %}"
];

let current = 0;

function nextImage(){
    current=(current+1)%images.length;
    document.getElementById("gallery").src=images[current];
}

function prevImage(){
    current=(current-1+images.length)%images.length;
    document.getElementById("gallery").src=images[current];
}

</script>

</body>
</html>
```

## OUTPUT
![alt text](<Screenshot 2026-06-02 134053.png>)
![alt text](<Screenshot 2026-06-02 134037.png>)
![alt text](<Screenshot 2026-06-02 134023.png>)
![alt text](<Screenshot 2026-06-02 133937.png>)
![alt text](<Screenshot 2026-06-02 133922.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
