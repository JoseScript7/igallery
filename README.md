# Ex.08 Design of Interactive Image Gallery
## Date:15.12.2024
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
    <title>Timeless Moments</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Georgia', serif;
            background-color: #f5f5f5; 
            color: #333;
        }

        header {
            background: linear-gradient(135deg, #f3eac2, #b7d5e8); 
            color: #2f4f4f; 
            text-align: center;
            padding: 100px 20px;
            position: relative;
            z-index: 1;
            border-bottom: 8px solid #d4af37; 
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            font-size: 48px;
            margin: 0;
            font-weight: bold;
        }

        header p {
            font-size: 20px;
            margin-top: 10px;
            color: #6a5f5f; 
            font-style: italic;
        }

        header .description {
            font-size: 18px;
            margin-top: 20px;
            color: #7f8c8d; 
            font-weight: 300;
            line-height: 1.5;
            max-width: 700px;
            margin: 20px auto;
        }

        .gallery-container {
            position: relative;
            margin-top: 50px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 40px;
        }

        .gallery-item {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 15px;
            transition: transform 0.4s ease;
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
        }

        .gallery-item:nth-child(odd) {
            width: 300px;
            height: 350px;
        }

        .gallery-item:nth-child(even) {
            width: 400px;
            height: 300px;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 10;
            justify-content: center;
            align-items: center;
        }

        .modal img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }

        .modal:target {
            display: flex;
        }

        footer {
            background-color: #2f4f4f;
            color: #eaeaea;
            text-align: center;
            padding: 10px;
            font-size: 14px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        .background-image {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url(background.png) no-repeat center center fixed;
            background-size: cover;
            opacity: 0.2;
            z-index: -1;
        }
    </style>
</head>
<body>

<header>
    <h1>Timeless Moments</h1>
    <p>Memories captured in time</p>
    <div class="description">
        Memories are windows to the soul, telling stories of our journey and preserving the beauty of fleeting moments. Here’s a collection that brings cherished experiences back to life.
    </div>
</header>

<div class="background-image"></div>

<div class="gallery-container">
    <div class="gallery-item" onclick="openModal('memory1.png')">
        <img src="memory1.png" alt="Memory 1">
    </div>
    <div class="gallery-item" onclick="openModal('memory2.png')">
        <img src="memory2.png" alt="Memory 2">
    </div>
    <div class="gallery-item" onclick="openModal('memory3.png')">
        <img src="memory3.png" alt="Memory 3">
    </div>
    <div class="gallery-item" onclick="openModal('memory4.png')">
        <img src="memory4.png" alt="Memory 4">
    </div>
    <div class="gallery-item" onclick="openModal('memory5.png')">
        <img src="memory5.png" alt="Memory 5">
    </div>
    <div class="gallery-item" onclick="openModal('memory6.png')">
        <img src="memory6.png" alt="Memory 6">
    </div>
</div>

<div id="modal" class="modal" onclick="closeModal()">
    <img id="modal-img" src="" alt="Zoomed Image">
</div>

<footer>
    Designed and developed by Ranen Joseph Solomon
</footer>

<script>
    function openModal(imageSrc) {
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modal-img');
        modal.style.display = 'flex';
        modalImg.src = imageSrc;
    }

    function closeModal() {
        const modal = document.getElementById('modal');
        modal.style.display = 'none';
    }
</script>

</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot 2024-12-15 200029.png>) 
![alt text](<Screenshot 2024-12-15 195950.png>) 
![alt text](<Screenshot 2024-12-15 200008.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
