# Ex.08 Design of Interactive Image Gallery
## Date:24-05-2024

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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: #040404;
            color: #fff;
        }

        h1, h2 {
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            text-align: center;
        }

        h1 {
            color: #f0f0f1;
        }

        h2 {
            color: #edf5ed;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            max-width: 1200px;
            padding: 10px;
            justify-content: center;
        }

        .gallery-item {
            cursor: pointer;
            text-align: center;
            width: 200px;
            margin: 10px;
            border: 2px solid #101111;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }

        
        #modal {
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

        #modal img {
            max-width: 90%;
            max-height: 90%;
            border: 2px solid #fff;
        }

        #modal .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 30px;
            color: #fff;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <h2>GOAT'S OF FOOTBALL</h2>

    <div class="gallery">
        <div class="gallery-item"><img src="cristiano.webp" alt=""></div>
        <div class="gallery-item"><img src="messi.jpeg" alt=""></div>
        <div class="gallery-item"><img src="messi2.jpeg" alt=""></div>
        <div class="gallery-item"><img src="AP.avif" alt=""></div>
        <div class="gallery-item"><img src="ronaldo2.png" alt=""></div>
        <div class="gallery-item"><img src="RM2.jpg" alt=""></div>
        <div class="gallery-item"><img src="messi2.webp" alt=""></div>
        <div class="gallery-item"><img src="ronaldo.png" alt=""></div>
        <div class="gallery-item"><img src="messironaldo.webp" alt=""></div>
    </div>

    
    <div id="modal">
        <span class="close">&times;</span>
        <img id="modal-img" src="" alt="Enlarged">
    </div>

    <footer>
        &copy; 2024 designed by MUKESH RAJ D 212224100038 All Rights Reserved.
    </footer>

    <script>
        
        const galleryItems = document.querySelectorAll('.gallery-item img');
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modal-img');
        const closeModal = document.querySelector('.close');

        
        galleryItems.forEach(item => {
            item.addEventListener('click', () => {
                modal.style.display = 'flex';
                modalImg.src = item.src; 
            });
        });

        
        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        
        modal.addEventListener('click', (event) => {
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>
</body>
</html>
```

## OUTPUT:

![alt text](<Screenshot 2025-05-25 222032-1.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
