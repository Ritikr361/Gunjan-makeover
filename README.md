<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gunjan Makeover | Portfolio</title>

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>

    <!-- Google Fonts: Playfair Display, Lora, Dancing Script -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800;900&family=Lora:wght@400;500;600&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">

    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <!-- Animate On Scroll Library -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

    <style>
        /* Custom Styles for a more professional look */
        :root {
            --gold: #D4AF37;
            --gold-dark: #b89b3c;
            --dark-bg: #0a0a0a;
            --light-dark-bg: #111111;
            --text-light: #e0e0e0;
            --text-dark: #1a1a1a;
        }

        body {
            background-color: var(--dark-bg);
            color: var(--text-light);
            font-family: 'Lora', serif;
            padding-top: 80px; /* Add padding to body to avoid content being hidden by fixed navbar */
        }
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Playfair Display', serif;
        }
        .gold-text {
            color: var(--gold);
        }
        .gold-bg {
            background: linear-gradient(145deg, #e7c35c, #D4AF37);
            transition: all 0.3s ease;
            color: var(--text-dark);
        }
        .gold-bg:hover {
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.4);
            transform: translateY(-2px);
        }
        
        /* --- New Hero Section --- */
        #home {
            position: relative;
            overflow: hidden; /* Contain the pseudo-element */
        }
        #home::before {
            content: '';
            position: absolute;
            top: -5%; left: -5%;
            width: 110%; height: 110%;
            background-image: url('https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753046724/hj6qmgmhj3e41ferewvv.jpg');
            background-size: cover;
            background-position: center;
            animation: kenburns 20s ease-out infinite;
            filter: blur(4px); /* Blur effect */
            z-index: 1;
        }
        .hero-overlay {
            background-color: rgba(0, 0, 0, 0.6);
            position: absolute;
            top: 0; left: 0;
            width: 100%; height: 100%;
            z-index: 2;
        }
        #home .hero-content {
            position: relative;
            z-index: 3;
        }

        /* Golden Glow Effect for Hero Title */
        .hero-title-glow {
             text-shadow: 0 0 8px rgba(212, 175, 55, 0.6), 
                         0 0 20px rgba(212, 175, 55, 0.4), 
                         0 0 40px rgba(212, 175, 55, 0.2);
        }

        @keyframes kenburns {
            0% {
                transform: scale(1) translate(0, 0);
            }
            50% {
                transform: scale(1.1) translate(-2%, 2%);
            }
            100% {
                transform: scale(1) translate(0, 0);
            }
        }

        /* --- Navbar Styling --- */
        #navbar {
            background-color: var(--light-dark-bg);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }
        
        /* Glow effect for nav links */
        #navbar .nav-links a {
            transition: color 0.3s ease, text-shadow 0.3s ease;
        }
        #navbar .nav-links a:hover {
            color: var(--gold);
            text-shadow: 0 0 12px rgba(212, 175, 55, 0.7);
        }

        /* Section Title Styling */
        .section-title {
            font-size: 3rem;
            font-weight: 800;
        }
        .section-subtitle {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            margin-top: -1rem;
        }

        /* Portfolio Hover Effect */
        .portfolio-item .overlay {
            opacity: 0;
            transition: opacity 0.4s ease;
            background: linear-gradient(to top, rgba(0,0,0,0.9), transparent);
        }
        .portfolio-item:hover .overlay {
            opacity: 1;
        }
        .portfolio-item img {
            transition: transform 0.4s ease;
        }
        .portfolio-item:hover img {
            transform: scale(1.05);
        }

        /* --- Testimonial Scroller --- */
        .testimonial-scroller-container {
            -webkit-mask-image: linear-gradient(to right, transparent, black 20%, black 80%, transparent);
            mask-image: linear-gradient(to right, transparent, black 20%, black 80%, transparent);
        }
        .testimonial-scroller {
            animation: scroll 45s linear infinite;
        }
        .testimonial-scroller-container:hover .testimonial-scroller {
            animation-play-state: paused;
        }
        @keyframes scroll {
            from { transform: translateX(0); }
            to { transform: translateX(-50%); }
        }

        .testimonial-card {
            background-color: var(--light-dark-bg);
            border: 1px solid rgba(212, 175, 55, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            flex-shrink: 0;
            width: 350px;
        }
        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.1);
        }

        /* Form Input Styling */
        .form-input {
            background-color: #1f1f1f;
            border: 1px solid #333;
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }
        .form-input:focus {
            outline: none;
            border-color: var(--gold);
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.3);
        }
    </style>
