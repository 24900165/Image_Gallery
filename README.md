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
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Chhota Bheem Gallery</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background: #0b1220 ;
            background-size: cover;
            color: #ffffff;
        }

        h1 {
            margin-top: 20px;
            font-size: 3rem;
            text-shadow: 0 0 10px #9b7653;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
        }

        .gallery img {
    width: 190px;
    height: 290px; 
    border: 4px solid #9b7653;
    border-radius: 12px;
    cursor: pointer;
    object-fit: cover;
    transition: transform 0.3s, box-shadow 0.3s;
    box-shadow: 0 0 5px #e0c097;
}

        .gallery img:hover {
            transform: scale(1.1);
            box-shadow: 0 0 20px #c9a75a;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background-color: rgba(11, 18, 32, 0.9);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal img {
            max-width: 90%;
            max-height: 90%;
            border: 5px solid #4e4339;
            border-radius: 15px;
            box-shadow: 0 0 30px #121211;
        }

        .modal span {
            position: absolute;
            top: 25px;
            right: 40px;
            font-size: 40px;
            color: #c9a75a;
            cursor: pointer;
            font-weight: bold;
            text-shadow: 0 0 8px #c9a75a;
        }
    </style>
</head>
<body>
    <h1>KDRAMAS</h1>

    <div class="gallery">
        <img src="untamed.jpg" alt="THE UNTAMED" onclick="openModal(this)">
        <img src="queen.jpg" alt="QUEEN OF TEARS" onclick="openModal(this)">
        <img src="king.jpg" alt="KING THE LAND" onclick="openModal(this)">
        <img src="demon.jpg" alt="MY DEMON" onclick="openModal(this)">
        <img src="vincenzo.jpg" alt="VINCENZO" onclick="openModal(this)">
        <img src="fight.jpg" alt="FIGHT FOR MY WAY" onclick="openModal(this)">
        <img src="love.jpg" alt="LOVE NEXT DOOR" onclick="openModal(this)">
        <img src="bong.jpg" alt="STRONG GIRL DO BONG SOON" onclick="openModal(this)">
        <img src="f4.jpg" alt="F4 THAILAND" onclick="openModal(this)">
        <img src="K2.jpg" alt="THE K2" onclick="openModal(this)">
    </div>

    <div class="modal" id="imageModal">
        <span onclick="closeModal()">&times;</span>
        <img id="modalImage" src="" alt="chhota beem image" />
    </div>

    <script>
        function openModal(image) {
            const modal = document.getElementById('imageModal');
            const modalImg = document.getElementById('modalImage');
            modal.style.display = 'flex';
            modalImg.src = image.src;
            modalImg.alt = image.alt;
        }

        function closeModal() {
            document.getElementById('imageModal').style.display = 'none';
        }
    </script>
</body>
</html>
```

## OUTPUT
![alt text](<Screenshot 2025-11-09 191206.png>)
![alt text](<Screenshot 2025-11-09 191231.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
