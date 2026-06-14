# portfolio-website-for-Haneen
Create a luxurious and modern personal portfolio website for a female Computer Science graduate named Haneen. The website should have a professional, elegant, and premium design with smooth animations and a clean user interface.
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Haneen — Computer Science Graduate & Software Developer. Premium portfolio showcasing projects, skills, and services.">
  <title>Haneen | Software Developer</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://code.iconify.design/3/3.1.0/iconify.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            burgundy: { 50:'#fdf2f4', 100:'#fce7eb', 200:'#f9cfdc', 300:'#f4a8bf', 400:'#ec769a', 500:'#e04d74', 600:'#c62a56', 700:'#800020', 800:'#6b001a', 900:'#5c0017' },
            gold: { 50:'#fdf9ed', 100:'#faf0cc', 200:'#f4de94', 300:'#edc85c', 400:'#D4AF37', 500:'#c49a2a', 600:'#a67c1e', 700:'#855e18', 800:'#6d4d1a', 900:'#5c4119' },
            dark: { 50:'#1a1a1a', 100:'#141414', 200:'#111111', 300:'#0E0E0E', 400:'#0B0B0B', 500:'#080808', 600:'#050505', 700:'#030303', 800:'#020202', 900:'#000000' }
          },
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            serif: ['Playfair Display', 'serif']
          }
        }
      }
    }
  </script>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { background: #0B0B0B; color: #f5f5f4; font-family: 'Inter', sans-serif; overflow-x: hidden; }

    /* Scrollbar */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: #0B0B0B; }
    ::-webkit-scrollbar-thumb { background: #800020; border-radius: 3px; }
    ::-webkit-scrollbar-thumb:hover { background: #D4AF37; }

    /* Loading Screen */
    #loader { position: fixed; inset: 0; z-index: 9999; background: #0B0B0B; display: flex; flex-direction: column; align-items: center; justify-content: center; transition: opacity 0.8s ease, visibility 0.8s ease; }
    #loader.hidden { opacity: 0; visibility: hidden; }
    .loader-ring { width: 60px; height: 60px; border: 3px solid rgba(128,0,32,0.2); border-top-color: #D4AF37; border-radius: 50%; animation: spin 1s linear infinite; }
    .loader-text { margin-top: 24px; font-family: 'Playfair Display', serif; font-size: 1.25rem; color: #D4AF37; letter-spacing: 0.15em; animation: pulse-gold 2s ease-in-out infinite; }

    @keyframes spin { to { transform: rotate(360deg); } }
    @keyframes pulse-gold { 0%, 100% { opacity: 0.5; } 50% { opacity: 1; } }

    /* Particles */
    #particles { position: fixed; inset: 0; z-index: 0; pointer-events: none; }

    /* Glassmorphism */
    .glass { background: rgba(255,255,255,0.03); backdrop-filter: blur(16px); -webkit-backdrop-filter: blur(16px); border: 1px solid rgba(255,255,255,0.06); }
    .glass-burgundy { background: rgba(128,0,32,0.08); backdrop-filter: blur(16px); -webkit-backdrop-filter: blur(16px); border: 1px solid rgba(128,0,32,0.15); }
    .glass-gold { background: rgba(212,175,55,0.06); backdrop-filter: blur(16px); -webkit-backdrop-filter: blur(16px); border: 1px solid rgba(212,175,55,0.12); }

    /* Typing cursor */
    .typing-cursor { display: inline-block; width: 3px; height: 1.1em; background: #D4AF37; margin-left: 4px; animation: blink 1s step-end infinite; vertical-align: text-bottom; }
    @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }

    /* Reveal animation */
    .reveal { opacity: 0; transform: translateY(40px); transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1); }
    .reveal.visible { opacity: 1; transform: translateY(0); }
    .reveal-left { opacity: 0; transform: translateX(-60px); transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1); }
    .reveal-left.visible { opacity: 1; transform: translateX(0); }
    .reveal-right { opacity: 0; transform: translateX(60px); transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1); }
    .reveal-right.visible { opacity: 1; transform: translateX(0); }
    .reveal-scale { opacity: 0; transform: scale(0.85); transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1); }
    .reveal-scale.visible { opacity: 1; transform: scale(1); }

    /* Progress bars */
    .skill-bar-fill { width: 0; transition: width 1.5s cubic-bezier(0.16, 1, 0.3, 1); }
    .skill-bar-fill.animate { width: var(--skill-level); }

    /* Gradient text */
    .text-gradient-gold { background: linear-gradient(135deg, #D4AF37, #f0d68a, #D4AF37); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
    .text-gradient-burgundy { background: linear-gradient(135deg, #800020, #c62a56, #800020); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }

    /* Hover glow */
    .glow-gold:hover { box-shadow: 0 0 30px rgba(212,175,55,0.2), 0 0 60px rgba(212,175,55,0.1); }
    .glow-burgundy:hover { box-shadow: 0 0 30px rgba(128,0,32,0.3), 0 0 60px rgba(128,0,32,0.15); }

    /* Card shine effect */
    .card-shine { position: relative; overflow: hidden; }
    .card-shine::before { content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: linear-gradient(45deg, transparent 40%, rgba(212,175,55,0.03) 50%, transparent 60%); transform: rotate(0deg); transition: transform 0.6s ease; pointer-events: none; }
    .card-shine:hover::before { transform: rotate(180deg); }

    /* Timeline */
    .timeline-line { position: absolute; left: 50%; top: 0; bottom: 0; width: 2px; background: linear-gradient(to bottom, transparent, #800020, #D4AF37, #800020, transparent); transform: translateX(-50%); }
    @media (max-width: 767px) { .timeline-line { left: 20px; } }

    /* Nav active */
    .nav-link.active { color: #D4AF37; }
    .nav-link.active::after { width: 100%; }
    .nav-link { position: relative; }
    .nav-link::after { content: ''; position: absolute; bottom: -4px; left: 0; width: 0; height: 2px; background: #D4AF37; transition: width 0.3s ease; }
    .nav-link:hover::after { width: 100%; }

    /* Floating animation */
    @keyframes float { 0%, 100% { transform: translateY(0px); } 50% { transform: translateY(-15px); } }
    .float { animation: float 6s ease-in-out infinite; }

    /* Testimonial card */
    .testimonial-card { transition: transform 0.5s cubic-bezier(0.16, 1, 0.3, 1), box-shadow 0.5s ease; }
    .testimonial-card:hover { transform: translateY(-8px); box-shadow: 0 25px 50px rgba(128,0,32,0.15); }

    /* Service icon pulse */
    @keyframes icon-pulse { 0%, 100% { box-shadow: 0 0 0 0 rgba(212,175,55,0.3); } 50% { box-shadow: 0 0 20px 5px rgba(212,175,55,0.1); } }
    .service-icon:hover { animation: icon-pulse 2s ease-in-out infinite; }

    /* Mobile menu */
    .mobile-menu { transform: translateX(100%); transition: transform 0.4s cubic-bezier(0.16, 1, 0.3, 1); }
    .mobile-menu.open { transform: translateX(0); }

    /* Hero gradient orbs */
    .orb-1 { position: absolute; width: 500px; height: 500px; border-radius: 50%; background: radial-gradient(circle, rgba(128,0,32,0.15), transparent 70%); filter: blur(80px); animation: float 8s ease-in-out infinite; }
    .orb-2 { position: absolute; width: 400px; height: 400px; border-radius: 50%; background: radial-gradient(circle, rgba(212,175,55,0.08), transparent 70%); filter: blur(80px); animation: float 10s ease-in-out infinite reverse; }

    /* Counter animation */
    .counter { display: inline-block; }

    /* Image hover */
    .img-hover { transition: transform 0.7s cubic-bezier(0.16, 1, 0.3, 1), filter 0.7s ease; }
    .img-hover:hover { transform: scale(1.05); filter: brightness(1.1); }

    /* Section divider */
    .section-divider { height: 1px; background: linear-gradient(90deg, transparent, rgba(212,175,55,0.3), rgba(128,0,32,0.3), transparent); }

    /* Button shine */
    .btn-shine { position: relative; overflow: hidden; }
    .btn-shine::after { content: ''; position: absolute; top: -50%; left: -100%; width: 50%; height: 200%; background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent); transform: skewX(-20deg); transition: left 0.6s ease; }
    .btn-shine:hover::after { left: 150%; }

    /* Certificate hover */
    .cert-card { transition: transform 0.5s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.5s ease; }
    .cert-card:hover { transform: translateY(-5px) scale(1.02); border-color: rgba(212,175,55,0.3); }
  </style>
</head>
<body>

<!-- Loading Screen -->
<div id="loader">
  <div class="loader-ring"></div>
  <p class="loader-text">HANEEN</p>
</div>

<!-- Particles Canvas -->
<canvas id="particles"></canvas>

<!-- Navigation -->
<nav id="navbar" class="fixed top-0 left-0 right-0 z-50 transition-all duration-500">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <div class="flex items-center justify-between h-20">
      <!-- Logo -->
      <a href="#home" class="flex items-center gap-2 group">
        <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center text-white font-serif font-bold text-lg group-hover:shadow-lg group-hover:shadow-gold-400/20 transition-shadow duration-300">H</div>
        <span class="text-xl font-serif font-semibold text-white tracking-wide">Haneen</span>
      </a>

      <!-- Desktop Menu -->
      <div class="hidden lg:flex items-center gap-8">
        <a href="#home" class="nav-link text-sm font-medium text-stone-300 hover:text-gold-400 transition-colors duration-300 active">Home</a>
        <a href="#about" class="nav-link text-sm font-medium text-stone-300 hover:text-gold-400 transition-colors duration-300">About</a>
        <a href="#skills" class="nav-link text-sm font-medium text-stone-300 hover:text-gold-400 transition-colors duration-300">Skills</a>
        <a href="#projects" class="nav-link text-sm font-medium text-stone-300 hover:text-gold-400 transition-colors duration-300">Projects</a>
        <a href="#certificates" class="nav-link text-sm font-medium text-stone-300 hover:text-gold-400 transition-colors duration-300">Certificates</a>
        <a href="#services" class="nav-link text-sm font-medium text-stone-300 hover:text-gold-400 transition-colors duration-300">Services</a>
        <a href="#contact" class="nav-link text-sm font-medium text-stone-300 hover:text-gold-400 transition-colors duration-300">Contact</a>
      </div>

      <!-- CTA Button -->
      <a href="#contact" class="hidden lg:inline-flex items-center gap-2 px-6 py-2.5 bg-gradient-to-r from-burgundy-700 to-burgundy-600 text-white text-sm font-medium rounded-full hover:from-gold-400 hover:to-gold-500 hover:text-dark-400 transition-all duration-500 btn-shine">
        Let's Talk
        <span class="iconify" data-icon="lucide:arrow-right" data-width="16"></span>
      </a>

      <!-- Mobile Toggle -->
      <button id="menuToggle" class="lg:hidden w-10 h-10 flex items-center justify-center text-white" aria-label="Toggle menu">
        <span class="iconify" data-icon="lucide:menu" data-width="24" id="menuIcon"></span>
      </button>
    </div>
  </div>
</nav>

<!-- Mobile Menu -->
<div id="mobileMenu" class="mobile-menu fixed top-0 right-0 bottom-0 w-80 max-w-[85vw] z-50 glass-burgundy">
  <div class="flex items-center justify-between p-6 border-b border-white/5">
    <span class="text-lg font-serif text-gold-400">Menu</span>
    <button id="menuClose" class="w-10 h-10 flex items-center justify-center text-white" aria-label="Close menu">
      <span class="iconify" data-icon="lucide:x" data-width="24"></span>
    </button>
  </div>
  <div class="flex flex-col p-6 gap-1">
    <a href="#home" class="mobile-link py-3 px-4 text-stone-300 hover:text-gold-400 hover:bg-white/5 rounded-xl transition-all duration-300 font-medium">Home</a>
    <a href="#about" class="mobile-link py-3 px-4 text-stone-300 hover:text-gold-400 hover:bg-white/5 rounded-xl transition-all duration-300 font-medium">About</a>
    <a href="#skills" class="mobile-link py-3 px-4 text-stone-300 hover:text-gold-400 hover:bg-white/5 rounded-xl transition-all duration-300 font-medium">Skills</a>
    <a href="#projects" class="mobile-link py-3 px-4 text-stone-300 hover:text-gold-400 hover:bg-white/5 rounded-xl transition-all duration-300 font-medium">Projects</a>
    <a href="#certificates" class="mobile-link py-3 px-4 text-stone-300 hover:text-gold-400 hover:bg-white/5 rounded-xl transition-all duration-300 font-medium">Certificates</a>
    <a href="#services" class="mobile-link py-3 px-4 text-stone-300 hover:text-gold-400 hover:bg-white/5 rounded-xl transition-all duration-300 font-medium">Services</a>
    <a href="#contact" class="mobile-link py-3 px-4 text-stone-300 hover:text-gold-400 hover:bg-white/5 rounded-xl transition-all duration-300 font-medium">Contact</a>
    <div class="mt-6 pt-6 border-t border-white/5">
      <a href="#contact" class="flex items-center justify-center gap-2 w-full py-3 bg-gradient-to-r from-burgundy-700 to-gold-400 text-white font-medium rounded-full hover:opacity-90 transition-opacity">Let's Talk</a>
    </div>
  </div>
</div>
<div id="menuOverlay" class="fixed inset-0 bg-black/60 z-40 opacity-0 pointer-events-none transition-opacity duration-300"></div>

<!-- ==================== HERO SECTION ==================== -->
<section id="home" class="relative min-h-screen flex items-center overflow-hidden">
  <div class="orb-1 -top-40 -left-40"></div>
  <div class="orb-2 bottom-0 right-0"></div>

  <div class="relative z-10 max-w-7xl mx-auto px-6 lg:px-8 pt-32 pb-20 w-full">
    <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
      <!-- Text Content -->
      <div class="order-2 lg:order-1">
        <div class="reveal" style="transition-delay: 0.1s;">
          <span class="inline-flex items-center gap-2 px-4 py-2 rounded-full glass-gold text-gold-400 text-xs font-semibold uppercase tracking-widest mb-6">
            <span class="w-2 h-2 rounded-full bg-gold-400 animate-pulse"></span>
            Available for Opportunities
          </span>
        </div>

        <h1 class="reveal font-serif text-4xl sm:text-5xl lg:text-6xl xl:text-7xl font-bold leading-none tracking-tight mb-6" style="transition-delay: 0.2s;">
          <span class="text-white">Hi, I'm</span><br>
          <span class="text-gradient-gold">Haneen</span>
        </h1>

        <div class="reveal mb-8" style="transition-delay: 0.3s;">
          <p class="text-lg sm:text-xl text-stone-400 leading-relaxed">
            <span id="typingText"></span><span class="typing-cursor"></span>
          </p>
        </div>

        <div class="reveal mb-10" style="transition-delay: 0.4s;">
          <blockquote class="border-l-2 border-gold-400/40 pl-4 italic text-stone-500 text-sm leading-relaxed">
            "Technology is best when it brings people together and makes life simpler — that's the kind of impact I strive to create."
          </blockquote>
        </div>

        <div class="reveal flex flex-wrap gap-4" style="transition-delay: 0.5s;">
          <a href="#projects" class="inline-flex items-center gap-2 px-8 py-4 bg-gradient-to-r from-burgundy-700 to-burgundy-600 text-white font-medium rounded-full hover:from-gold-400 hover:to-gold-500 hover:text-dark-400 transition-all duration-500 btn-shine shadow-lg shadow-burgundy-700/25">
            View Projects
            <span class="iconify" data-icon="lucide:arrow-down-right" data-width="18"></span>
          </a>
          <a href="#contact" class="inline-flex items-center gap-2 px-8 py-4 glass text-white font-medium rounded-full hover:border-gold-400/30 transition-all duration-300">
            Contact Me
            <span class="iconify" data-icon="lucide:mail" data-width="18"></span>
          </a>
        </div>

        <!-- Social Links -->
        <div class="reveal flex items-center gap-4 mt-10" style="transition-delay: 0.6s;">
          <span class="text-xs text-stone-600 uppercase tracking-widest">Follow</span>
          <div class="w-8 h-px bg-stone-700"></div>
          <a href="#" class="w-10 h-10 rounded-full glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="GitHub">
            <span class="iconify" data-icon="mdi:github" data-width="20"></span>
          </a>
          <a href="#" class="w-10 h-10 rounded-full glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="LinkedIn">
            <span class="iconify" data-icon="mdi:linkedin" data-width="20"></span>
          </a>
          <a href="#" class="w-10 h-10 rounded-full glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="Facebook">
            <span class="iconify" data-icon="mdi:facebook" data-width="20"></span>
          </a>
        </div>
      </div>

      <!-- Profile Image -->
      <div class="order-1 lg:order-2 flex justify-center reveal-scale" style="transition-delay: 0.3s;">
        <div class="relative">
          <!-- Decorative ring -->
          <div class="absolute -inset-4 rounded-full border border-gold-400/10 animate-spin" style="animation-duration: 30s;"></div>
          <div class="absolute -inset-8 rounded-full border border-burgundy-700/10 animate-spin" style="animation-duration: 45s; animation-direction: reverse;"></div>
          <!-- Image container -->
          <div class="relative w-64 h-64 sm:w-80 sm:h-80 lg:w-96 lg:h-96 rounded-full overflow-hidden border-2 border-gold-400/20 shadow-2xl shadow-burgundy-700/20 float">
            <img src="https://picsum.photos/seed/haneen-portrait/500/500.jpg" alt="Haneen - Software Developer" class="w-full h-full object-cover">
            <div class="absolute inset-0 bg-gradient-to-t from-dark-400/40 via-transparent to-transparent"></div>
          </div>
          <!-- Floating badges -->
          <div class="absolute -right-4 top-12 glass-gold rounded-2xl px-4 py-2 float" style="animation-delay: -2s;">
            <span class="text-gold-400 text-xs font-semibold">CS Graduate</span>
          </div>
          <div class="absolute -left-4 bottom-16 glass-burgundy rounded-2xl px-4 py-2 float" style="animation-delay: -4s;">
            <span class="text-burgundy-300 text-xs font-semibold">Developer</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Scroll indicator -->
  <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 animate-bounce">
    <span class="text-xs text-stone-600 uppercase tracking-widest">Scroll</span>
    <span class="iconify text-gold-400/50" data-icon="lucide:chevron-down" data-width="20"></span>
  </div>
</section>

<!-- Section Divider -->
<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== ABOUT SECTION ==================== -->
<section id="about" class="relative py-24 lg:py-32">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <!-- Section Header -->
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">About Me</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">Get to Know <span class="text-gradient-gold">Haneen</span></h2>
    </div>

    <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
      <!-- Image -->
      <div class="reveal-left">
        <div class="relative rounded-3xl overflow-hidden">
          <img src="https://picsum.photos/seed/haneen-about/600/700.jpg" alt="About Haneen" class="w-full h-[400px] lg:h-[500px] object-cover img-hover">
          <div class="absolute inset-0 bg-gradient-to-t from-dark-400 via-transparent to-transparent"></div>
          <!-- Overlay card -->
          <div class="absolute bottom-6 left-6 right-6 glass rounded-2xl p-5">
            <div class="flex items-center gap-3">
              <div class="w-3 h-3 rounded-full bg-green-400 animate-pulse"></div>
              <span class="text-sm text-stone-300">Open to new opportunities</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Content -->
      <div class="reveal-right">
        <h3 class="font-serif text-2xl font-semibold text-white mb-6">A Passionate Developer with a Vision</h3>
        <p class="text-stone-400 leading-relaxed mb-4">
          I'm Haneen, a Computer Science graduate with a deep passion for building meaningful software solutions. My journey in technology began with curiosity and has evolved into a commitment to creating applications that make a real difference in people's lives.
        </p>
        <p class="text-stone-400 leading-relaxed mb-4">
          Throughout my academic career, I've developed strong foundations in software engineering, database management, and user interface design. I believe that great technology should be accessible, intuitive, and impactful.
        </p>
        <p class="text-stone-400 leading-relaxed mb-8">
          My mission is to leverage technology to solve real-world problems, particularly in healthcare and education, while continuously learning and growing as a developer. I'm always eager to take on new challenges and collaborate with like-minded professionals.
        </p>

        <!-- Education -->
        <div class="glass rounded-2xl p-6 mb-8">
          <div class="flex items-center gap-3 mb-3">
            <span class="iconify text-gold-400" data-icon="lucide:graduation-cap" data-width="20"></span>
            <h4 class="font-semibold text-white">Education</h4>
          </div>
          <p class="text-stone-400 text-sm">Bachelor's Degree in Computer Science</p>
          <p class="text-stone-500 text-xs mt-1">Focused on Software Development & Database Systems</p>
        </div>

        <!-- Stats -->
        <div class="grid grid-cols-3 gap-4">
          <div class="glass-gold rounded-2xl p-5 text-center glow-gold transition-shadow duration-500">
            <div class="text-2xl sm:text-3xl font-bold text-gradient-gold counter" data-target="15">0</div>
            <div class="text-xs text-stone-400 mt-1">Projects</div>
          </div>
          <div class="glass-burgundy rounded-2xl p-5 text-center glow-burgundy transition-shadow duration-500">
            <div class="text-2xl sm:text-3xl font-bold text-gradient-burgundy counter" data-target="10">0</div>
            <div class="text-xs text-stone-400 mt-1">Certificates</div>
          </div>
          <div class="glass-gold rounded-2xl p-5 text-center glow-gold transition-shadow duration-500">
            <div class="text-2xl sm:text-3xl font-bold text-gradient-gold counter" data-target="12">0</div>
            <div class="text-xs text-stone-400 mt-1">Technologies</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== SKILLS SECTION ==================== -->
<section id="skills" class="relative py-24 lg:py-32">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">My Skills</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">Technical <span class="text-gradient-gold">Expertise</span></h2>
    </div>

    <div class="grid md:grid-cols-2 gap-x-16 gap-y-8 max-w-5xl mx-auto">
      <!-- Skill items -->
      <div class="reveal skill-item">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">HTML</span>
          <span class="text-sm font-semibold text-gold-400">95%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 95%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.05s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">CSS</span>
          <span class="text-sm font-semibold text-gold-400">90%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 90%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.1s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">JavaScript</span>
          <span class="text-sm font-semibold text-gold-400">85%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 85%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.15s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">PHP</span>
          <span class="text-sm font-semibold text-gold-400">80%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 80%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.2s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">Python</span>
          <span class="text-sm font-semibold text-gold-400">82%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 82%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.25s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">Visual Basic</span>
          <span class="text-sm font-semibold text-gold-400">75%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 75%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.3s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">Java</span>
          <span class="text-sm font-semibold text-gold-400">78%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 78%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.35s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">MySQL</span>
          <span class="text-sm font-semibold text-gold-400">85%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 85%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.4s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">Android Development</span>
          <span class="text-sm font-semibold text-gold-400">80%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 80%;"></div>
        </div>
      </div>

      <div class="reveal skill-item" style="transition-delay: 0.45s;">
        <div class="flex justify-between mb-2">
          <span class="text-sm font-medium text-stone-300">UI/UX Design</span>
          <span class="text-sm font-semibold text-gold-400">88%</span>
        </div>
        <div class="w-full h-2 rounded-full bg-white/5 overflow-hidden">
          <div class="skill-bar-fill h-full rounded-full bg-gradient-to-r from-burgundy-700 to-gold-400" style="--skill-level: 88%;"></div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== PROJECTS SECTION ==================== -->
<section id="projects" class="relative py-24 lg:py-32">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">Portfolio</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">Featured <span class="text-gradient-gold">Projects</span></h2>
    </div>

    <!-- Featured Project -->
    <div class="reveal mb-12">
      <div class="glass rounded-3xl overflow-hidden card-shine glow-gold transition-shadow duration-500">
        <div class="grid lg:grid-cols-2">
          <div class="relative h-64 lg:h-auto overflow-hidden">
            <img src="https://picsum.photos/seed/my-pharmacy-app/700/500.jpg" alt="My Pharmacy App" class="w-full h-full object-cover img-hover">
            <div class="absolute top-4 left-4 px-3 py-1.5 bg-gold-400 text-dark-400 text-xs font-bold uppercase tracking-wider rounded-full">Featured</div>
          </div>
          <div class="p-8 lg:p-12 flex flex-col justify-center">
            <span class="text-xs font-semibold uppercase tracking-widest text-burgundy-400 mb-3">Android Application</span>
            <h3 class="font-serif text-2xl lg:text-3xl font-bold text-white mb-4">My Pharmacy</h3>
            <p class="text-stone-400 leading-relaxed mb-6">
              An Android application designed to help families organize medications, reminders, and medicine tracking in a simple and user-friendly way. The app provides intuitive medication management, dose reminders, and a comprehensive medicine inventory system that ensures no medication is ever missed.
            </p>
            <div class="flex flex-wrap gap-2 mb-8">
              <span class="px-3 py-1 glass-gold rounded-full text-xs text-gold-400 font-medium">Java</span>
              <span class="px-3 py-1 glass-gold rounded-full text-xs text-gold-400 font-medium">Android</span>
              <span class="px-3 py-1 glass-gold rounded-full text-xs text-gold-400 font-medium">SQLite</span>
              <span class="px-3 py-1 glass-gold rounded-full text-xs text-gold-400 font-medium">XML</span>
              <span class="px-3 py-1 glass-gold rounded-full text-xs text-gold-400 font-medium">Firebase</span>
            </div>
            <div class="flex gap-4">
              <a href="#" class="inline-flex items-center gap-2 px-6 py-3 bg-gradient-to-r from-burgundy-700 to-burgundy-600 text-white text-sm font-medium rounded-full hover:from-gold-400 hover:to-gold-500 hover:text-dark-400 transition-all duration-500 btn-shine">
                <span class="iconify" data-icon="mdi:github" data-width="18"></span>
                GitHub
              </a>
              <a href="#" class="inline-flex items-center gap-2 px-6 py-3 glass text-white text-sm font-medium rounded-full hover:border-gold-400/30 transition-all duration-300">
                <span class="iconify" data-icon="lucide:external-link" data-width="18"></span>
                Live Demo
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Other Projects Grid -->
    <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <!-- Project 2 -->
      <div class="reveal glass rounded-2xl overflow-hidden card-shine group" style="transition-delay: 0.1s;">
        <div class="relative h-48 overflow-hidden">
          <img src="https://picsum.photos/seed/haneen-web-project/500/300.jpg" alt="Web Project" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
          <div class="absolute inset-0 bg-gradient-to-t from-dark-400/80 to-transparent"></div>
        </div>
        <div class="p-6">
          <h4 class="font-serif text-lg font-semibold text-white mb-2">E-Commerce Platform</h4>
          <p class="text-stone-400 text-sm leading-relaxed mb-4">Full-stack web application with product management, cart functionality, and secure payment integration.</p>
          <div class="flex flex-wrap gap-1.5 mb-4">
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">PHP</span>
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">MySQL</span>
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">JavaScript</span>
          </div>
          <div class="flex gap-3">
            <a href="#" class="text-stone-400 hover:text-gold-400 transition-colors"><span class="iconify" data-icon="mdi:github" data-width="20"></span></a>
            <a href="#" class="text-stone-400 hover:text-gold-400 transition-colors"><span class="iconify" data-icon="lucide:external-link" data-width="20"></span></a>
          </div>
        </div>
      </div>

      <!-- Project 3 -->
      <div class="reveal glass rounded-2xl overflow-hidden card-shine group" style="transition-delay: 0.2s;">
        <div class="relative h-48 overflow-hidden">
          <img src="https://picsum.photos/seed/haneen-db-project/500/300.jpg" alt="Database Project" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
          <div class="absolute inset-0 bg-gradient-to-t from-dark-400/80 to-transparent"></div>
        </div>
        <div class="p-6">
          <h4 class="font-serif text-lg font-semibold text-white mb-2">Student Management System</h4>
          <p class="text-stone-400 text-sm leading-relaxed mb-4">Comprehensive database system for managing student records, grades, and academic performance tracking.</p>
          <div class="flex flex-wrap gap-1.5 mb-4">
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">Python</span>
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">MySQL</span>
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">Tkinter</span>
          </div>
          <div class="flex gap-3">
            <a href="#" class="text-stone-400 hover:text-gold-400 transition-colors"><span class="iconify" data-icon="mdi:github" data-width="20"></span></a>
            <a href="#" class="text-stone-400 hover:text-gold-400 transition-colors"><span class="iconify" data-icon="lucide:external-link" data-width="20"></span></a>
          </div>
        </div>
      </div>

      <!-- Project 4 -->
      <div class="reveal glass rounded-2xl overflow-hidden card-shine group" style="transition-delay: 0.3s;">
        <div class="relative h-48 overflow-hidden">
          <img src="https://picsum.photos/seed/haneen-ui-project/500/300.jpg" alt="UI/UX Project" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
          <div class="absolute inset-0 bg-gradient-to-t from-dark-400/80 to-transparent"></div>
        </div>
        <div class="p-6">
          <h4 class="font-serif text-lg font-semibold text-white mb-2">Health & Wellness App</h4>
          <p class="text-stone-400 text-sm leading-relaxed mb-4">Mobile-first application design for tracking daily health metrics, nutrition, and fitness goals.</p>
          <div class="flex flex-wrap gap-1.5 mb-4">
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">UI/UX</span>
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">Figma</span>
            <span class="px-2 py-0.5 glass-gold rounded-full text-[10px] text-gold-400">Prototyping</span>
          </div>
          <div class="flex gap-3">
            <a href="#" class="text-stone-400 hover:text-gold-400 transition-colors"><span class="iconify" data-icon="mdi:github" data-width="20"></span></a>
            <a href="#" class="text-stone-400 hover:text-gold-400 transition-colors"><span class="iconify" data-icon="lucide:external-link" data-width="20"></span></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== CERTIFICATES SECTION ==================== -->
<section id="certificates" class="relative py-24 lg:py-32">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">Achievements</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">Certificates & <span class="text-gradient-gold">Awards</span></h2>
    </div>

    <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-5">
      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.05s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:award" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">Web Development</h4>
        <p class="text-xs text-stone-500">Full Stack Certification</p>
      </div>

      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.1s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:smartphone" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">Android Development</h4>
        <p class="text-xs text-stone-500">Mobile App Certification</p>
      </div>

      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.15s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:database" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">Database Management</h4>
        <p class="text-xs text-stone-500">SQL Professional</p>
      </div>

      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.2s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:palette" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">UI/UX Design</h4>
        <p class="text-xs text-stone-500">Design Thinking Certificate</p>
      </div>

      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.25s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:code-2" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">Python Programming</h4>
        <p class="text-xs text-stone-500">Advanced Python</p>
      </div>

      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.3s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:shield-check" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">Cybersecurity</h4>
        <p class="text-xs text-stone-500">Security Fundamentals</p>
      </div>

      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.35s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:cloud" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">Cloud Computing</h4>
        <p class="text-xs text-stone-500">Cloud Practitioner</p>
      </div>

      <div class="reveal cert-card glass-gold rounded-2xl p-6 text-center" style="transition-delay: 0.4s;">
        <div class="w-14 h-14 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center">
          <span class="iconify text-gold-400" data-icon="lucide:brain" data-width="28"></span>
        </div>
        <h4 class="font-serif font-semibold text-white mb-1">Machine Learning</h4>
        <p class="text-xs text-stone-500">ML Foundations</p>
      </div>
    </div>
  </div>
</section>

<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== SERVICES SECTION ==================== -->
<section id="services" class="relative py-24 lg:py-32">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">What I Offer</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">My <span class="text-gradient-gold">Services</span></h2>
    </div>

    <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <!-- Service 1 -->
      <div class="reveal glass rounded-2xl p-8 text-center card-shine group hover:border-burgundy-700/30 transition-all duration-500 glow-burgundy" style="transition-delay: 0.05s;">
        <div class="service-icon w-16 h-16 mx-auto mb-6 rounded-2xl bg-gradient-to-br from-burgundy-700/20 to-gold-400/20 flex items-center justify-center group-hover:from-burgundy-700/40 group-hover:to-gold-400/40 transition-all duration-500">
          <span class="iconify text-gold-400" data-icon="lucide:globe" data-width="30"></span>
        </div>
        <h4 class="font-serif text-lg font-semibold text-white mb-3">Web Development</h4>
        <p class="text-stone-400 text-sm leading-relaxed">Custom, responsive websites built with modern technologies and best practices for optimal performance.</p>
      </div>

      <!-- Service 2 -->
      <div class="reveal glass rounded-2xl p-8 text-center card-shine group hover:border-burgundy-700/30 transition-all duration-500 glow-burgundy" style="transition-delay: 0.1s;">
        <div class="service-icon w-16 h-16 mx-auto mb-6 rounded-2xl bg-gradient-to-br from-burgundy-700/20 to-gold-400/20 flex items-center justify-center group-hover:from-burgundy-700/40 group-hover:to-gold-400/40 transition-all duration-500">
          <span class="iconify text-gold-400" data-icon="lucide:smartphone" data-width="30"></span>
        </div>
        <h4 class="font-serif text-lg font-semibold text-white mb-3">Mobile App Development</h4>
        <p class="text-stone-400 text-sm leading-relaxed">Native Android applications with intuitive interfaces and seamless user experiences.</p>
      </div>

      <!-- Service 3 -->
      <div class="reveal glass rounded-2xl p-8 text-center card-shine group hover:border-burgundy-700/30 transition-all duration-500 glow-burgundy" style="transition-delay: 0.15s;">
        <div class="service-icon w-16 h-16 mx-auto mb-6 rounded-2xl bg-gradient-to-br from-burgundy-700/20 to-gold-400/20 flex items-center justify-center group-hover:from-burgundy-700/40 group-hover:to-gold-400/40 transition-all duration-500">
          <span class="iconify text-gold-400" data-icon="lucide:database" data-width="30"></span>
        </div>
        <h4 class="font-serif text-lg font-semibold text-white mb-3">Database Design</h4>
        <p class="text-stone-400 text-sm leading-relaxed">Efficient database architectures designed for scalability, security, and data integrity.</p>
      </div>

      <!-- Service 4 -->
      <div class="reveal glass rounded-2xl p-8 text-center card-shine group hover:border-burgundy-700/30 transition-all duration-500 glow-burgundy" style="transition-delay: 0.2s;">
        <div class="service-icon w-16 h-16 mx-auto mb-6 rounded-2xl bg-gradient-to-br from-burgundy-700/20 to-gold-400/20 flex items-center justify-center group-hover:from-burgundy-700/40 group-hover:to-gold-400/40 transition-all duration-500">
          <span class="iconify text-gold-400" data-icon="lucide:pen-tool" data-width="30"></span>
        </div>
        <h4 class="font-serif text-lg font-semibold text-white mb-3">UI/UX Design</h4>
        <p class="text-stone-400 text-sm leading-relaxed">User-centered design solutions that combine aesthetics with functionality for exceptional experiences.</p>
      </div>
    </div>
  </div>
</section>

<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== EXPERIENCE TIMELINE ==================== -->
<section id="experience" class="relative py-24 lg:py-32">
  <div class="max-w-5xl mx-auto px-6 lg:px-8">
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">My Journey</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">Experience <span class="text-gradient-gold">Timeline</span></h2>
    </div>

    <div class="relative">
      <div class="timeline-line hidden md:block"></div>

      <!-- Timeline Item 1 -->
      <div class="reveal relative flex flex-col md:flex-row items-center mb-12" style="transition-delay: 0.1s;">
        <div class="md:w-1/2 md:pr-12 md:text-right mb-4 md:mb-0">
          <span class="text-xs font-semibold text-gold-400 uppercase tracking-widest">2019 - 2020</span>
          <h4 class="font-serif text-xl font-semibold text-white mt-2">Started CS Journey</h4>
          <p class="text-stone-400 text-sm mt-2 leading-relaxed">Enrolled in Computer Science program, discovering the fundamentals of programming and computational thinking.</p>
        </div>
        <div class="relative z-10 w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center shadow-lg shadow-gold-400/20 flex-shrink-0">
          <span class="iconify text-white" data-icon="lucide:rocket" data-width="18"></span>
        </div>
        <div class="md:w-1/2 md:pl-12 mt-4 md:mt-0">
          <div class="glass rounded-xl p-4 inline-block">
            <span class="text-xs text-stone-500">Foundation Year</span>
          </div>
        </div>
      </div>

      <!-- Timeline Item 2 -->
      <div class="reveal relative flex flex-col md:flex-row-reverse items-center mb-12" style="transition-delay: 0.2s;">
        <div class="md:w-1/2 md:pl-12 md:text-left mb-4 md:mb-0">
          <span class="text-xs font-semibold text-gold-400 uppercase tracking-widest">2020 - 2021</span>
          <h4 class="font-serif text-xl font-semibold text-white mt-2">Web Development Focus</h4>
          <p class="text-stone-400 text-sm mt-2 leading-relaxed">Mastered HTML, CSS, JavaScript, and PHP. Built first full-stack web applications and database-driven systems.</p>
        </div>
        <div class="relative z-10 w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center shadow-lg shadow-gold-400/20 flex-shrink-0">
          <span class="iconify text-white" data-icon="lucide:code-2" data-width="18"></span>
        </div>
        <div class="md:w-1/2 md:pr-12 md:text-right mt-4 md:mt-0">
          <div class="glass rounded-xl p-4 inline-block">
            <span class="text-xs text-stone-500">Growth Phase</span>
          </div>
        </div>
      </div>

      <!-- Timeline Item 3 -->
      <div class="reveal relative flex flex-col md:flex-row items-center mb-12" style="transition-delay: 0.3s;">
        <div class="md:w-1/2 md:pr-12 md:text-right mb-4 md:mb-0">
          <span class="text-xs font-semibold text-gold-400 uppercase tracking-widest">2021 - 2022</span>
          <h4 class="font-serif text-xl font-semibold text-white mt-2">Android Development</h4>
          <p class="text-stone-400 text-sm mt-2 leading-relaxed">Ventured into mobile app development with Java and Android Studio. Created "My Pharmacy" as a major project.</p>
        </div>
        <div class="relative z-10 w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center shadow-lg shadow-gold-400/20 flex-shrink-0">
          <span class="iconify text-white" data-icon="lucide:smartphone" data-width="18"></span>
        </div>
        <div class="md:w-1/2 md:pl-12 mt-4 md:mt-0">
          <div class="glass rounded-xl p-4 inline-block">
            <span class="text-xs text-stone-500">Mobile Era</span>
          </div>
        </div>
      </div>

      <!-- Timeline Item 4 -->
      <div class="reveal relative flex flex-col md:flex-row-reverse items-center mb-12" style="transition-delay: 0.4s;">
        <div class="md:w-1/2 md:pl-12 md:text-left mb-4 md:mb-0">
          <span class="text-xs font-semibold text-gold-400 uppercase tracking-widest">2022 - 2023</span>
          <h4 class="font-serif text-xl font-semibold text-white mt-2">UI/UX & Design Thinking</h4>
          <p class="text-stone-400 text-sm mt-2 leading-relaxed">Deepened expertise in user experience design, prototyping, and creating intuitive interfaces for applications.</p>
        </div>
        <div class="relative z-10 w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center shadow-lg shadow-gold-400/20 flex-shrink-0">
          <span class="iconify text-white" data-icon="lucide:palette" data-width="18"></span>
        </div>
        <div class="md:w-1/2 md:pr-12 md:text-right mt-4 md:mt-0">
          <div class="glass rounded-xl p-4 inline-block">
            <span class="text-xs text-stone-500">Design Phase</span>
          </div>
        </div>
      </div>

      <!-- Timeline Item 5 -->
      <div class="reveal relative flex flex-col md:flex-row items-center" style="transition-delay: 0.5s;">
        <div class="md:w-1/2 md:pr-12 md:text-right mb-4 md:mb-0">
          <span class="text-xs font-semibold text-gold-400 uppercase tracking-widest">2023 - Present</span>
          <h4 class="font-serif text-xl font-semibold text-white mt-2">Graduation & Beyond</h4>
          <p class="text-stone-400 text-sm mt-2 leading-relaxed">Graduated with honors. Ready to contribute to innovative projects and make an impact in the tech industry.</p>
        </div>
        <div class="relative z-10 w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center shadow-lg shadow-gold-400/20 flex-shrink-0">
          <span class="iconify text-white" data-icon="lucide:graduation-cap" data-width="18"></span>
        </div>
        <div class="md:w-1/2 md:pl-12 mt-4 md:mt-0">
          <div class="glass-gold rounded-xl p-4 inline-block">
            <span class="text-xs text-gold-400 font-semibold">Current Chapter ✨</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== TESTIMONIALS SECTION ==================== -->
<section id="testimonials" class="relative py-24 lg:py-32">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">Testimonials</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">What People <span class="text-gradient-gold">Say</span></h2>
    </div>

    <div class="grid md:grid-cols-3 gap-6">
      <!-- Testimonial 1 -->
      <div class="reveal testimonial-card glass rounded-2xl p-8" style="transition-delay: 0.1s;">
        <div class="flex items-center gap-1 mb-4">
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
        </div>
        <p class="text-stone-400 text-sm leading-relaxed mb-6 italic">"Haneen's attention to detail and dedication to quality is remarkable. Her pharmacy app project demonstrated both technical skill and genuine care for user needs."</p>
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center text-white font-serif font-bold text-sm">D</div>
          <div>
            <p class="text-sm font-semibold text-white">Dr. Ahmad</p>
            <p class="text-xs text-stone-500">Project Supervisor</p>
          </div>
        </div>
      </div>

      <!-- Testimonial 2 -->
      <div class="reveal testimonial-card glass rounded-2xl p-8" style="transition-delay: 0.2s;">
        <div class="flex items-center gap-1 mb-4">
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
        </div>
        <p class="text-stone-400 text-sm leading-relaxed mb-6 italic">"Working with Haneen on our team project was an excellent experience. She brings creative solutions and always delivers beyond expectations."</p>
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center text-white font-serif font-bold text-sm">S</div>
          <div>
            <p class="text-sm font-semibold text-white">Sara K.</p>
            <p class="text-xs text-stone-500">University Colleague</p>
          </div>
        </div>
      </div>

      <!-- Testimonial 3 -->
      <div class="reveal testimonial-card glass rounded-2xl p-8" style="transition-delay: 0.3s;">
        <div class="flex items-center gap-1 mb-4">
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
          <span class="iconify text-gold-400" data-icon="lucide:star" data-width="16"></span>
        </div>
        <p class="text-stone-400 text-sm leading-relaxed mb-6 italic">"Haneen transformed our outdated system into a modern, efficient solution. Her expertise in both design and development is truly impressive."</p>
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center text-white font-serif font-bold text-sm">M</div>
          <div>
            <p class="text-sm font-semibold text-white">Mohammed R.</p>
            <p class="text-xs text-stone-500">Client</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="section-divider max-w-4xl mx-auto"></div>

<!-- ==================== CONTACT SECTION ==================== -->
<section id="contact" class="relative py-24 lg:py-32">
  <div class="max-w-7xl mx-auto px-6 lg:px-8">
    <div class="text-center mb-16">
      <span class="reveal inline-block text-xs font-semibold uppercase tracking-widest text-gold-400 mb-4">Get in Touch</span>
      <h2 class="reveal font-serif text-3xl sm:text-4xl lg:text-5xl font-bold text-white tracking-tight">Let's Work <span class="text-gradient-gold">Together</span></h2>
      <p class="reveal text-stone-400 mt-4 max-w-xl mx-auto">Have a project in mind or want to collaborate? I'd love to hear from you. Let's create something extraordinary.</p>
    </div>

    <div class="grid lg:grid-cols-5 gap-12">
      <!-- Contact Info -->
      <div class="lg:col-span-2 space-y-6">
        <div class="reveal glass rounded-2xl p-6 flex items-start gap-4 group hover:border-gold-400/20 transition-all duration-300" style="transition-delay: 0.1s;">
          <div class="w-12 h-12 rounded-xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center flex-shrink-0 group-hover:from-burgundy-700/50 group-hover:to-gold-400/50 transition-all duration-300">
            <span class="iconify text-gold-400" data-icon="lucide:mail" data-width="22"></span>
          </div>
          <div>
            <h4 class="font-semibold text-white text-sm mb-1">Email</h4>
            <a href="mailto:hanonshaheen074@gmail.com" class="text-stone-400 text-sm hover:text-gold-400 transition-colors break-all">hanonshaheen074@gmail.com</a>
          </div>
        </div>

        <div class="reveal glass rounded-2xl p-6 flex items-start gap-4 group hover:border-gold-400/20 transition-all duration-300" style="transition-delay: 0.15s;">
          <div class="w-12 h-12 rounded-xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center flex-shrink-0 group-hover:from-burgundy-700/50 group-hover:to-gold-400/50 transition-all duration-300">
            <span class="iconify text-gold-400" data-icon="lucide:phone" data-width="22"></span>
          </div>
          <div>
            <h4 class="font-semibold text-white text-sm mb-1">Phone</h4>
            <p class="text-stone-400 text-sm">+970 5XX XXX XXX</p>
          </div>
        </div>

        <div class="reveal glass rounded-2xl p-6 flex items-start gap-4 group hover:border-gold-400/20 transition-all duration-300" style="transition-delay: 0.2s;">
          <div class="w-12 h-12 rounded-xl bg-gradient-to-br from-burgundy-700/30 to-gold-400/30 flex items-center justify-center flex-shrink-0 group-hover:from-burgundy-700/50 group-hover:to-gold-400/50 transition-all duration-300">
            <span class="iconify text-gold-400" data-icon="lucide:map-pin" data-width="22"></span>
          </div>
          <div>
            <h4 class="font-semibold text-white text-sm mb-1">Location</h4>
            <p class="text-stone-400 text-sm">Mansoura</p>
          </div>
        </div>

        <!-- Social Links -->
        <div class="reveal pt-4" style="transition-delay: 0.25s;">
          <p class="text-xs text-stone-600 uppercase tracking-widest mb-4">Connect with me</p>
          <div class="flex gap-3">
            <a href="#" class="w-11 h-11 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="GitHub">
              <span class="iconify" data-icon="mdi:github" data-width="22"></span>
            </a>
            <a href="#" class="w-11 h-11 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="LinkedIn">
              <span class="iconify" data-icon="mdi:linkedin" data-width="22"></span>
            </a>
            <a href="#" class="w-11 h-11 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="Facebook">
              <span class="iconify" data-icon="mdi:facebook" data-width="22"></span>
            </a>
            <a href="mailto:hanonshaheen074@gmail.com" class="w-11 h-11 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="Email">
              <span class="iconify" data-icon="lucide:mail" data-width="22"></span>
            </a>
          </div>
        </div>
      </div>

      <!-- Contact Form -->
      <div class="lg:col-span-3 reveal" style="transition-delay: 0.2s;">
        <form id="contactForm" class="glass rounded-3xl p-8 lg:p-10 space-y-6">
          <div class="grid sm:grid-cols-2 gap-6">
            <div>
              <label for="name" class="block text-xs font-semibold text-stone-400 uppercase tracking-wider mb-2">Name</label>
              <input type="text" id="name" name="name" required placeholder="Your full name" class="w-full px-4 py-3.5 bg-white/5 border border-white/10 rounded-xl text-white placeholder-stone-600 text-sm focus:outline-none focus:border-gold-400/40 focus:bg-white/[0.07] transition-all duration-300">
            </div>
            <div>
              <label for="email" class="block text-xs font-semibold text-stone-400 uppercase tracking-wider mb-2">Email</label>
              <input type="email" id="email" name="email" required placeholder="your@email.com" class="w-full px-4 py-3.5 bg-white/5 border border-white/10 rounded-xl text-white placeholder-stone-600 text-sm focus:outline-none focus:border-gold-400/40 focus:bg-white/[0.07] transition-all duration-300">
            </div>
          </div>
          <div>
            <label for="subject" class="block text-xs font-semibold text-stone-400 uppercase tracking-wider mb-2">Subject</label>
            <input type="text" id="subject" name="subject" required placeholder="Project inquiry" class="w-full px-4 py-3.5 bg-white/5 border border-white/10 rounded-xl text-white placeholder-stone-600 text-sm focus:outline-none focus:border-gold-400/40 focus:bg-white/[0.07] transition-all duration-300">
          </div>
          <div>
            <label for="message" class="block text-xs font-semibold text-stone-400 uppercase tracking-wider mb-2">Message</label>
            <textarea id="message" name="message" rows="5" required placeholder="Tell me about your project..." class="w-full px-4 py-3.5 bg-white/5 border border-white/10 rounded-xl text-white placeholder-stone-600 text-sm focus:outline-none focus:border-gold-400/40 focus:bg-white/[0.07] transition-all duration-300 resize-none"></textarea>
          </div>
          <button type="submit" class="w-full sm:w-auto inline-flex items-center justify-center gap-2 px-10 py-4 bg-gradient-to-r from-burgundy-700 to-burgundy-600 text-white font-medium rounded-full hover:from-gold-400 hover:to-gold-500 hover:text-dark-400 transition-all duration-500 btn-shine shadow-lg shadow-burgundy-700/25">
            Send Message
            <span class="iconify" data-icon="lucide:send" data-width="18"></span>
          </button>
          <!-- Success message -->
          <div id="formSuccess" class="hidden items-center gap-2 px-4 py-3 bg-green-500/10 border border-green-500/20 rounded-xl text-green-400 text-sm">
            <span class="iconify" data-icon="lucide:check-circle" data-width="18"></span>
            <span>Message sent successfully! I'll get back to you soon.</span>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>

<!-- ==================== FOOTER ==================== -->
<footer class="relative border-t border-white/5">
  <div class="max-w-7xl mx-auto px-6 lg:px-8 py-16">
    <div class="grid md:grid-cols-3 gap-12 mb-12">
      <!-- Brand -->
      <div>
        <div class="flex items-center gap-2 mb-4">
          <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-burgundy-700 to-gold-400 flex items-center justify-center text-white font-serif font-bold text-lg">H</div>
          <span class="text-xl font-serif font-semibold text-white">Haneen</span>
        </div>
        <p class="text-stone-500 text-sm leading-relaxed">Computer Science Graduate & Software Developer crafting elegant digital experiences with passion and precision.</p>
      </div>

      <!-- Quick Links -->
      <div>
        <h4 class="font-semibold text-white mb-4 text-sm">Quick Links</h4>
        <div class="grid grid-cols-2 gap-2">
          <a href="#home" class="text-stone-500 hover:text-gold-400 text-sm transition-colors duration-300">Home</a>
          <a href="#about" class="text-stone-500 hover:text-gold-400 text-sm transition-colors duration-300">About</a>
          <a href="#skills" class="text-stone-500 hover:text-gold-400 text-sm transition-colors duration-300">Skills</a>
          <a href="#projects" class="text-stone-500 hover:text-gold-400 text-sm transition-colors duration-300">Projects</a>
          <a href="#services" class="text-stone-500 hover:text-gold-400 text-sm transition-colors duration-300">Services</a>
          <a href="#contact" class="text-stone-500 hover:text-gold-400 text-sm transition-colors duration-300">Contact</a>
        </div>
      </div>

      <!-- Social -->
      <div>
        <h4 class="font-semibold text-white mb-4 text-sm">Connect</h4>
        <div class="flex gap-3">
          <a href="#" class="w-10 h-10 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="GitHub">
            <span class="iconify" data-icon="mdi:github" data-width="20"></span>
          </a>
          <a href="#" class="w-10 h-10 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="LinkedIn">
            <span class="iconify" data-icon="mdi:linkedin" data-width="20"></span>
          </a>
          <a href="#" class="w-10 h-10 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="Facebook">
            <span class="iconify" data-icon="mdi:facebook" data-width="20"></span>
          </a>
          <a href="mailto:hanonshaheen074@gmail.com" class="w-10 h-10 rounded-xl glass flex items-center justify-center text-stone-400 hover:text-gold-400 hover:border-gold-400/30 transition-all duration-300" aria-label="Email">
            <span class="iconify" data-icon="lucide:mail" data-width="20"></span>
          </a>
        </div>
      </div>
    </div>

    <!-- Bottom bar -->
    <div class="section-divider mb-8"></div>
    <div class="flex flex-col sm:flex-row items-center justify-between gap-4">
      <p class="text-stone-600 text-xs">&copy; 2025 Haneen. All rights reserved.</p>
      <p class="text-stone-700 text-xs">Designed with <span class="text-burgundy-700">♥</span> and dedication</p>
    </div>
  </div>
</footer>

<!-- ==================== BACK TO TOP ==================== -->
<button id="backToTop" class="fixed bottom-8 right-8 z-40 w-12 h-12 rounded-full bg-gradient-to-br from-burgundy-700 to-gold-400 text-white flex items-center justify-center shadow-lg shadow-burgundy-700/30 opacity-0 pointer-events-none transition-all duration-500 hover:scale-110" aria-label="Back to top">
  <span class="iconify" data-icon="lucide:chevron-up" data-width="22"></span>
</button>

<!-- ==================== JAVASCRIPT ==================== -->
<script>
// ===== LOADING SCREEN =====
window.addEventListener('load', () => {
  setTimeout(() => {
    document.getElementById('loader').classList.add('hidden');
  }, 1500);
});

// ===== PARTICLES =====
(function() {
  const canvas = document.getElementById('particles');
  const ctx = canvas.getContext('2d');
  let particles = [];
  let w, h;

  function resize() {
    w = canvas.width = window.innerWidth;
    h = canvas.height = window.innerHeight;
  }
  resize();
  window.addEventListener('resize', resize);

  class Particle {
    constructor() {
      this.reset();
    }
    reset() {
      this.x = Math.random() * w;
      this.y = Math.random() * h;
      this.size = Math.random() * 1.5 + 0.5;
      this.speedX = (Math.random() - 0.5) * 0.3;
      this.speedY = (Math.random() - 0.5) * 0.3;
      this.opacity = Math.random() * 0.4 + 0.1;
      this.color = Math.random() > 0.6 ? '212,175,55' : '128,0,32';
    }
    update() {
      this.x += this.speedX;
      this.y += this.speedY;
      if (this.x < 0 || this.x > w || this.y < 0 || this.y > h) this.reset();
    }
    draw() {
      ctx.beginPath();
      ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
      ctx.fillStyle = `rgba(${this.color},${this.opacity})`;
      ctx.fill();
    }
  }

  const count = Math.min(80, Math.floor(w * h / 15000));
  for (let i = 0; i < count; i++) particles.push(new Particle());

  function connectParticles() {
    for (let a = 0; a < particles.length; a++) {
      for (let b = a + 1; b < particles.length; b++) {
        const dx = particles[a].x - particles[b].x;
        const dy = particles[a].y - particles[b].y;
        const dist = Math.sqrt(dx * dx + dy * dy);
        if (dist < 120) {
          ctx.beginPath();
          ctx.strokeStyle = `rgba(212,175,55,${0.04 * (1 - dist / 120)})`;
          ctx.lineWidth = 0.5;
          ctx.moveTo(particles[a].x, particles[a].y);
          ctx.lineTo(particles[b].x, particles[b].y);
          ctx.stroke();
        }
      }
    }
  }

  function animate() {
    ctx.clearRect(0, 0, w, h);
    particles.forEach(p => { p.update(); p.draw(); });
    connectParticles();
    requestAnimationFrame(animate);
  }
  animate();
})();

// ===== NAVBAR =====
const navbar = document.getElementById('navbar');
let lastScroll = 0;

window.addEventListener('scroll', () => {
  const scroll = window.scrollY;
  if (scroll > 50) {
    navbar.classList.add('glass');
    navbar.style.borderBottom = '1px solid rgba(255,255,255,0.05)';
  } else {
    navbar.classList.remove('glass');
    navbar.style.borderBottom = 'none';
  }
  lastScroll = scroll;
});

// ===== MOBILE MENU =====
const menuToggle = document.getElementById('menuToggle');
const menuClose = document.getElementById('menuClose');
const mobileMenu = document.getElementById('mobileMenu');
const menuOverlay = document.getElementById('menuOverlay');
const mobileLinks = document.querySelectorAll('.mobile-link');

function openMenu() {
  mobileMenu.classList.add('open');
  menuOverlay.style.opacity = '1';
  menuOverlay.style.pointerEvents = 'auto';
  document.body.style.overflow = 'hidden';
}
function closeMenu() {
  mobileMenu.classList.remove('open');
  menuOverlay.style.opacity = '0';
  menuOverlay.style.pointerEvents = 'none';
  document.body.style.overflow = '';
}

menuToggle.addEventListener('click', openMenu);
menuClose.addEventListener('click', closeMenu);
menuOverlay.addEventListener('click', closeMenu);
mobileLinks.forEach(link => link.addEventListener('click', closeMenu));

// ===== ACTIVE NAV LINK =====
const sections = document.querySelectorAll('section[id]');
const navLinks = document.querySelectorAll('.nav-link');

window.addEventListener('scroll', () => {
  let current = '';
  sections.forEach(section => {
    const top = section.offsetTop - 100;
    if (window.scrollY >= top) current = section.getAttribute('id');
  });
  navLinks.forEach(link => {
    link.classList.remove('active');
    if (link.getAttribute('href') === `#${current}`) link.classList.add('active');
  });
});

// ===== TYPING EFFECT =====
const typingTexts = [
  'Computer Science Graduate',
  'Software Developer',
  'Android App Creator',
  'UI/UX Enthusiast',
  'Problem Solver'
];
let textIndex = 0;
let charIndex = 0;
let isDeleting = false;
const typingElement = document.getElementById('typingText');

function type() {
  const current = typingTexts[textIndex];
  if (isDeleting) {
    typingElement.textContent = current.substring(0, charIndex - 1);
    charIndex--;
  } else {
    typingElement.textContent = current.substring(0, charIndex + 1);
    charIndex++;
  }

  let speed = isDeleting ? 40 : 80;

  if (!isDeleting && charIndex === current.length) {
    speed = 2000;
    isDeleting = true;
  } else if (isDeleting && charIndex === 0) {
    isDeleting = false;
    textIndex = (textIndex + 1) % typingTexts.length;
    speed = 500;
  }

  setTimeout(type, speed);
}
setTimeout(type, 2000);

// ===== SCROLL REVEAL =====
const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      if (entry.target.classList.contains('skill-item')) {
        const bar = entry.target.querySelector('.skill-bar-fill');
        if (bar) setTimeout(() => bar.classList.add('animate'), 200);
      }
    }
  });
}, { threshold: 0.1, rootMargin: '0px 0px -50px 0px' });

document.querySelectorAll('.reveal, .reveal-left, .reveal-right, .reveal-scale, .skill-item').forEach(el => {
  revealObserver.observe(el);
});

// ===== COUNTER ANIMATION =====
const counterObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const counter = entry.target;
      const target = parseInt(counter.dataset.target);
      let count = 0;
      const duration = 2000;
      const step = target / (duration / 16);
      const timer = setInterval(() => {
        count += step;
        if (count >= target) {
          count = target;
          clearInterval(timer);
        }
        counter.textContent = Math.floor(count) + '+';
      }, 16);
      counterObserver.unobserve(counter);
    }
  });
}, { threshold: 0.5 });

