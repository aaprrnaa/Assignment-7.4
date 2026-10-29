
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.3 - Responsive Product Listing</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f4f6f9;
            color: #333;
        }

        header {
            background-color: #2563eb;
            color: white;
            text-align: center;
            padding: 25px 15px;
        }

        header h1 {
            margin-bottom: 8px;
        }

        .product-section {
            max-width: 1200px;
            margin: 0 auto;
            padding: 35px 20px;
        }

        .product-section h2 {
            text-align: center;
            margin-bottom: 25px;
        }

        /* Flexbox product container */
        .product-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: stretch;
            gap: 24px;
        }

        /* Product card */
        .product-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);

            /* Flexbox sizing properties */
            flex-grow: 1;
            flex-shrink: 1;
            flex-basis: 250px;

            max-width: 350px;
            display: flex;
            flex-direction: column;
            transition: transform 0.2s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-card img {
            width: 100%;
            height: 210px;
            object-fit: cover;
            display: block;
        }

        .product-info {
            padding: 18px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            gap: 12px;
            flex-grow: 1;
        }

        .product-info h3 {
            font-size: 19px;
        }

        .description {
            font-size: 14px;
            color: #666;
            line-height: 1.5;
        }

        .price {
            color: #2563eb;
            font-size: 22px;
            font-weight: bold;
        }

        .product-btn {
            margin-top: auto;
            width: 100%;
            padding: 12px;
            background: #2563eb;
            color: white;
            border: none;
            border-radius: 6px;
            font-size: 15px;
            cursor: pointer;
        }

        .product-btn:hover {
            background: #1d4ed8;
        }

        footer {
            text-align: center;
            padding: 20px;
            background: #e5e7eb;
            color: #555;
        }

        /* Mobile responsive layout */
        @media (max-width: 600px) {
            .product-section {
                padding: 25px 15px;
            }

            .product-container {
                flex-direction: column;
                align-items: center;
                gap: 20px;
            }

            .product-card {
                flex: 1 1 auto;
                width: 100%;
                max-width: 400px;
            }

            .product-card img {
                height: 230px;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>ShopEase</h1>
        <p>Discover quality products at great prices</p>
    </header>

    <main class="product-section">
        <h2>Our Products</h2>

        <div class="product-container">

            <!-- Product 1 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=600&q=80"
                     alt="Wireless headphones">
                <div class="product-info">
                    <h3>Wireless Headphones</h3>
                    <p class="description">Enjoy clear sound and comfortable listening.</p>
                    <p class="price">$49.99</p>
                    <button class="product-btn" type="button">Add to Cart</button>
                </div>
            </article>

            <!-- Product 2 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=600&q=80"
                     alt="Classic wristwatch">
                <div class="product-info">
                    <h3>Classic Watch</h3>
                    <p class="description">A stylish watch for everyday use.</p>
                    <p class="price">$79.99</p>
                    <button class="product-btn" type="button">Add to Cart</button>
                </div>
            </article>

            <!-- Product 3 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=600&q=80"
                     alt="Red sports shoes">
                <div class="product-info">
                    <h3>Sports Shoes</h3>
                    <p class="description">Lightweight shoes designed for daily comfort.</p>
                    <p class="price">$59.99</p>
                    <button class="product-btn" type="button">Add to Cart</button>
                </div>
            </article>

            <!-- Product 4 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?auto=format&fit=crop&w=600&q=80"
                     alt="Vintage camera">
                <div class="product-info">
                    <h3>Digital Camera</h3>
                    <p class="description">Capture memorable moments in style.</p>
                    <p class="price">$299.99</p>
                    <button class="product-btn" type="button">Add to Cart</button>
                </div>
            </article>

            <!-- Product 5 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1546868871-7041f2a55e12?auto=format&fit=crop&w=600&q=80"
                     alt="Smartwatch">
                <div class="product-info">
                    <h3>Smart Watch</h3>
                    <p class="description">Track activity and stay connected on the go.</p>
                    <p class="price">$129.99</p>
                    <button class="product-btn" type="button">Add to Cart</button>
                </div>
            </article>

            <!-- Product 6 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1503602642458-232111445657?auto=format&fit=crop&w=600&q=80"
                     alt="Modern chair">
                <div class="product-info">
                    <h3>Modern Chair</h3>
                    <p class="description">A comfortable chair for your home or office.</p>
                    <p class="price">$89.99</p>
                    <button class="product-btn" type="button">Add to Cart</button>
                </div>
            </article>

        </div>
    </main>

    <footer>
        <p>&copy; 2026 ShopEase. All rights reserved.</p>
    </footer>

</body>
</html>
