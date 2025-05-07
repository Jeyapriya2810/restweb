# Ex.07 Restaurant Website
## Date:

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GRAND | Home</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Playfair+Display:wght@700&family=Montserrat:wght@400&display=swap"
        rel="stylesheet">
    <style>
        /* General Reset & Body */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            color: #333;
            background: linear-gradient(135deg, #f0f4f8, #d9e2ec);
            line-height: 1.6;
            transition: background 0.3s ease;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: #ffffff;
            padding: 15px 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        header img {
            height: 50px;
            transition: transform 0.3s ease;
        }

        header img:hover {
            transform: scale(1.1);
        }

        nav {
            display: flex;
            gap: 20px;
        }

        nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            transition: color 0.3s ease, transform 0.2s ease;
            font-size: 1rem;
        }

        nav a:hover {
            color: #f4b400;
            transform: translateY(-2px);
        }

        /* Banner Section */
        .banner {
            height: 400px;
            background: url('https://source.unsplash.com/1600x900/?restaurant') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            position: relative;
            text-shadow: 0 5px 10px rgba(0, 0, 0, 0.7);
        }

        .banner-content {
            background: rgba(0, 0, 0, 0.6);
            padding: 20px 35px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .banner-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            color: #f4b400;
        }

        .banner-content p {
            margin: 10px 0;
            font-size: 1.2rem;
            color: #e2e8f0;
        }

        .banner-content a {
            text-decoration: none;
            background: #f4b400;
            padding: 10px 20px;
            color: #333;
            font-weight: 700;
            border-radius: 25px;
            transition: background 0.3s ease, transform 0.3s ease;
        }

        .banner-content a:hover {
            background: #e09e00;
            transform: translateY(-3px);
        }

        /* Features Grid Section */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 30px 15px;
            background: #ffffff;
            border-top: 1px solid #d1d5e0;
        }

        .feature {
            background: #f9f9f9;
            padding: 15px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s ease, box-shadow 0.3s ease;
            text-align: center;
        }

        .feature:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        .feature img {
            max-width: 100%;
            height: 120px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .feature img:hover {
            transform: scale(1.1);
        }

        .feature h3 {
            font-family: 'Montserrat', sans-serif;
            margin: 10px 0;
            font-size: 1.1rem;
            color: #333;
        }

        .feature p {
            font-size: 0.9rem;
            color: #555;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
            text-align: center;
            padding: 15px 20px;
            font-size: 0.9rem;
        }

        footer a {
            color: #f4b400;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #e09e00;
        }

        /* Responsiveness */
        @media (max-width: 768px) {
            .banner-content h1 {
                font-size: 2.2rem;
            }

            .banner-content p {
                font-size: 1rem;
            }

            header {
                flex-direction: column;
                gap: 10px;
            }
        }

        @media (max-width: 480px) {
            .banner-content h1 {
                font-size: 1.8rem;
            }

            .features {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>
    <!-- Header Section -->
    <header>
        <img src="logo.webp" alt="Modern Muse Logo">
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Admin</a>
        </nav>
    </header>

    <!-- Banner Section -->
    <div class="banner">
        <div class="banner-content">
            <h1>GRAND</h1>
            <p>Serving You the Finest Cuisine</p>
            <a href="#features">Discover More</a>
        </div>
    </div>

    <!-- Features Section -->
    <section class="features">
        <div class="feature">
            <img src="dosa.webp" alt="High quality dishes">
            <h3>High Quality Dishes</h3>
            <p>Indulge in the finest and freshest meals crafted with love and expertise.</p>
        </div>
    </section>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2024 GRAND. All rights reserved. | <a href="#">Privacy Policy</a></p>
    </footer>
</body>

</html>
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/0ba73e76-0fce-4b9e-b97f-d0ab8bf03b2f)

![image](https://github.com/user-attachments/assets/f1ad0661-46f6-4b75-9937-26ff50298dd1)

![image](https://github.com/user-attachments/assets/10d949ee-7e5e-4527-962f-eeda0bb774cd)

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
