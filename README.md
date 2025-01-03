# Ex.08 Design of Interactive Image Gallery
## Date: 25.12.2024

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

html code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            padding: 20px;
        }
        .gallery img {
            width: 200px;
            height: 150px;
            object-fit: cover;
            cursor: pointer;
            border: 2px solid transparent;
            transition: transform 0.3s, border-color 0.3s;
        }
        .gallery img:hover {
            transform: scale(1.1);
            border-color: #007BFF;
        }
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
        }
        .modal img {
            max-width: 90%;
            max-height: 90%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }
        .modal .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 30px;
            color: white;
            cursor: pointer;
        }
    </style>
</head>
<body>

<h1 style="text-align: center; padding: 20px;">Interactive Photo Gallery</h1>
<div class="gallery">
    <img src="475309.webp" alt="Image 1" data-large="475309.webp">
    <img src="3458928.jpg" alt="Image 2" data-large="3458928.jpg">
    <img src="d7JcFSq.webp" alt="Image 3" data-large="d7JcFSq.webp">
    <img src="R.jpeg" alt="Image 4" data-large="R.jpeg">
    <img src="898e0893906d7fb3baf4547c4e64a5f3.jpg" alt="Image 5" data-large="898e0893906d7fb3baf4547c4e64a5f3.jpg">
</div>

<div class="modal" id="modal">
    <span class="close" id="close">&times;</span>
    <img id="modalImage" src="" alt="">
</div>

<script>
    // Select all gallery images and modal elements
    const galleryImages = document.querySelectorAll('.gallery img');
    const modal = document.getElementById('modal');
    const modalImage = document.getElementById('modalImage');
    const closeModal = document.getElementById('close');

    // Function to open the modal with the selected image
    galleryImages.forEach(image => {
        image.addEventListener('click', () => {
            modalImage.src = image.dataset.large;
            modal.style.display = 'flex';
        });
    });

    // Function to close the modal
    closeModal.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    // Close the modal when clicking outside the image
    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            modal.style.display = 'none';
        }
    });
</script>

</body>
</html>




## OUTPUT:

![alt text](<img/Screenshot 2024-12-25 141120.png>)
![alt text](<img/Screenshot 2024-12-25 141132.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