document.querySelectorAll('.counter').forEach(el => counterObserver.observe(el));

// ===== BACK TO TOP =====
const backToTop = document.getElementById('backToTop');
window.addEventListener('scroll', () => {
  if (window.scrollY > 500) {
    backToTop.style.opacity = '1';
    backToTop.style.pointerEvents = 'auto';
  } else {
    backToTop.style.opacity = '0';
    backToTop.style.pointerEvents = 'none';
  }
});
backToTop.addEventListener('click', () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
});

// ===== CONTACT FORM =====
document.getElementById('contactForm').addEventListener('submit', function(e) {
  e.preventDefault();
  const btn = this.querySelector('button[type="submit"]');
  const originalText = btn.innerHTML;
  btn.innerHTML = '<span class="iconify animate-spin" data-icon="lucide:loader-2" data-width="18"></span> Sending...';
  btn.disabled = true;

  setTimeout(() => {
    btn.innerHTML = originalText;
    btn.disabled = false;
    const success = document.getElementById('formSuccess');
    success.classList.remove('hidden');
    success.classList.add('flex');
    this.reset();
    setTimeout(() => {
      success.classList.add('hidden');
      success.classList.remove('flex');
    }, 5000);
  }, 1500);
});

// ===== SMOOTH SCROLL FOR ANCHOR LINKS =====
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function(e) {
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    if (target) {
      target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
  });
});
</script>

</body>
</html>
