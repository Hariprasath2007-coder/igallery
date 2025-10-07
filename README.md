# Ex.08 Design of Interactive Image Gallery
## Date: 07-10-2025
## Name: HARI PRASATH E
## Ref No: 25007799

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
image.html

<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Photo Gallery</title>
  <link rel="stylesheet" href="image.css">
</head>
<body>
  <h1>Image Gallery</h1>
  <div class="gallery">
    <img src="luffy.png" alt="LUFFY" class="thumbnail">
    <img src="zoro.png" alt="ZORO" class="thumbnail">
    <img src="sanji.png" alt="SANJI" class="thumbnail">
    <img src="robin.png" alt="ROBIN" class="thumbnail">
    <img src="nami.png" alt="NAMI" class="thumbnail">
    <img src="chopper.png" alt="CHOPPER" class="thumbnail">
    <img src="brook.png" alt="BROOK" class="thumbnail">
    <img src="jimbei.png" alt="JIMBEI" class="thumbnail">
    <img src="franky.png" alt="FRANKY" class="thumbnail">
    <img src="usoop.png" alt="USOOP" class="thumbnail">
  </div>

  <div id="overlay">
    <span id="closeBtn">&times;</span>
    <img id="overlayImg" src="" alt="Expanded view">
  </div>
  <p>&copyImage gallery created by HARI PRASATH E</p>
  <script src="image.js"></script>
</body>
</html>

image.css

body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #f4f4f4;
}

.gallery {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 20px;
}

.thumbnail {
  width: 150px;
  height: auto;
  cursor: pointer;
  border: 2px solid #ccc;
  transition: transform 0.2s;
}

.thumbnail:hover {
  transform: scale(1.05);
  border-color: #333;
}

#overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.8);
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

#overlayImg {
  max-width: 80%;
  max-height: 80%;
  border: 5px solid white;
}

#closeBtn {
  position: absolute;
  top: 20px;
  right: 40px;
  font-size: 40px;
  color: white;
  cursor: pointer;
}

image.js

document.addEventListener("DOMContentLoaded", () => {
  const thumbnails = document.querySelectorAll(".thumbnail");
  const overlay = document.getElementById("overlay");
  const overlayImg = document.getElementById("overlayImg");
  const closeBtn = document.getElementById("closeBtn");

  thumbnails.forEach(img => {
    img.addEventListener("click", () => {
      overlayImg.src = img.src;
      overlay.style.display = "flex";
    });
  });

  closeBtn.addEventListener("click", () => {
    overlay.style.display = "none";
    overlayImg.src = "";
  });

  overlay.addEventListener("click", (e) => {
    if (e.target === overlay) {
      overlay.style.display = "none";
      overlayImg.src = "";
    }
  });
});


```
## OUTPUT:
<img width="1905" height="1068" alt="Screenshot 2025-10-07 213104" src="https://github.com/user-attachments/assets/0633e8b4-375e-41a4-a46c-303e1e2a9237" />
<img width="1910" height="1052" alt="Screenshot 2025-10-07 213118" src="https://github.com/user-attachments/assets/5623a18a-ed0f-4c96-af5f-4b6b36e1d7f4" />



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
