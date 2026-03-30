<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gazania Restaurant LLC - Authentic Middle Eastern Cuisine in Al Warqa, Dubai</title>
    <meta name="description" content="Experience the finest Middle Eastern cuisine at Gazania Restaurant in Al Warqa, Dubai. Specializing in grilled meats, shawarma, and traditional dishes. Order now or reserve your table!">
    <meta name="keywords" content="Best restaurant in Al Warqa, Shawarma Dubai, Charcoal chicken Dubai, Middle Eastern cuisine, Iranian shawarma, Dubai restaurant">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --gold: #D4AF37;
            --dark-brown: #3E2723;
            --beige: #F5E6D3;
            --white: #FFFFFF;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--dark-brown);
            background: var(--white);
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
        }

        .nav-sticky {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background: rgba(62, 39, 35, 0.98);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .hero-bg {
            background: linear-gradient(rgba(62, 39, 35, 0.7), rgba(62, 39, 35, 0.7)), 
                        url('https://api.kuse.ai/api/folder/v1/file/35ca3ab33ce11bfb22af6c747d267ad665234b0186e557cc0f6175968ae5b215_2759491.jpeg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            min-height: 100vh;
        }

        .btn-primary {
            background: var(--gold);
            color: var(--dark-brown);
            padding: 14px 32px;
            border-radius: 8px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid var(--gold);
            display: inline-block;
            text-decoration: none;
        }

        .btn-primary:hover {
            background: transparent;
            color: var(--gold);
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.3);
        }

        .btn-secondary {
            background: transparent;
            color: var(--white);
            padding: 14px 32px;
            border-radius: 8px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid var(--white);
            display: inline-block;
            text-decoration: none;
        }

        .btn-secondary:hover {
            background: var(--white);
            color: var(--dark-brown);
            transform: translateY(-2px);
        }

        .card {
            background: var(--white);
            border-radius: 16px;
            padding: 24px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            border: 2px solid rgba(212, 175, 55, 0.1);
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 40px rgba(212, 175, 55, 0.2);
        }

        .dish-card {
            background: var(--white);
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .dish-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 50px rgba(212, 175, 55, 0.3);
        }

        .dish-card img {
            width: 100%;
            height: 280px;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .dish-card:hover img {
            transform: scale(1.1);
        }

        .section-title {
            font-size: 48px;
            font-weight: 700;
            color: var(--dark-brown);
            text-align: center;
            margin-bottom: 16px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--gold);
            margin: 16px auto 0;
            border-radius: 2px;
        }

        .star-rating {
            color: var(--gold);
            font-size: 20px;
        }

        .menu-category {
            background: var(--beige);
            border-radius: 12px;
            padding: 32px;
            margin-bottom: 24px;
        }

        .menu-item {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 20px;
            padding-bottom: 20px;
            border-bottom: 1px solid rgba(62, 39, 35, 0.1);
        }

        .menu-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .ramadan-banner {
            background: linear-gradient(135deg, var(--gold), #C19A2E);
            color: var(--dark-brown);
            padding: 40px;
            border-radius: 16px;
            text-align: center;
            box-shadow: 0 8px 30px rgba(212, 175, 55, 0.3);
        }

        .mobile-menu {
            display: none;
            position: fixed;
            top: 80px;
            left: 0;
            right: 0;
            background: rgba(62, 39, 35, 0.98);
            backdrop-filter: blur(10px);
            padding: 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }

        .mobile-menu.active {
            display: block;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 4px;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: var(--white);
            border-radius: 2px;
            transition: all 0.3s ease;
        }

        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            .desktop-menu {
                display: none;
            }

            .section-title {
                font-size: 32px;
            }

            .hero-bg {
                background-attachment: scroll;
            }
        }

        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        input, textarea, select {
            width: 100%;
            padding: 14px;
            border: 2px solid rgba(62, 39, 35, 0.2);
            border-radius: 8px;
            font-family: 'Poppins', sans-serif;
            font-size: 16px;
            transition: border-color 0.3s ease;
        }

        input:focus, textarea:focus, select:focus {
            outline: none;
            border-color: var(--gold);
        }

        .trust-badge {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            padding: 12px 24px;
            border-radius: 50px;
            display: inline-block;
            color: var(--white);
            font-weight: 600;
        }

        .service-icon {
            font-size: 48px;
            margin-bottom: 16px;
        }

        .kuse-branding {
            display: flex;
            align-items: center;
            gap: 8px;
            justify-content: center;
            margin-top: 24px;
            font-size: 14px;
            color: rgba(62, 39, 35, 0.6);
            transition: color 0.3s ease;
            cursor: pointer;
            text-decoration: none;
        }

        .kuse-branding:hover {
            color: var(--gold);
        }

        .kuse-branding svg {
            height: 1.2em;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="nav-sticky">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center">
                    <h1 class="text-3xl font-bold text-white" style="font-family: 'Playfair Display', serif; color: var(--gold);">GAZANIA</h1>
                </div>
                
                <div class="desktop-menu hidden md:flex items-center gap-8">
                    <a href="#home" class="text-white hover:text-[#D4AF37] transition-colors font-medium">Home</a>
                    <a href="#menu" class="text-white hover:text-[#D4AF37] transition-colors font-medium">Menu</a>
                    <a href="#reviews" class="text-white hover:text-[#D4AF37] transition-colors font-medium">Reviews</a>
                    <a href="#about" class="text-white hover:text-[#D4AF37] transition-colors font-medium">About</a>
                    <a href="#contact" class="text-white hover:text-[#D4AF37] transition-colors font-medium">Contact</a>
                    <a href="https://wa.me/971502152515" class="btn-primary text-sm">Order Now</a>
                    <a href="#reservation" class="btn-secondary text-sm">Reserve Table</a>
                </div>

                <div class="hamburger md:hidden" onclick="toggleMobileMenu()">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
        </div>

        <div class="mobile-menu" id="mobileMenu">
            <div class="flex flex-col gap-4">
                <a href="#home" class="text-white hover:text-[#D4AF37] transition-colors font-medium py-2" onclick="toggleMobileMenu()">Home</a>
                <a href="#menu" class="text-white hover:text-[#D4AF37] transition-colors font-medium py-2" onclick="toggleMobileMenu()">Menu</a>
                <a href="#reviews" class="text-white hover:text-[#D4AF37] transition-colors font-medium py-2" onclick="toggleMobileMenu()">Reviews</a>
                <a href="#about" class="text-white hover:text-[#D4AF37] transition-colors font-medium py-2" onclick="toggleMobileMenu()">About</a>
                <a href="#contact" class="text-white hover:text-[#D4AF37] transition-colors font-medium py-2" onclick="toggleMobileMenu()">Contact</a>
                <a href="https://wa.me/971502152515" class="btn-primary text-center mt-2">Order Now</a>
                <a href="#reservation" class="btn-secondary text-center" onclick="toggleMobileMenu()">Reserve Table</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-bg flex items-center justify-center text-white">
        <div class="max-w-4xl mx-auto px-4 text-center">
            <div class="trust-badge mb-6">⭐ 4.8 Rating • 295+ Reviews</div>
            <h2 class="text-5xl md:text-7xl font-bold mb-6" style="font-family: 'Playfair Display', serif;">Authentic Flavors.<br>Unforgettable Experience.</h2>
            <p class="text-xl md:text-2xl mb-10 text-gray-200">Experience the finest Middle Eastern cuisine in Al Warqa, Dubai</p>
            <div class="flex flex-wrap gap-4 justify-center">
                <a href="https://wa.me/971502152515" class="btn-primary">Order Now</a>
                <a href="#menu" class="btn-secondary">View Menu</a>
                <a href="#reservation" class="btn-secondary">Reserve a Table</a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div class="card text-center fade-in">
                    <div class="service-icon">🍽️</div>
                    <h3 class="text-2xl font-bold mb-3" style="color: var(--dark-brown);">Dine-in</h3>
                    <p class="text-gray-600">Enjoy our cozy ambiance</p>
                </div>
                <div class="card text-center fade-in">
                    <div class="service-icon">🚗</div>
                    <h3 class="text-2xl font-bold mb-3" style="color: var(--dark-brown);">Drive-through</h3>
                    <p class="text-gray-600">Quick & convenient</p>
                </div>
                <div class="card text-center fade-in">
                    <div class="service-icon">🛵</div>
                    <h3 class="text-2xl font-bold mb-3" style="color: var(--dark-brown);">No-contact Delivery</h3>
                    <p class="text-gray-600">Safe delivery to your door</p>
                </div>
                <div class="card text-center fade-in">
                    <div class="service-icon">📦</div>
                    <h3 class="text-2xl font-bold mb-3" style="color: var(--dark-brown);">Takeaway</h3>
                    <p class="text-gray-600">Fresh food on the go</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Dishes Section -->
    <section class="py-20" style="background: var(--beige);">
        <div class="max-w-7xl mx-auto px-4">
            <h2 class="section-title fade-in">Our Signature Dishes</h2>
            <p class="text-center text-gray-600 mb-12 text-lg max-w-2xl mx-auto fade-in">Discover our most loved dishes, crafted with passion and authentic flavors</p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="dish-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://api.kuse.ai/api/folder/v1/file/8751b4f2891e5e747247d0771cf41e6531b563a45406ce7906db5160807f8fc0_2759560.jpeg" alt="Dynamite Chicken Pizza">
                    </div>
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-3" style="color: var(--dark-brown);">Dynamite Chicken Pizza</h3>
                        <p class="text-gray-600 mb-4">Spicy, crispy, and absolutely irresistible</p>
                        <a href="https://wa.me/971502152515?text=I'd like to order Dynamite Chicken Pizza" class="text-[#D4AF37] font-semibold hover:underline">Order Now →</a>
                    </div>
                </div>

                <div class="dish-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://api.kuse.ai/api/folder/v1/file/8675c5adb992997ae96d65bd70a58d76d43aa1e8ad23c92457a451ff4488b82e_2759538.jpeg" alt="Charcoal Chicken">
                    </div>
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-3" style="color: var(--dark-brown);">Charcoal Chicken</h3>
                        <p class="text-gray-600 mb-4">Tender, juicy, grilled to perfection</p>
                        <a href="https://wa.me/971502152515?text=I'd like to order Charcoal Chicken" class="text-[#D4AF37] font-semibold hover:underline">Order Now →</a>
                    </div>
                </div>

                <div class="dish-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://api.kuse.ai/api/folder/v1/file/12f150274fe688e75b46b9789bb8cac629c72e515fd2333e784c513889079633_2759552.jpeg" alt="Iranian Shawarma">
                    </div>
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-3" style="color: var(--dark-brown);">Iranian Shawarma</h3>
                        <p class="text-gray-600 mb-4">Authentic flavors wrapped with love</p>
                        <a href="https://wa.me/971502152515?text=I'd like to order Iranian Shawarma" class="text-[#D4AF37] font-semibold hover:underline">Order Now →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Ramadan Special Banner -->
    <section class="py-16 bg-white">
        <div class="max-w-5xl mx-auto px-4">
            <div class="ramadan-banner fade-in">
                <h3 class="text-4xl font-bold mb-4" style="font-family: 'Playfair Display', serif;">🌙 Ramadan Special: Luqaimat</h3>
                <p class="text-xl mb-6">Traditional Sweet Delight - Available for a Limited Time!</p>
                <a href="https://wa.me/971502152515?text=I'd like to order Luqaimat" class="btn-secondary" style="border-color: var(--dark-brown); color: var(--dark-brown);">Order Now</a>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="py-20" style="background: var(--beige);">
        <div class="max-w-7xl mx-auto px-4">
            <h2 class="section-title fade-in">Our Menu</h2>
            <p class="text-center text-gray-600 mb-12 text-lg max-w-2xl mx-auto fade-in">Explore our diverse selection of authentic Middle Eastern dishes</p>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                <!-- Starters -->
                <div class="menu-category fade-in">
                    <h3 class="text-3xl font-bold mb-6" style="color: var(--dark-brown); font-family: 'Playfair Display', serif;">🥗 Starters</h3>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Crispy Calamari</h4>
                            <p class="text-sm text-gray-600">Golden fried squid rings with tangy sauce</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 32</span>
                    </div>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Chicken Wings</h4>
                            <p class="text-sm text-gray-600">Spicy marinated wings, perfectly grilled</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 28</span>
                    </div>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Lentil Soup</h4>
                            <p class="text-sm text-gray-600">Traditional warm soup with aromatic spices</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 18</span>
                    </div>
                </div>

                <!-- Salads -->
                <div class="menu-category fade-in">
                    <h3 class="text-3xl font-bold mb-6" style="color: var(--dark-brown); font-family: 'Playfair Display', serif;">🥬 Salads</h3>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Mediterranean Salad</h4>
                            <p class="text-sm text-gray-600">Fresh vegetables with feta and olives</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 25</span>
                    </div>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Caesar Salad</h4>
                            <p class="text-sm text-gray-600">Crisp romaine with creamy Caesar dressing</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 28</span>
                    </div>
                </div>

                <!-- Main Courses -->
                <div class="menu-category fade-in">
                    <h3 class="text-3xl font-bold mb-6" style="color: var(--dark-brown); font-family: 'Playfair Display', serif;">🍛 Main Courses</h3>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Madghout Mutton (2 Pax)</h4>
                            <p class="text-sm text-gray-600">Slow-cooked tender mutton with aromatic rice</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 95</span>
                    </div>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Grilled Lamb</h4>
                            <p class="text-sm text-gray-600">Succulent lamb chops with herbs</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 78</span>
                    </div>
                </div>

                <!-- Grills & BBQ -->
                <div class="menu-category fade-in">
                    <h3 class="text-3xl font-bold mb-6" style="color: var(--dark-brown); font-family: 'Playfair Display', serif;">🔥 Grills & BBQ</h3>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Mixed Grill</h4>
                            <p class="text-sm text-gray-600">Assorted grilled meats platter</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 85</span>
                    </div>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Beef Kebab</h4>
                            <p class="text-sm text-gray-600">Juicy beef skewers with spices</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 42</span>
                    </div>
                </div>

                <!-- Burgers & Sandwiches -->
                <div class="menu-category fade-in">
                    <h3 class="text-3xl font-bold mb-6" style="color: var(--dark-brown); font-family: 'Playfair Display', serif;">🍔 Burgers & Sandwiches</h3>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Chicken Caesar Burger</h4>
                            <p class="text-sm text-gray-600">Grilled chicken with Caesar sauce</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 35</span>
                    </div>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Iraqi Bread Chicken Shawarma</h4>
                            <p class="text-sm text-gray-600">Traditional shawarma in fresh Iraqi bread</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 28</span>
                    </div>
                </div>

                <!-- Beverages -->
                <div class="menu-category fade-in">
                    <h3 class="text-3xl font-bold mb-6" style="color: var(--dark-brown); font-family: 'Playfair Display', serif;">🥤 Beverages</h3>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Fresh Juices</h4>
                            <p class="text-sm text-gray-600">Orange, Mango, Lemon Mint</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 15</span>
                    </div>
                    <div class="menu-item">
                        <div>
                            <h4 class="font-semibold text-lg mb-1">Soft Drinks</h4>
                            <p class="text-sm text-gray-600">Coca-Cola, Sprite, Fanta</p>
                        </div>
                        <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 8</span>
                    </div>
                </div>

                <!-- Desserts -->
                <div class="menu-category fade-in lg:col-span-2">
                    <h3 class="text-3xl font-bold mb-6" style="color: var(--dark-brown); font-family: 'Playfair Display', serif;">🍰 Desserts</h3>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div class="menu-item">
                            <div>
                                <h4 class="font-semibold text-lg mb-1">Kunafa</h4>
                                <p class="text-sm text-gray-600">Sweet cheese pastry with syrup</p>
                            </div>
                            <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 22</span>
                        </div>
                        <div class="menu-item">
                            <div>
                                <h4 class="font-semibold text-lg mb-1">Baklava</h4>
                                <p class="text-sm text-gray-600">Layered filo pastry with nuts and honey</p>
                            </div>
                            <span class="font-bold text-[#D4AF37] text-lg whitespace-nowrap ml-4">AED 18</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="text-center mt-12 fade-in">
                <a href="https://wa.me/971502152515?text=Can I see the full menu?" class="btn-primary">View Full Menu</a>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section id="reviews" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4">
            <h2 class="section-title fade-in">What Our Customers Say</h2>
            <div class="text-center mb-12 fade-in">
                <div class="text-5xl font-bold mb-2" style="color: var(--gold);">4.8</div>
                <div class="star-rating mb-2">★★★★★</div>
                <p class="text-gray-600">Based on 295+ reviews</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="card fade-in">
                    <div class="star-rating mb-4">★★★★★</div>
                    <p class="text-gray-700 mb-4 italic">"Food quality is top notch… meat was tender and juicy."</p>
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-full bg-[#D4AF37] flex items-center justify-center text-white font-bold text-xl">A</div>
                        <div>
                            <h4 class="font-semibold">Ahmed K.</h4>
                            <p class="text-sm text-gray-500">Regular Customer</p>
                        </div>
                    </div>
                </div>

                <div class="card fade-in">
                    <div class="star-rating mb-4">★★★★★</div>
                    <p class="text-gray-700 mb-4 italic">"Perfect Iftar experience with amazing service."</p>
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-full bg-[#D4AF37] flex items-center justify-center text-white font-bold text-xl">F</div>
                        <div>
                            <h4 class="font-semibold">Fatima S.</h4>
                            <p class="text-sm text-gray-500">Food Enthusiast</p>
                        </div>
                    </div>
                </div>

                <div class="card fade-in">
                    <div class="star-rating mb-4">★★★★★</div>
                    <p class="text-gray-700 mb-4 italic">"Iranian shawarma is a must-try!"</p>
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-full bg-[#D4AF37] flex items-center justify-center text-white font-bold text-xl">M</div>
                        <div>
                            <h4 class="font-semibold">Mohammed R.</h4>
                            <p class="text-sm text-gray-500">Local Resident</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20" style="background: var(--beige);">
        <div class="max-w-7xl mx-auto px-4">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="fade-in">
                    <h2 class="section-title text-left">About Gazania Restaurant</h2>
                    <p class="text-lg text-gray-700 mb-6 leading-relaxed">At Gazania Restaurant, we bring you the finest Middle Eastern cuisine with authentic flavors and quality ingredients. Located in the heart of Al Warqa, Dubai, we specialize in grilled meats, traditional shawarma, and signature dishes that keep our customers coming back.</p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                        <div>
                            <div class="text-4xl mb-2">🥇</div>
                            <h4 class="font-bold mb-1">Quality Ingredients</h4>
                            <p class="text-sm text-gray-600">Only the freshest, finest ingredients</p>
                        </div>
                        <div>
                            <div class="text-4xl mb-2">🌟</div>
                            <h4 class="font-bold mb-1">Authentic Flavors</h4>
                            <p class="text-sm text-gray-600">Traditional recipes passed down</p>
                        </div>
                        <div>
                            <div class="text-4xl mb-2">❤️</div>
                            <h4 class="font-bold mb-1">Customer Experience</h4>
                            <p class="text-sm text-gray-600">Service with a smile</p>
                        </div>
                    </div>

                    <div class="bg-white p-6 rounded-lg border-l-4 border-[#D4AF37]">
                        <h4 class="font-bold text-xl mb-3">Our Specialties</h4>
                        <ul class="space-y-2">
                            <li class="flex items-center gap-2">
                                <span class="text-[#D4AF37]">✓</span>
                                <span>Grilled Meats</span>
                            </li>
                            <li class="flex items-center gap-2">
                                <span class="text-[#D4AF37]">✓</span>
                                <span>Traditional Shawarma</span>
                            </li>
                            <li class="flex items-center gap-2">
                                <span class="text-[#D4AF37]">✓</span>
                                <span>Authentic Middle Eastern Cuisine</span>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="fade-in">
                    <img src="https://api.kuse.ai/api/folder/v1/file/35ca3ab33ce11bfb22af6c747d267ad665234b0186e557cc0f6175968ae5b215_2759491.jpeg" alt="Gazania Restaurant Interior" class="rounded-2xl shadow-2xl w-full h-auto object-cover">
                </div>
            </div>
        </div>
    </section>

    <!-- Reservation Section -->
    <section id="reservation" class="py-20 bg-white">
        <div class="max-w-4xl mx-auto px-4">
            <h2 class="section-title fade-in">Reserve Your Table</h2>
            <p class="text-center text-gray-600 mb-12 text-lg fade-in">Book your table in advance for a seamless dining experience</p>

            <form class="card fade-in" onsubmit="handleReservation(event)">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                    <div>
                        <label class="block mb-2 font-semibold text-gray-700">Name</label>
                        <input type="text" name="name" placeholder="Your Name" required>
                    </div>
                    <div>
                        <label class="block mb-2 font-semibold text-gray-700">Phone</label>
                        <input type="tel" name="phone" placeholder="+971 XX XXX XXXX" required>
                    </div>
                    <div>
                        <label class="block mb-2 font-semibold text-gray-700">Date</label>
                        <input type="date" name="date" required>
                    </div>
                    <div>
                        <label class="block mb-2 font-semibold text-gray-700">Time</label>
                        <input type="time" name="time" required>
                    </div>
                    <div class="md:col-span-2">
                        <label class="block mb-2 font-semibold text-gray-700">Number of Guests</label>
                        <select name="guests" required>
                            <option value="">Select number of guests</option>
                            <option value="1">1 Guest</option>
                            <option value="2">2 Guests</option>
                            <option value="3">3 Guests</option>
                            <option value="4">4 Guests</option>
                            <option value="5">5 Guests</option>
                            <option value="6">6+ Guests</option>
                        </select>
                    </div>
                </div>

                <button type="submit" class="btn-primary w-full text-center">Reserve Table</button>
                
                <div class="text-center mt-6">
                    <p class="text-gray-600 mb-3">Or reserve via WhatsApp</p>
                    <a href="https://wa.me/971502152515?text=I'd like to reserve a table" class="btn-secondary">WhatsApp Reservation</a>
                </div>
            </form>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20" style="background: var(--beige);">
        <div class="max-w-7xl mx-auto px-4">
            <h2 class="section-title fade-in">Get In Touch</h2>
            <p class="text-center text-gray-600 mb-12 text-lg fade-in">Visit us or get in touch for any inquiries</p>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div class="fade-in">
                    <div class="card mb-6">
                        <h3 class="text-2xl font-bold mb-6" style="color: var(--dark-brown);">Contact Information</h3>
                        
                        <div class="space-y-6">
                            <div class="flex items-start gap-4">
                                <div class="text-3xl">📍</div>
                                <div>
                                    <h4 class="font-semibold text-lg mb-1">Address</h4>
                                    <p class="text-gray-600">Al Warqa 1, Dubai, UAE<br>(Located in MALZAM 2)</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-4">
                                <div class="text-3xl">📞</div>
                                <div>
                                    <h4 class="font-semibold text-lg mb-1">Phone</h4>
                                    <a href="tel:+971502152515" class="text-[#D4AF37] hover:underline">050 215 2515</a>
                                </div>
                            </div>

                            <div class="flex items-start gap-4">
                                <div class="text-3xl">🌐</div>
                                <div>
                                    <h4 class="font-semibold text-lg mb-1">Website</h4>
                                    <a href="https://gazaniaresturant.com" target="_blank" class="text-[#D4AF37] hover:underline">gazaniaresturant.com</a>
                                </div>
                            </div>

                            <div class="flex items-start gap-4">
                                <div class="text-3xl">⏰</div>
                                <div>
                                    <h4 class="font-semibold text-lg mb-1">Operating Hours</h4>
                                    <p class="text-gray-600">Open Daily until 12 AM</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="flex flex-wrap gap-4">
                        <a href="tel:+971502152515" class="btn-primary flex-1 text-center">Call Now</a>
                        <a href="https://wa.me/971502152515" class="btn-primary flex-1 text-center">WhatsApp</a>
                        <a href="https://maps.google.com/?q=Al+Warqa+1+Dubai+UAE" target="_blank" class="btn-secondary flex-1 text-center" style="border-color: var(--dark-brown); color: var(--dark-brown);">Get Directions</a>
                    </div>
                </div>

                <div class="fade-in">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3608.6847219!2d55.4!3d25.2!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjXCsDEyJzAwLjAiTiA1NcKwMjQnMDAuMCJF!5e0!3m2!1sen!2sae!4v1234567890" width="100%" height="450" style="border:0; border-radius: 16px;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-[#3E2723] text-white py-12">
        <div class="max-w-7xl mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <h3 class="text-3xl font-bold mb-4" style="font-family: 'Playfair Display', serif; color: var(--gold);">GAZANIA</h3>
                    <p class="text-gray-300 mb-4">Authentic Middle Eastern cuisine in the heart of Al Warqa, Dubai.</p>
                    <div class="flex gap-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-[#D4AF37] flex items-center justify-center hover:bg-[#C19A2E] transition-colors">
                            <span class="text-[#3E2723] font-bold">f</span>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-[#D4AF37] flex items-center justify-center hover:bg-[#C19A2E] transition-colors">
                            <span class="text-[#3E2723] font-bold">📷</span>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-[#D4AF37] flex items-center justify-center hover:bg-[#C19A2E] transition-colors">
                            <span class="text-[#3E2723] font-bold">𝕏</span>
                        </a>
                    </div>
                </div>

                <div>
                    <h4 class="font-bold text-lg mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#menu" class="text-gray-300 hover:text-[#D4AF37] transition-colors">Menu</a></li>
                        <li><a href="#about" class="text-gray-300 hover:text-[#D4AF37] transition-colors">About</a></li>
                        <li><a href="#reviews" class="text-gray-300 hover:text-[#D4AF37] transition-colors">Reviews</a></li>
                        <li><a href="#contact" class="text-gray-300 hover:text-[#D4AF37] transition-colors">Contact</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="font-bold text-lg mb-4">Contact</h4>
                    <ul class="space-y-2 text-gray-300">
                        <li>📍 Al Warqa 1, Dubai, UAE</li>
                        <li>📞 <a href="tel:+971502152515" class="hover:text-[#D4AF37]">050 215 2515</a></li>
                        <li>🌐 <a href="https://gazaniaresturant.com" class="hover:text-[#D4AF37]">gazaniaresturant.com</a></li>
                        <li>⏰ Open Daily until 12 AM</li>
                    </ul>
                </div>

                <div>
                    <h4 class="font-bold text-lg mb-4">Location</h4>
                    <p class="text-gray-300 mb-4">Located in MALZAM 2, Al Warqa 1, Dubai</p>
                    <a href="https://maps.google.com/?q=Al+Warqa+1+Dubai+UAE" target="_blank" class="text-[#D4AF37] hover:underline">Get Directions →</a>
                </div>
            </div>

            <div class="border-t border-gray-700 pt-8 text-center">
                <p class="text-gray-400 mb-2">© 2024 Gazania Restaurant LLC. All rights reserved.</p>
                <a href="https://kuse.ai" target="_blank" class="kuse-branding">
                    <span>made with</span>
                    <svg viewBox="0,0,160,44" xmlns="http://www.w3.org/2000/svg"><path d="m.01,20.65C-.43,8.25,9.3-2.03,22.04.34,34.78,2.72,43.29,8.32,43.29,22.9s-8.66,19.01-22.03,20.3C7.9,44.5.46,33.05.01,20.65z" fill="currentColor"/><path fill-rule="evenodd" clip-rule="evenodd" d="m146.76,7.94c8.07,0,13.24,6.15,13.24,14.58v1.39h-20.75c.45,4.05,3.51,7.37,8.57,7.37,2.62,0,5.73-1.05,7.62-2.94l2.67,3.83c-2.67,2.55-6.62,3.88-10.9,3.88-8.07,0-14.08-5.6-14.08-14.08,0-7.76,5.67-14.02,13.63-14.02zm0,4.77c-5.01,0-7.29,3.83-7.57,7.1h15.13c-.11-3.16-2.28-7.1-7.57-7.1z" fill="currentColor"/><path d="m86.64,24.49c0,4.15,2.39,6.84,6.84,6.84,4.4,0,6.84-2.69,6.84-6.84V8.55h5.37v16.33c0,6.7-4.06,11.14-12.21,11.14-8.21,0-12.21-4.5-12.21-11.09V8.55h5.37v15.94zm32.99-16.55c4.49,0,8.06,1.47,10.6,3.86l-2.59,3.81c-2.05-2-5.28-3.08-8.06-3.08-2.88,0-4.84,1.37-4.84,3.32,0,1.91,2.64,2.54,5.81,3.27,4.59,1.08,10.26,2.4,10.26,8.46,0,4.94-3.76,8.41-11.14,8.41-4.98,0-8.94-1.76-11.24-4.11l2.54-4.11c1.86,1.91,5.18,3.67,8.84,3.67,3.91,0,5.57-1.66,5.57-3.62,0-2.3-2.88-2.98-6.21-3.76-4.54-1.08-9.87-2.3-9.87-8.06,0-4.5,4.2-8.06,10.31-8.06zM60.79,20.82,71.44,8.55h6.5L66.46,21.26,78.82,35.44h-6.5l-9.28-11.1-2.25,2.49v8.6h-5.33V8.55h5.33v12.27z" fill="currentColor"/></svg>
                </a>
            </div>
        </div>
    </footer>

    <script>
        function toggleMobileMenu() {
            const menu = document.getElementById(`mobileMenu`);
            menu.classList.toggle(`active`);
        }

        function handleReservation(event) {
            event.preventDefault();
            const formData = new FormData(event.target);
            const name = formData.get(`name`);
            const phone = formData.get(`phone`);
            const date = formData.get(`date`);
            const time = formData.get(`time`);
            const guests = formData.get(`guests`);
            
            const message = `I'd like to reserve a table:\nName: ${name}\nPhone: ${phone}\nDate: ${date}\nTime: ${time}\nGuests: ${guests}`;
            const whatsappUrl = `https://wa.me/971502152515?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, `_blank`);
        }

        const observerOptions = {
            threshold: 0.1,
            rootMargin: `0px 0px -50px 0px`
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add(`visible`);
                }
            });
        }, observerOptions);

        document.addEventListener(`DOMContentLoaded`, () => {
            const fadeElements = document.querySelectorAll(`.fade-in`);
            fadeElements.forEach(el => observer.observe(el));
        });

        document.querySelectorAll(`a[href^="#"]`).forEach(anchor => {
            anchor.addEventListener(`click`, function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute(`href`));
                if (target) {
                    const offset = 80;
                    const targetPosition = target.offsetTop - offset;
                    window.scrollTo({
                        top: targetPosition,
                        behavior: `smooth`
                    });
                }
            });
        });
    </script>

    <script src="https://cdn.kuse.ai/sdk.prd.js"></script>
</body>
</html>
