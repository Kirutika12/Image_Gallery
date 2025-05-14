# Ex.08 Design of Interactive Image Gallery

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
<h2 align="center">SEVEN WONDERS OF THE WORLD</h2>
<!DOCTYPE html>


<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 
  <title>Image Gallery</title>
  

  <link rel="stylesheet" href="styles.css">

</head>
<style>
 
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  padding: 20px;
}

.image-container {
  position: relative;
  overflow: hidden;
  width: 500px;
  height: 400px;
}

.gallery-item {
  width: 100%;
  height: auto;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.1);
}


.modal {
  display: none; 
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  overflow: auto;
}

.modal-content {
  display: block;
  margin: auto;
  max-width: 80%;
  max-height: 80%;
}

.close {
  color: #fff;
  font-size: 40px;
  font-weight: bold;
  position: absolute;
  top: 10px;
  right: 25px;
  transition: 0.3s;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #ddd;
  text-decoration: none;
  cursor: pointer;
}

#caption {
  text-align: center;
  color: #fff;
  font-size: 20px;
  padding: 10px;
}

</style>
<body>

  <div class="gallery">
    <div class="image-container">
      <img src="MACHU PICCHU.png"  alt="MACHU PICCHU" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="TAJMAHAL.png"  alt="TAJMAHAL" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="THE COLOSSEUM.png"  alt="THE COLOSSEUM" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="GREAT WALL OF CHINA.png" alt="GREAT WALL OF CHINA" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="PETRA.png"  alt="PETRA" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="CHICHEN ITZA.png"  alt="CHICHEN ITZA" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="CHRIST THE REDEEMER.png"  alt="CHRIST THE REDEEMER" class="gallery-item">
    </div>    
  </div>

  
  <div id="myModal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="img01">
    <div id="caption"></div>
  </div>

  <script>
  
const modal = document.getElementById("myModal");
const modalImg = document.getElementById("img01");
const captionText = document.getElementById("caption");
const closeBtn = document.getElementsByClassName("close")[0];


const images = document.querySelectorAll(".gallery-item");


images.forEach(img => {
  img.onclick = function() {
    modal.style.display = "block";
    modalImg.src = this.src;
    captionText.innerHTML = this.alt;
  };
});


closeBtn.onclick = function() {
  modal.style.display = "none";
};


window.onclick = function(event) {
  if (event.target === modal) {
    modal.style.display = "none";
  }
};

  </script>
  <footer>
    <h2 align="center">Designed and developed by K.R.KIRUTIKA</h2>
  </footer>
</body>
</html
```


## OUTPUT
![alt text](<Screenshot (15).png>)

![alt text](<Screenshot 2025-05-14 190805.png>)

![alt text](<Screenshot (16).png>)

![alt text](<Screenshot (17).png>)

![alt text](<Screenshot (18).png>)

![alt text](<Screenshot 2025-05-14 190107.png>)

![alt text](<Screenshot 2025-05-14 190119.png>)

![alt text](<Screenshot 2025-05-14 190130.png>)

![alt text](<Screenshot 2025-05-14 190649.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
