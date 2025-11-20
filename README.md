# Ex.08 
# Design of Interactive Image Gallery

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
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Cars and Bikes Image Gallery</title>
  <link rel="stylesheet" href="gallery.css" />
</head>
<body>
  <h1 class="title">Image Gallery</h1>

  <div class="gallery">
    <img src="IMAGE1.jpeg" alt="Royal Enfield Continental GT 650" />
    <img src="IMAGE2.jpeg" alt="Kawasaki Z900" />
    <img src="IMAGE3.jpeg" alt="BMW" />
    <img src="IMAGE4.jpeg" alt="Rolls-Royce" />
    <img src="IMAGE5.jpeg" alt="Lamborghini" />
  </div>

  <div id="lightbox" class="lightbox">
    <span class="close">&times;</span>
    <img class="lightbox-content" id="lightbox-img" />
  </div>

  <script src="gallery.js"></script>
</body>
</html>

```

gallery.css
```
body {
  font-family: 'Poppins', sans-serif;
  background-color: #0a0a0a;
  color: white;
  text-align: center;
  margin: 0;
  padding: 0;
}

.title {
  margin: 20px;
  font-size: 2rem;
  letter-spacing: 2px;
  color: #ff4500;
  text-transform: uppercase;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 15px;
  padding: 20px;
}

.gallery img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 12px;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.gallery img:hover {
  transform: scale(1.05);
  box-shadow: 0 5px 15px rgba(255, 69, 0, 0.4);
}

.lightbox {
  display: none;
  position: fixed;
  z-index: 1000;
  padding-top: 80px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
}

.lightbox-content {
  margin: auto;
  display: block;
  max-width: 80%;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(255, 69, 0, 0.7);
}

.close {
  position: absolute;
  top: 40px;
  right: 60px;
  color: white;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
  transition: color 0.3s ease;
}

.close:hover {
  color: #ff4500;
}
```

gallery.jss
```
const galleryImages = document.querySelectorAll('.gallery img');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');
const closeBtn = document.querySelector('.close');

galleryImages.forEach(img => {
  img.addEventListener('click', () => {
    lightbox.style.display = 'block';
    lightboxImg.src = img.src;
  });
});

closeBtn.addEventListener('click', () => {
  lightbox.style.display = 'none';
});

lightbox.addEventListener('click', (e) => {
  if (e.target !== lightboxImg) {
    lightbox.style.display = 'none';
  }
});
```
## OUTPUT
<img width="1265" height="471" alt="image" src="https://github.com/user-attachments/assets/99c516d7-af8a-4627-b338-81e5541d71af" />
<img width="1257" height="613" alt="image" src="https://github.com/user-attachments/assets/9ad1827d-bd4d-425c-b202-6c5dbd81738b" />
<img width="1257" height="633" alt="image" src="https://github.com/user-attachments/assets/f12c4ff9-64c9-4c8d-921a-d0883abf373f" />
<img width="1260" height="684" alt="image" src="https://github.com/user-attachments/assets/e62e1846-72ee-4377-8367-6339c4109d37" />
<img width="1253" height="723" alt="image" src="https://github.com/user-attachments/assets/1c78b039-fe9e-4236-ad34-9288e0aafde9" />


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
