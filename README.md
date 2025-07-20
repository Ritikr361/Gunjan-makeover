<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gunjan Makeover - Professional Makeover Artist</title>
    
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
            background-image: url('https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1752959265/nvyfxyfnh3ysyhgh7tun.jpg');
            background-size: cover;
            background-position: center;
            animation: kenburns 20s ease-out infinite;
            filter: blur(4px); /* Blur effect */
            z-index: 1;
        }
        .hero-overlay {
            background-color: rgba(0, 0, 0, 0.5);
            position: absolute;
            top: 0; left: 0;
            width: 100%; height: 100%;
            z-index: 2;
        }
        #home .hero-content {
            position: relative;
            z-index: 3;
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
            background-color: transparent;
            transition: background-color 0.4s ease, backdrop-filter 0.4s ease;
        }
        #navbar.scrolled {
            background-color: rgba(10, 10, 10, 0.8);
            backdrop-filter: blur(10px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        /* Glow effect for nav links */
        #navbar .hidden a {
            transition: color 0.3s ease, text-shadow 0.3s ease;
        }
        #navbar .hidden a.hover\:gold-text:hover {
            text-shadow: 0 0 12px rgba(212, 175, 55, 0.7);
        }

        /* Section Title Styling */
        .section-title {
            font-size: 3rem;
            font-weight: 800;
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
            background-color: var(--dark-bg);
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
<body class="overflow-x-hidden">

    <!-- Header -->
    <header class="fixed top-0 left-0 right-0 z-50" id="navbar">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold gold-text" style="font-family: 'Playfair Display', serif;">GM</a>
            <div class="hidden md:flex space-x-8 items-center">
                <a href="#about" class="hover:gold-text transition-colors">About</a>
                <a href="#portfolio" class="hover:gold-text transition-colors">Portfolio</a>
                <a href="#testimonials" class="hover:gold-text transition-colors">Testimonials</a>
                <a href="#contact" class="hover:gold-text transition-colors">Contact</a>
                <a href="#booking" class="gold-bg text-black font-bold py-2 px-6 rounded-full">Book Now</a>
            </div>
            <div class="md:hidden">
                <button id="mobile-menu-button" class="text-white focus:outline-none">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </nav>
    </header>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="hidden fixed inset-0 bg-black bg-opacity-95 z-50 flex flex-col items-center justify-center space-y-8">
        <button id="close-mobile-menu" class="absolute top-6 right-6 text-white text-3xl">&times;</button>
        <a href="#about" class="text-2xl hover:gold-text transition-colors mobile-link">About</a>
        <a href="#portfolio" class="text-2xl hover:gold-text transition-colors mobile-link">Portfolio</a>
        <a href="#testimonials" class="text-2xl hover:gold-text transition-colors mobile-link">Testimonials</a>
        <a href="#contact" class="text-2xl hover:gold-text transition-colors mobile-link">Contact</a>
        <a href="#booking" class="text-2xl gold-bg text-black font-bold py-3 px-8 rounded-full mobile-link">Book Now</a>
    </div>

    <!-- Hero Section -->
    <section id="home" class="relative h-screen flex items-center justify-center text-center">
        <div class="hero-overlay"></div>
        <div class="hero-content px-4 flex flex-col items-center">
            <h1 class="text-5xl md:text-7xl lg:text-8xl font-extrabold gold-text" data-aos="fade-down" style="font-family: 'Playfair Display', serif;">Gunjan Makeover</h1>
            <p class="mt-4 text-xl md:text-2xl text-gray-200 tracking-wide" data-aos="fade-up" data-aos-delay="200">Because You Deserve to Shine</p>
            <a href="#booking" class="mt-8 inline-block gold-bg text-black font-bold py-3 px-10 rounded-full text-lg" data-aos="fade-up" data-aos-delay="400">Book a Consultation</a>
        </div>
    </section>

    <!-- Main Content -->
    <main>
        <!-- About Section -->
        <section id="about" class="py-20 md:py-32 bg-black">
            <div class="container mx-auto px-6">
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div data-aos="fade-right">
                        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753044306/pgnpez06d3f50znhffak.jpg" alt="Gunjan, the makeup artist" class="rounded-lg shadow-2xl w-full h-auto object-cover aspect-square" onerror="this.onerror=null;this.src='https://placehold.co/600x600/0a0a0a/e0e0e0?text=Artist+Image';">
                    </div>
                    <div data-aos="fade-left">
                        <h2 class="section-title mb-6"><span class="gold-text">About</span> the Artist</h2>
                        <p class="mb-4 text-lg">My name is Gunjan, and I believe makeup is more than just color on a face—it's a form of art, an expression of identity, and a tool for empowerment. With over a decade of experience in bridal, editorial, and celebrity makeup, my passion lies in creating timeless, elegant looks that enhance natural beauty.</p>
                        <p class="mb-6">From the initial consultation to the final touch-up, I provide a bespoke, luxurious experience. I am dedicated to understanding your vision and bringing it to life, ensuring you look and feel absolutely radiant for your most important moments.</p>
                        <a href="#contact" class="font-bold gold-text hover:underline">Get in Touch &rarr;</a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Portfolio Section -->
        <section id="portfolio" class="py-20 md:py-32 bg-light-dark-bg">
            <div class="container mx-auto px-6 text-center">
                <h2 class="section-title mb-12" data-aos="fade-up">My <span class="gold-text">Work</span></h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-7xl mx-auto">
                    <!-- Portfolio items will be dynamically generated here -->
                </div>
            </div>
        </section>

        <!-- Videos Section -->
        <section id="videos" class="py-20 md:py-32 bg-black">
            <div class="container mx-auto px-6 text-center">
                <h2 class="section-title mb-12" data-aos="fade-up">Behind the <span class="gold-text">Scenes</span></h2>
                <div class="flex justify-center" data-aos="zoom-in">
                     <div class="w-full max-w-md"> 
                        <div class="aspect-w-9 aspect-h-16">
                           <iframe class="rounded-lg shadow-xl w-full h-full" src="https://www.youtube.com/embed/FaUlixCRVWw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Testimonials Section -->
        <section id="testimonials" class="py-20 md:py-32 bg-light-dark-bg">
            <div class="container mx-auto px-6 text-center">
                <h2 class="section-title mb-12" data-aos="fade-up">Client <span class="gold-text">Love</span></h2>
                <div class="testimonial-scroller-container overflow-hidden" data-aos="fade-up">
                    <div id="testimonial-scroller" class="flex gap-8">
                        <!-- Testimonials will be dynamically generated here -->
                    </div>
                </div>
            </div>
        </section>

        <!-- Booking Section -->
        <section id="booking" class="py-20 md:py-32 bg-black">
            <div class="container mx-auto px-6">
                <h2 class="section-title text-center mb-12" data-aos="fade-up">Book an <span class="gold-text">Appointment</span></h2>
                <div class="grid lg:grid-cols-2 gap-12">
                    <div data-aos="fade-right">
                        <div class="bg-light-dark-bg p-6 md:p-8 rounded-lg shadow-2xl">
                            <div class="flex justify-between items-center mb-6">
                                <button id="prev-month" class="p-2 rounded-full hover:bg-gray-700"><i class="fas fa-angle-left"></i></button>
                                <h3 id="month-year" class="text-xl font-bold gold-text"></h3>
                                <button id="next-month" class="p-2 rounded-full hover:bg-gray-700"><i class="fas fa-angle-right"></i></button>
                            </div>
                            <div id="calendar-grid" class="grid grid-cols-7 gap-2 text-center">
                                <!-- Calendar will be generated here -->
                            </div>
                        </div>
                        <div id="time-slots-container" class="mt-8 hidden">
                            <h4 class="text-lg font-semibold mb-4 text-center">Available Slots for <span id="selected-date-display" class="gold-text"></span>:</h4>
                            <div id="time-slots-grid" class="grid grid-cols-3 sm:grid-cols-4 gap-4">
                                <!-- Time slots will be generated here -->
                            </div>
                        </div>
                    </div>
                    <div data-aos="fade-left">
                        <div id="booking-form-container" class="bg-light-dark-bg p-6 md:p-8 rounded-lg shadow-2xl hidden">
                            <h3 class="text-2xl font-bold mb-6">Confirm Your <span class="gold-text">Booking</span></h3>
                            <form id="booking-form">
                                <input type="hidden" id="selected-date-input">
                                <input type="hidden" id="selected-time-input">
                                <div class="mb-4">
                                    <label for="name" class="block mb-2">Full Name</label>
                                    <input type="text" id="name" name="name" class="w-full form-input rounded-lg px-4 py-2" required>
                                </div>
                                <div class="mb-4">
                                    <label for="email" class="block mb-2">Email Address</label>
                                    <input type="email" id="email" name="email" class="w-full form-input rounded-lg px-4 py-2" required>
                                </div>
                                <div class="mb-6">
                                    <label for="service" class="block mb-2">Service Type</label>
                                    <select id="service" name="service" class="w-full form-input rounded-lg px-4 py-2" required>
                                        <option value="Bridal Makeup">Bridal Makeup</option>
                                        <option value="Event Makeup">Event Makeup</option>
                                        <option value="Editorial Photoshoot">Editorial Photoshoot</option>
                                        <option value="Personal Consultation">Personal Consultation</option>
                                    </select>
                                </div>
                                <button type="submit" class="w-full gold-bg text-black font-bold py-3 px-6 rounded-full">Confirm Appointment</button>
                            </form>
                        </div>
                        <div id="confirmation-message" class="bg-green-900 border border-green-600 text-green-200 p-6 rounded-lg text-center hidden">
                            <h3 class="text-2xl font-bold mb-2">Thank You!</h3>
                            <p>Your appointment is confirmed. We've sent a confirmation to your email address.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="py-20 md:py-32 bg-light-dark-bg">
            <div class="container mx-auto px-6">
                <h2 class="section-title text-center mb-12" data-aos="fade-up">Get in <span class="gold-text">Touch</span></h2>
                <div class="grid lg:grid-cols-2 gap-12 items-center">
                    <div data-aos="fade-up">
                        <form id="contact-form">
                           <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                               <input type="text" id="contact-name" placeholder="Your Name" class="w-full form-input rounded-lg px-4 py-3" required>
                               <input type="email" placeholder="Your Email" class="w-full form-input rounded-lg px-4 py-3" required>
                           </div>
                           <textarea id="contact-message" placeholder="Your Message" rows="6" class="w-full form-input rounded-lg px-4 py-3 mb-6" required></textarea>
                           <button type="submit" class="w-full gold-bg text-black font-bold py-3 px-6 rounded-full">Send Message</button>
                        </form>
                    </div>
                    <div class="space-y-6" data-aos="fade-up" data-aos-delay="200">
                        <div class="flex items-center space-x-4">
                            <i class="fas fa-map-marker-alt fa-2x gold-text"></i>
                            <p>Jhabua (M.P)</p>
                        </div>
                        <div class="flex items-center space-x-4">
                            <i class="fas fa-phone fa-2x gold-text"></i>
                            <p>+91 6263 136851</p>
                        </div>
                        <div class="flex items-center space-x-4">
                            <i class="fas fa-envelope fa-2x gold-text"></i>
                            <p>contact@gunjanmakeover.com</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-black py-12">
        <div class="container mx-auto px-6 text-center text-gray-400">
            <div class="flex justify-center space-x-6 mb-6">
                <a href="https://www.instagram.com/gunjanmakeover29?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==" target="_blank" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-instagram"></i></a>
                <a href="#" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-youtube"></i></a>
                <a href="#" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-facebook-f"></i></a>
                <a href="#" class="text-2xl hover:gold-text transition-colors"><i class="fab fa-tiktok"></i></a>
            </div>
            <p>&copy; 2025 Gunjan Makeover. All Rights Reserved.</p>
            <p class="text-sm mt-2">Designed with <i class="fas fa-heart gold-text"></i></p>
        </div>
    </footer>

    <!-- Scripts -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize Animate on Scroll
        AOS.init({
            once: true,
            duration: 800,
        });

        // Navbar Scroll Effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Mobile Menu Toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const closeMobileMenuButton = document.getElementById('close-mobile-menu');
        const mobileMenu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileMenuButton.addEventListener('click', () => mobileMenu.classList.remove('hidden'));
        closeMobileMenuButton.addEventListener('click', () => mobileMenu.classList.add('hidden'));
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => mobileMenu.classList.add('hidden'));
        });

        // Dynamic Portfolio Data
        const portfolioData = [
            { img: 'https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1752953221/cmtbhevtcaaaywdjchmz.jpg', category: 'Glamour Look' },
            { img: 'https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1752953360/bzhlw8idq81ay4yvtzbq.jpg', category: 'Bridal Beauty' },
            { img: 'https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1752958179/vqj2atkoborhhfaqcrsd.jpg', category: 'Elegant Look' },
            { img: 'https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1752958609/ceblntlk88xlqw6gxgew.jpg', category: 'Party Ready' }
        ];

        const portfolioGrid = document.querySelector('#portfolio .grid');
        portfolioData.forEach((item, index) => {
            const div = document.createElement('div');
            div.className = 'portfolio-item relative rounded-lg overflow-hidden shadow-lg group aspect-[3/4]';
            div.setAttribute('data-aos', 'fade-up');
            div.setAttribute('data-aos-delay', (index % 4) * 100);
            div.innerHTML = `
                <img src="${item.img}" alt="${item.category}" class="w-full h-full object-cover" onerror="this.onerror=null;this.src='https://placehold.co/600x800/111111/D4AF37?text=Portfolio+Image';">
                <div class="overlay absolute inset-0 flex items-end justify-start p-6">
                    <h3 class="text-white text-2xl font-bold transform translate-y-8 group-hover:translate-y-0 transition-transform duration-500">${item.category}</h3>
                </div>
            `;
            portfolioGrid.appendChild(div);
        });

        // Dynamic Testimonials Data
        const testimonialsData = [
             { name: '_RATHOR._.DIKSHA', quote: 'Hey @gunjanmakeover29, I really want to appreciate your beautiful artistry and the wonderful job you have done on my special day. Such a great experience with you and your team.', stars: 5, img: 'https://placehold.co/96x96/D4AF37/0a0a0a?text=D' },
             { name: 'anshuu._09_', quote: 'Thank you so much MUA - Gunjan Soni. I really appreciate your work & creativity. You are the best MUA. Hairstyling is awesome.', stars: 5, img: 'https://placehold.co/96x96/D4AF37/0a0a0a?text=A' },
            { name: 'Jessica L.', quote: 'Gunjan is a true artist! She made me feel like a queen on my wedding day. The makeup was flawless and lasted all night. I couldn\'t have asked for more.', stars: 5, img: 'https://images.unsplash.com/photo-1580489944761-15a19d654956?q=80&w=1961&auto=format&fit=crop' },
            { name: 'Samantha P.', quote: 'The best makeup experience I have ever had. Gunjan listened to exactly what I wanted and executed it perfectly for my gala event. Highly, highly recommend!', stars: 5, img: 'https://images.unsplash.com/photo-1438761681033-6461ffad8d80?q=80&w=2070&auto=format&fit=crop' },
            { name: 'Chloe T.', quote: 'Working with Gunjan for my magazine shoot was a dream. Professional, creative, and incredibly talented. The looks she created were stunning.', stars: 5, img: 'https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=1888&auto=format&fit=crop' },
            { name: 'Priya S.', quote: 'Absolutely loved my makeup for the family function. Gunjan is professional and uses the best products. Felt so confident!', stars: 5, img: 'https://images.unsplash.com/photo-1599577181262-292158c53755?q=80&w=1887&auto=format&fit=crop' },
            { name: 'Anjali K.', quote: 'The engagement makeup was subtle yet so glamorous, just how I wanted it. Thank you, Gunjan, for making my day special.', stars: 5, img: 'https://images.unsplash.com/photo-1542206395-9feb3edaa68d?q=80&w=1964&auto=format&fit=crop' },
        ];

        const testimonialScroller = document.getElementById('testimonial-scroller');
        
        // Populate original testimonials
        testimonialsData.forEach(t => {
            const slide = document.createElement('div');
            slide.className = 'testimonial-card p-8 rounded-lg shadow-lg';
            let starsHTML = '';
            for(let i=0; i<t.stars; i++) {
                starsHTML += '<i class="fas fa-star text-yellow-400"></i>';
            }
            slide.innerHTML = `
                <img src="${t.img}" alt="${t.name}" class="w-24 h-24 rounded-full mx-auto mb-4 border-4 border-gray-700 object-cover" onerror="this.onerror=null;this.src='https://placehold.co/96x96/0a0a0a/e0e0e0?text=Client';">
                <div class="mb-4">${starsHTML}</div>
                <p class="text-lg italic mb-6">"${t.quote}"</p>
                <h4 class="font-bold text-xl gold-text">- ${t.name}</h4>
            `;
            testimonialScroller.appendChild(slide);
        });

        // Clone and append for seamless scroll
        const originalSlides = testimonialScroller.innerHTML;
        testimonialScroller.innerHTML += originalSlides;
        
        // Calendar & Booking Logic
        const monthYearEl = document.getElementById('month-year');
        const calendarGridEl = document.getElementById('calendar-grid');
        const prevMonthBtn = document.getElementById('prev-month');
        const nextMonthBtn = document.getElementById('next-month');
        const timeSlotsContainer = document.getElementById('time-slots-container');
        const timeSlotsGrid = document.getElementById('time-slots-grid');
        const selectedDateDisplay = document.getElementById('selected-date-display');
        const bookingFormContainer = document.getElementById('booking-form-container');
        const bookingForm = document.getElementById('booking-form');
        const confirmationMessage = document.getElementById('confirmation-message');
        const selectedDateInput = document.getElementById('selected-date-input');
        const selectedTimeInput = document.getElementById('selected-time-input');

        let currentDate = new Date();
        let selectedDate = null;
        let selectedTime = null;

        const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
        const timeSlots = ["09:00 AM", "11:00 AM", "01:00 PM", "03:00 PM", "05:00 PM"];
        // Store booked slots to persist them during navigation
        const bookedSlots = new Map();

        function renderCalendar() {
            calendarGridEl.innerHTML = '';
            const year = currentDate.getFullYear();
            const month = currentDate.getMonth();
            monthYearEl.textContent = `${months[month]} ${year}`;

            const firstDay = new Date(year, month, 1).getDay();
            const daysInMonth = new Date(year, month + 1, 0).getDate();
            
            // Add day names
            ['S', 'M', 'T', 'W', 'T', 'F', 'S'].forEach(day => {
                calendarGridEl.innerHTML += `<div class="font-bold gold-text">${day}</div>`;
            });

            for (let i = 0; i < firstDay; i++) {
                calendarGridEl.innerHTML += '<div></div>';
            }

            for (let day = 1; day <= daysInMonth; day++) {
                const dayEl = document.createElement('div');
                dayEl.textContent = day;
                dayEl.className = 'calendar-day cursor-pointer p-2 rounded-full';
                const today = new Date();
                const dayDate = new Date(year, month, day);

                // Disable past dates
                if (dayDate < today.setHours(0,0,0,0)) {
                    dayEl.classList.add('disabled');
                } else {
                    // Simulate some permanently unavailable dates (e.g., every 5th day)
                    if (day % 5 === 0) {
                        dayEl.classList.add('disabled', 'line-through', 'text-gray-600');
                    } else {
                         dayEl.addEventListener('click', () => selectDate(day, month, year));
                    }
                }
                
                if (selectedDate && day === selectedDate.getDate() && month === selectedDate.getMonth() && year === selectedDate.getFullYear()) {
                    dayEl.classList.add('selected');
                }
                calendarGridEl.appendChild(dayEl);
            }
        }

        function selectDate(day, month, year) {
            selectedDate = new Date(year, month, day);
            selectedTime = null; // Reset time on new date selection
            renderCalendar(); // Re-render to show selection
            
            selectedDateDisplay.textContent = selectedDate.toLocaleDateString('en-US', { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' });
            timeSlotsContainer.classList.remove('hidden');
            bookingFormContainer.classList.add('hidden');
            confirmationMessage.classList.add('hidden');
            renderTimeSlots();
        }

        function renderTimeSlots() {
            timeSlotsGrid.innerHTML = '';
            const dateString = selectedDate.toISOString().split('T')[0];
            
            // Generate or retrieve booked slots for the selected date
            if (!bookedSlots.has(dateString)) {
                const dateBookedTimes = new Set();
                timeSlots.forEach(time => {
                    if (Math.random() > 0.7) { // Simulate random initial unavailability
                        dateBookedTimes.add(time);
                    }
                });
                bookedSlots.set(dateString, dateBookedTimes);
            }

            const dateBookedTimes = bookedSlots.get(dateString);

            timeSlots.forEach(time => {
                const slotEl = document.createElement('button');
                slotEl.type = 'button';
                slotEl.textContent = time;
                slotEl.className = 'time-slot border border-gray-600 rounded-lg p-2 hover:border-gold-500';

                if (dateBookedTimes.has(time)) {
                    slotEl.classList.add('disabled', 'bg-gray-800', 'line-through');
                    slotEl.disabled = true;
                } else {
                    slotEl.addEventListener('click', () => selectTime(time));
                }
                if (time === selectedTime) {
                    slotEl.classList.add('selected');
                }
                timeSlotsGrid.appendChild(slotEl);
            });
        }
        
        function selectTime(time) {
            selectedTime = time;
            renderTimeSlots(); // Re-render to show selection
            bookingFormContainer.classList.remove('hidden');
            confirmationMessage.classList.add('hidden');
            // Smooth scroll to the form
            bookingFormContainer.scrollIntoView({ behavior: 'smooth', block: 'center' });
            
            selectedDateInput.value = selectedDate.toISOString().split('T')[0];
            selectedTimeInput.value = selectedTime;
        }

        prevMonthBtn.addEventListener('click', () => {
            const today = new Date();
            // Prevent going to a month that is entirely in the past
            if (currentDate.getFullYear() > today.getFullYear() || currentDate.getMonth() > today.getMonth()) {
                 currentDate.setMonth(currentDate.getMonth() - 1);
                 renderCalendar();
            }
        });

        nextMonthBtn.addEventListener('click', () => {
            currentDate.setMonth(currentDate.getMonth() + 1);
            renderCalendar();
        });
        
        bookingForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const dateString = selectedDate.toISOString().split('T')[0];
            // Mark the slot as booked
            if(bookedSlots.has(dateString)) {
                bookedSlots.get(dateString).add(selectedTime);
            }

            bookingFormContainer.classList.add('hidden');
            confirmationMessage.classList.remove('hidden');
            bookingForm.reset();
            
            // Reset state after a delay to show confirmation
            setTimeout(() => {
                selectedDate = null;
                selectedTime = null;
                timeSlotsContainer.classList.add('hidden');
                confirmationMessage.classList.add('hidden');
                renderCalendar();
            }, 4000);
        });

        // Contact Form Submission to WhatsApp
        const contactForm = document.getElementById('contact-form');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const name = document.getElementById('contact-name').value;
            const message = document.getElementById('contact-message').value;
            const phoneNumber = '916263136851';
            
            const whatsappURL = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(`Hello, my name is ${name}. My message is: ${message}`)}`;
            
            window.open(whatsappURL, '_blank');
        });

        // Initial Render
        renderCalendar();

    </script>
</body>
</html>