</head>
<body>

    <!-- Header & Navigation Bar -->
    <header id="navbar" class="fixed top-0 left-0 right-0 z-50">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#home" class="text-3xl font-bold gold-text" style="font-family: 'Dancing Script', cursive;">Gunjan Makeover</a>
            <nav class="hidden md:flex space-x-8 items-center nav-links">
                <a href="#home" class="text-white hover:gold-text">Home</a>
                <a href="#about" class="text-white hover:gold-text">About</a>
                <a href="#portfolio" class="text-white hover:gold-text">Portfolio</a>
                <a href="#testimonials" class="text-white hover:gold-text">Testimonials</a>
                <a href="#contact" class="text-white hover:gold-text">Contact</a>
            </nav>
            <button id="mobile-menu-button" class="md:hidden text-white text-2xl">
                <i class="fas fa-bars"></i>
            </button>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-black bg-opacity-90">
            <a href="#home" class="block text-center text-white py-3 hover:bg-gray-800">Home</a>
            <a href="#about" class="block text-center text-white py-3 hover:bg-gray-800">About</a>
            <a href="#portfolio" class="block text-center text-white py-3 hover:bg-gray-800">Portfolio</a>
            <a href="#testimonials" class="block text-center text-white py-3 hover:bg-gray-800">Testimonials</a>
            <a href="#contact" class="block text-center text-white py-3 hover:bg-gray-800">Contact</a>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="home" class="h-screen flex items-center justify-center text-center text-white -mt-[80px]">
            <div class="hero-overlay"></div>
            <div class="hero-content" data-aos="fade-in" data-aos-delay="300">
                <h1 class="text-6xl md:text-8xl font-black uppercase tracking-wider hero-title-glow">Gunjan Makeover</h1>
                <p class="text-xl md:text-2xl mt-4 max-w-3xl mx-auto" style="font-family: 'Lora', serif;">Transforming Beauty with 4+ Years of Professional Makeup Artistry</p>
                <a href="#portfolio" class="inline-block mt-8 px-10 py-4 font-bold text-lg rounded-md gold-bg text-gray-900 uppercase tracking-widest">View My Work</a>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="py-20 md:py-32 bg-light-dark-bg">
            <div class="container mx-auto px-6">
                <div class="grid md:grid-cols-5 gap-16 items-center">
                    <!-- Image Column -->
                    <div class="md:col-span-2 flex justify-center" data-aos="fade-right">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753044306/pgnpez06d3f50znhffak.jpg" alt="Gunjan Makeover" class="rounded-lg shadow-2xl w-full h-full object-cover" style="max-height: 75vh;">
                    </div>
                    <!-- Text Column -->
                    <div class="md:col-span-3" data-aos="fade-left" data-aos-delay="200">
                        <h2 class="section-title">About Me</h2>
                        <p class="section-subtitle gold-text">Crafting Your Perfect Look</p>
                        <p class="mt-6 text-lg leading-relaxed">
                            With over 4 years of experience, I create a special and excellent look for every client. My goal is not just to apply makeup, but to highlight your natural beauty.
                        </p>
                        <p class="mt-4 text-lg leading-relaxed">
                           From bridal makeup to fashion shoots and special events, I specialize in creating the perfect look for every occasion. Let's create a memorable look for your next event.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Portfolio Section -->
        <section id="portfolio" class="py-20 md:py-32">
            <div class="container mx-auto px-6 text-center">
                <h2 class="section-title" data-aos="fade-up">Portfolio</h2>
                <p class="section-subtitle gold-text" data-aos="fade-up" data-aos-delay="100">A Glimpse of My Art</p>
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mt-12">
                    <!-- Portfolio Item 1 -->
                    <div class="portfolio-item relative rounded-lg overflow-hidden shadow-lg" data-aos="zoom-in-up">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753045528/nyl2blkkykq1jindrafc.jpg" alt="Elegant Makeup Look" class="w-full h-full object-cover">
                        <div class="overlay absolute inset-0 flex items-end p-6">
                            <div>
                                <h3 class="text-2xl font-bold text-white">Subtle Glam</h3>
                                <p class="text-gray-300">Perfect for any occasion.</p>
                            </div>
                        </div>
                    </div>
                    <!-- Portfolio Item 2 -->
                    <div class="portfolio-item relative rounded-lg overflow-hidden shadow-lg" data-aos="zoom-in-up" data-aos-delay="150">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753045553/b81ptaqupkrtcinarhrx.jpg" alt="Bridal Makeup" class="w-full h-full object-cover">
                        <div class="overlay absolute inset-0 flex items-end p-6">
                            <div>
                                <h3 class="text-2xl font-bold text-white">Bridal Beauty</h3>
                                <p class="text-gray-300">Radiant and timeless.</p>
                            </div>
                        </div>
                    </div>
                    <!-- Portfolio Item 3 -->
                    <div class="portfolio-item relative rounded-lg overflow-hidden shadow-lg" data-aos="zoom-in-up" data-aos-delay="300">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753045576/bd0e9fmzrbflj9c1ddzh.jpg" alt="Vibrant Makeup" class="w-full h-full object-cover">
                        <div class="overlay absolute inset-0 flex items-end p-6">
                            <div>
                                <h3 class="text-2xl font-bold text-white">Colorful Creations</h3>
                                <p class="text-gray-300">Bold and artistic.</p>
                            </div>
                        </div>
                    </div>
                     <!-- Portfolio Item 4 -->
                    <div class="portfolio-item relative rounded-lg overflow-hidden shadow-lg" data-aos="zoom-in-up" data-aos-delay="450">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753045675/hjtqpwnkraamgw03haeb.jpg" alt="Classic Makeup Look" class="w-full h-full object-cover">
                        <div class="overlay absolute inset-0 flex items-end p-6">
                            <div>
                                <h3 class="text-2xl font-bold text-white">Classic Elegance</h3>
                                <p class="text-gray-300">A timeless, sophisticated look.</p>
                            </div>
                        </div>
                    </div>
                    <!-- Portfolio Item 5 -->
                    <div class="portfolio-item relative rounded-lg overflow-hidden shadow-lg" data-aos="zoom-in-up" data-aos-delay="600">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753046037/ptekwxc6m8qrpwf6u2qb.jpg" alt="Stunning Eye Makeup" class="w-full h-full object-cover">
                        <div class="overlay absolute inset-0 flex items-end p-6">
                            <div>
                                <h3 class="text-2xl font-bold text-white">Eye Artistry</h3>
                                <p class="text-gray-300">Detailed and captivating.</p>
                            </div>
                        </div>
                    </div>
                    <!-- Portfolio Item 6 -->
                    <div class="portfolio-item relative rounded-lg overflow-hidden shadow-lg" data-aos="zoom-in-up" data-aos-delay="750">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753046096/l9od3ezngdqayy7rfhxf.jpg" alt="Bold and Beautiful Makeup" class="w-full h-full object-cover">
                        <div class="overlay absolute inset-0 flex items-end p-6">
                            <div>
                                <h3 class="text-2xl font-bold text-white">Bold and Beautiful</h3>
                                <p class="text-gray-300">Making a statement.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials Section -->
        <section id="testimonials" class="py-20 md:py-32 bg-light-dark-bg overflow-hidden">
            <div class="container mx-auto px-6 text-center">
                <h2 class="section-title" data-aos="fade-up">Testimonials</h2>
                <p class="section-subtitle gold-text" data-aos="fade-up" data-aos-delay="100">Words From My Clients</p>
            </div>
            <div class="testimonial-scroller-container mt-16" data-aos="fade-in">
                <div class="testimonial-scroller flex gap-8">
                    <!-- Cards are duplicated for seamless scroll -->
                    <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"The makeup Gunjan did for my wedding was amazing. Everyone praised my look. Thank you so much!"</p>
                        <h4 class="mt-6 font-bold text-xl">- Priya S.</h4>
                    </div>
                    <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"Very professional and the work is flawless. My party makeup was exactly as I had imagined. Highly recommended."</p>
                        <h4 class="mt-6 font-bold text-xl">- Anjali V.</h4>
                    </div>
                    <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"Her work for my portfolio shoot was incredible. Every look was perfect. I will definitely work with her again."</p>
                        <h4 class="mt-6 font-bold text-xl">- Simran K.</h4>
                    </div>
                    <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"A true artist. She listened to me carefully and gave me an elegant and natural look. I am very happy."</p>
                        <h4 class="mt-6 font-bold text-xl">- Neha M.</h4>
                    </div>
                    <!-- Duplicates -->
                     <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"The makeup Gunjan did for my wedding was amazing. Everyone praised my look. Thank you so much!"</p>
                        <h4 class="mt-6 font-bold text-xl">- Priya S.</h4>
                    </div>
                    <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"Very professional and the work is flawless. My party makeup was exactly as I had imagined. Highly recommended."</p>
                        <h4 class="mt-6 font-bold text-xl">- Anjali V.</h4>
                    </div>
                    <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"Her work for my portfolio shoot was incredible. Every look was perfect. I will definitely work with her again."</p>
                        <h4 class="mt-6 font-bold text-xl">- Simran K.</h4>
                    </div>
                    <div class="testimonial-card p-8 rounded-lg">
                        <i class="fas fa-quote-left text-4xl gold-text opacity-50"></i>
                        <p class="mt-4 text-lg">"A true artist. She listened to me carefully and gave me an elegant and natural look. I am very happy."</p>
                        <h4 class="mt-6 font-bold text-xl">- Neha M.</h4>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="py-20 md:py-32">
            <div class="container mx-auto px-6 text-center">
                 <h2 class="section-title" data-aos="fade-up">Get In Touch</h2>
                <p class="section-subtitle gold-text" data-aos-fade-up" data-aos-delay="100">Let's Create Something Beautiful</p>
                <form class="max-w-2xl mx-auto mt-12 text-left" data-aos="fade-up" data-aos-delay="200" onsubmit="return false;">
                    <div class="mb-6">
                        <label for="name" class="block mb-2 text-lg text-gray-400">Name</label>
                        <input type="text" id="name" class="form-input w-full p-4 rounded-md text-white" placeholder="Your Name">
                    </div>
                    <div class="mb-6">
                        <label for="email" class="block mb-2 text-lg text-gray-400">Email</label>
                        <input type="email" id="email" class="form-input w-full p-4 rounded-md text-white" placeholder="your.email@example.com">
                    </div>
                    <div class="mb-6">
                        <label for="message" class="block mb-2 text-lg text-gray-400">Message</label>
                        <textarea id="message" rows="6" class="form-input w-full p-4 rounded-md text-white" placeholder="Tell me about your event..."></textarea>
                    </div>
                    <p id="validation-msg" class="text-red-500 text-center mt-2"></p>
                    <div class="text-center">
                        <button type="button" id="send-whatsapp-btn" class="inline-block mt-4 px-12 py-4 font-bold text-lg rounded-md gold-bg text-gray-900 uppercase tracking-widest">Send Message</button>
                    </div>
                </form>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-light-dark-bg py-12">
        <div class="container mx-auto px-6 text-center text-gray-400">
            <div class="flex justify-center space-x-6 mb-6">
                <a href="#" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-twitter"></i></a>
                <a href="#" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-instagram"></i></a>
                <a href="#" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-pinterest"></i></a>
            </div>
            <p>&copy; <span id="year"></span> Gunjan Makeover. All Rights Reserved.</p>
            <p class="text-sm text-gray-600 mt-2">Designed with Elegance</p>
        </div>
    </footer>

    <!-- Animate On Scroll Library JS -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>

    <script>
        // Initialize Animate on Scroll
        AOS.init({
            duration: 800,
            once: true,
            offset: 50,
        });

        // Mobile Menu Toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // Close mobile menu when a link is clicked
        const mobileMenuLinks = mobileMenu.getElementsByTagName('a');
        for(let link of mobileMenuLinks) {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        }

        // Set current year in footer
        document.getElementById('year').textContent = new Date().getFullYear();

        // WhatsApp redirect logic
        const whatsappBtn = document.getElementById('send-whatsapp-btn');
        const validationMsg = document.getElementById('validation-msg');
        
        whatsappBtn.addEventListener('click', function() {
            validationMsg.textContent = ''; // Clear previous message
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();

            if (!name || !message) {
                validationMsg.textContent = 'Please fill in your name and message.';
                return;
            }

            const fullMessage = `Hello! I got your number from the website.\n\n*Name:* ${name}\n*Email:* ${email}\n*Message:* ${message}`;
            const phoneNumber = '916263136851';
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(fullMessage)}`;
            
            window.open(whatsappUrl, '_blank').focus();
        });
    </script>

</body>
</html>
