# Ex.08 Design of Interactive Image Gallery
## DATE:22.5.25

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
```
image.html


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
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            padding: 20px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal-content {
            position: relative;
            max-width: 90%;
            max-height: 80%;
        }

        .modal-content img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }

        .modal-close {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #fff;
            border: none;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-size: 18px;
            font-weight: bold;
        }

        .modal-close:hover {
            background-color: #f00;
            color: #fff;
        }
    </style>
</head>
<body>
    <br>
    <br>
    <br>

    <h1 style="text-align: center; margin-top: 20px;">Interactive Photo Gallery</h1>
    <h3 style="text-align: center; margin-top: 20px;">ROSHINI S(212223230174)</h3>
     <br>
     <br>
     <br>
     <br>
     <br>

    <div class="gallery">
        <div class="gallery-item" data-image="image1.jpg">
            <img src="image.1.png" alt="Photo 1">
        </div>
        <div class="gallery-item" data-image="image2.jpg">
            <img src="image.2.jpg" alt="Photo 2">
        </div>
        <div class="gallery-item" data-image="image3.jpg">
            <img src="image.3.jpg" alt="Photo 3">
        </div>
        <div class="gallery-item" data-image="image3.jpg">
          <img src="image.4.webp" alt="Photo 3">
      </div>
      <div class="gallery-item" data-image="image3.jpg">
        <img src="image.5.webp" alt="Photo 3">
    </div>
        
    

    <div class="modal" id="modal">
        <div class="modal-content">
            <button class="modal-close" id="closeModal">&times;</button>
            <img id="modalImage" src="" alt="">
        </div>
    </div>

    <script>
        const galleryItems = document.querySelectorAll('.gallery-item');
        const modal = document.getElementById('modal');
        const modalImage = document.getElementById('modalImage');
        const closeModal = document.getElementById('closeModal');

        galleryItems.forEach(item => {
            item.addEventListener('click', () => {
                const imgSrc = item.getAttribute('data-image');
                modalImage.src = imgSrc;
                modal.style.display = 'flex';
            });
        });

        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>

</body>
</html>
```

## OUTPUT
![WhatsApp Image 2025-05-22 at 16 23 51_69d07087](https://github.com/user-attachments/assets/66a411e0-0794-49be-a106-b18d02937752)


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
