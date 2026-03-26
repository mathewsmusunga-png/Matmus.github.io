# Matmus.github.io
For learning 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Pre-emptive Healthcare Movement (PHM) - Empowering individuals in Zambia to take control of their health through preventive care, education, and community support.">
    <title>Pre-emptive Healthcare Movement (PHM) | Zambia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;family=Space+Grotesk:wght@500;600&amp;display=swap');
        
        :root {
            --primary: #10b981;
        }
        
        * {
            transition-property: color, background-color, border-color, text-decoration-color, fill, stroke, transform, opacity;
            transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
            transition-duration: 150ms;
        }
        
        .hero-bg {
            background: linear-gradient(90deg, rgba(16, 185, 129, 0.92) 0%, rgba(16, 185, 129, 0.85) 100%), 
                        url('https://picsum.photos/id/1015/2000/1200') center/cover no-repeat;
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #10b981;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        .section-header {
            position: relative;
        }
        
        .section-header:after {
            content: '';
            position: absolute;
            width: 60px;
            height: 3px;
            background: #10b981;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .card-hover {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .card-hover:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
        }
        
        /* ENHANCED MODAL ANIMATIONS */
        .modal-overlay {
            animation: modalBackdropIn 0.3s ease forwards;
        }
        
        @keyframes modalBackdropIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        
        .modal {
            animation: modalSlideUp 0.45s cubic-bezier(0.34, 1.56, 0.64, 1) forwards;
            /* bouncy spring feel */
        }
        
        @keyframes modalSlideUp {
            0% {
                opacity: 0;
                transform: translateY(40px) scale(0.95);
            }
            60% {
                transform: translateY(-8px) scale(1.03);
            }
            100% {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }
        
        .modal-exit {
            animation: modalSlideDown 0.3s cubic-bezier(0.4, 0, 1, 1) forwards;
        }
        
        @keyframes modalSlideDown {
            0% { opacity: 1; transform: translateY(0) scale(1); }
            100% { opacity: 0; transform: translateY(30px) scale(0.95); }
        }
        
        .modal-content-inner {
            animation: modalContentFade 0.5s cubic-bezier(0.23, 1, 0.32, 1) 80ms both;
        }
        
        @keyframes modalContentFade {
            0% { opacity: 0; transform: translateY(15px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        
        .modal-close-btn {
            transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .modal-close-btn:hover {
            transform: rotate(90deg) scale(1.15);
        }
        
        .program-card {
            cursor: pointer;
        }
        
        .stat-number {
            font-variant-numeric: tabular-nums;
        }
    </style>
</head>
<body class="font-sans antialiased">
    <!-- NAVBAR (unchanged from previous version) -->
    <nav class="bg-white border-b sticky top-0 z-50 shadow-sm">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center gap-x-3">
                    <div class="w-10 h-10 bg-emerald-600 rounded-2xl flex items-center justify-center text-white text-2xl shadow-inner">
                        <i class="fa-solid fa-heart-pulse"></i>
                    </div>
                    <div>
                        <span class="text-2xl font-semibold tracking-tight text-emerald-600">PHM</span>
                        <span class="text-sm font-medium text-gray-500 block -mt-1">Zambia</span>
                    </div>
                </div>

                <div class="hidden md:flex items-center gap-x-8 text-sm font-medium">
                    <a href="#about" class="nav-link text-gray-700 hover:text-emerald-600">About</a>
                    <a href="#vision" class="nav-link text-gray-700 hover:text-emerald-600">Vision &amp; Mission</a>
                    <a href="#objectives" class="nav-link text-gray-700 hover:text-emerald-600">Objectives</a>
                    <a href="#programs" class="nav-link text-gray-700 hover:text-emerald-600">Programs</a>
                    <a href="#impact" class="nav-link text-gray-700 hover:text-emerald-600">Impact</a>
                    <a href="#get-involved" class="nav-link text-gray-700 hover:text-emerald-600">Get Involved</a>
                </div>

                <div class="flex items-center gap-x-4">
                    <a href="#get-involved" 
                       class="px-6 py-2.5 bg-emerald-600 hover:bg-emerald-700 text-white text-sm font-semibold rounded-2xl flex items-center gap-x-2">
                        <i class="fa-solid fa-hand-holding-heart"></i>
                        DONATE
                    </a>
                    <button onclick="toggleMobileMenu()" 
                            class="md:hidden w-10 h-10 flex items-center justify-center text-2xl text-gray-700">
                        <i id="mobile-icon" class="fa-solid fa-bars"></i>
                    </button>
                </div>
            </div>
            
            <div id="mobile-menu" class="hidden md:hidden border-t py-4 bg-white">
                <div class="flex flex-col gap-y-4 px-6 text-sm font-medium">
                    <a href="#about" onclick="toggleMobileMenu()" class="py-2 text-gray-700">About PHM</a>
                    <a href="#vision" onclick="toggleMobileMenu()" class="py-2 text-gray-700">Vision &amp; Mission</a>
                    <a href="#objectives" onclick="toggleMobileMenu()" class="py-2 text-gray-700">Objectives</a>
                    <a href="#programs" onclick="toggleMobileMenu()" class="py-2 text-gray-700">Programs &amp; Services</a>
                    <a href="#impact" onclick="toggleMobileMenu()" class="py-2 text-gray-700">Expected Impact</a>
                    <a href="#get-involved" onclick="toggleMobileMenu()" class="py-2 text-gray-700">Get Involved</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- HERO, ABOUT, VISION, OBJECTIVES, IMPACT sections unchanged (full code available from previous version) -->
    <!-- INTERACTIVE PROGRAMS SECTION (unchanged) -->
    <section id="programs" class="py-20 bg-emerald-900 text-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-end mb-12">
                <div>
                    <span class="text-emerald-400 text-sm font-medium tracking-widest">INTERACTIVE PROGRAMS</span>
                    <h2 class="text-4xl font-semibold">Discover Our Programs</h2>
                    <p class="text-emerald-300 mt-2">Click any card below to explore detailed information, impact metrics, and how to get involved</p>
                </div>
                <div class="hidden md:flex items-center text-emerald-300 text-sm font-medium">
                    <i class="fa-solid fa-mouse-pointer mr-2"></i>
                    Click cards for full details
                </div>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6" id="programs-grid">
                <!-- Populated by JavaScript -->
            </div>
        </div>
    </section>

    <!-- ENHANCED PROGRAM DETAIL MODAL -->
    <div id="program-modal" onclick="if(event.target === this) closeModal()" 
         class="hidden fixed inset-0 bg-black/70 z-[9999] flex items-center justify-center p-4 modal-overlay">
        
        <div onclick="event.stopImmediatePropagation()" 
             id="modal-content-wrapper"
             class="modal bg-white text-gray-900 rounded-3xl max-w-2xl w-full max-h-[90vh] overflow-hidden flex flex-col shadow-2xl border border-white">
            
            <!-- Header -->
            <div class="px-8 pt-6 pb-4 border-b flex items-center justify-between">
                <div id="modal-icon" class="text-5xl"></div>
                <h2 id="modal-title" class="text-3xl font-semibold flex-1 px-6"></h2>
                <button onclick="closeModal()" 
                        class="modal-close-btn w-11 h-11 flex items-center justify-center text-4xl text-gray-400 hover:text-gray-600 rounded-2xl">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
            
            <!-- Scrollable Content -->
            <div class="flex-1 overflow-auto px-8 py-8 modal-content-inner" id="modal-body">
                <!-- Dynamically injected by JS -->
            </div>
            
            <!-- Footer -->
            <div class="px-8 py-6 border-t flex items-center justify-between bg-emerald-50 rounded-b-3xl">
                <button onclick="closeModal()" 
                        class="px-8 py-3 text-gray-500 hover:text-gray-700 font-medium flex items-center gap-x-2 text-sm">
                    <i class="fa-solid fa-arrow-left"></i>
                    BACK TO PROGRAMS
                </button>
                
                <a onclick="handleJoinProgram()" 
                   class="inline-flex items-center px-9 py-4 bg-emerald-600 hover:bg-emerald-700 active:scale-95 text-white rounded-3xl font-semibold shadow-lg shadow-emerald-500/30">
                    JOIN THIS PROGRAM 
                    <i class="fa-solid fa-arrow-right ml-3"></i>
                </a>
            </div>
        </div>
    </div>

    <!-- GET INVOLVED & FOOTER (unchanged) -->
    <section id="get-involved" class="py-20 bg-gradient-to-br from-emerald-700 to-emerald-900 text-white">
        <div class="max-w-7xl mx-auto px-6 text-center">
            <h2 class="text-5xl font-semibold tracking-tight mb-6">Be part of the movement</h2>
            <p class="max-w-2xl mx-auto text-xl mb-12 text-emerald-200">
                Whether you volunteer, donate, partner, or simply spread the word — your support creates healthier communities in Zambia.
            </p>
            <div class="grid md:grid-cols-3 gap-8 max-w-4xl mx-auto">
                <div onclick="alert('Thank you! Volunteer form would open here.')" class="cursor-pointer bg-white/10 hover:bg-white/20 backdrop-blur-xl border border-white/30 rounded-3xl p-8 text-left">
                    <i class="fa-solid fa-hands-helping text-4xl mb-6"></i>
                    <h3 class="text-2xl font-semibold mb-2">Volunteer</h3>
                    <p class="text-emerald-100">Become a health educator, outreach worker, or event facilitator.</p>
                    <span class="text-xs uppercase tracking-widest mt-6 inline-block border border-white/50 rounded-3xl px-5 py-2">Join our team →</span>
                </div>
                <div onclick="alert('Thank you! Donation page would open here.')" class="cursor-pointer bg-white/10 hover:bg-white/20 backdrop-blur-xl border border-white/30 rounded-3xl p-8 text-left relative">
                    <div class="absolute -top-3 right-8 bg-amber-400 text-emerald-900 text-xs font-bold px-6 py-1 rounded-3xl">Most needed</div>
                    <i class="fa-solid fa-hand-holding-dollar text-4xl mb-6"></i>
                    <h3 class="text-2xl font-semibold mb-2">Donate</h3>
                    <p class="text-emerald-100">Help us reach the $500,000 inaugural goal and save lives.</p>
                    <span class="text-xs uppercase tracking-widest mt-6 inline-block border border-white/50 rounded-3xl px-5 py-2">Donate now →</span>
                </div>
                <div onclick="alert('Thank you! Partnership inquiry would open here.')" class="cursor-pointer bg-white/10 hover:bg-white/20 backdrop-blur-xl border border-white/30 rounded-3xl p-8 text-left">
                    <i class="fa-solid fa-link text-4xl mb-6"></i>
                    <h3 class="text-2xl font-semibold mb-2">Partner with us</h3>
                    <p class="text-emerald-100">Clinics, NGOs, schools, corporations — let’s collaborate for impact.</p>
                    <span class="text-xs uppercase tracking-widest mt-6 inline-block border border-white/50 rounded-3xl px-5 py-2">Become a partner →</span>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact" class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-6 grid md:grid-cols-12 gap-y-12">
            <div class="md:col-span-4">
                <div class="flex items-center gap-x-3 text-white mb-6">
                    <div class="w-9 h-9 bg-emerald-600 rounded-2xl flex items-center justify-center text-xl"><i class="fa-solid fa-heart-pulse"></i></div>
                    <span class="text-3xl font-semibold tracking-tighter">PHM</span>
                </div>
                <p class="text-sm leading-relaxed max-w-xs">
                    Pre-emptive Healthcare Movement<br>
                    Empowering Zambians to live healthier, longer lives.
                </p>
            </div>
            <div class="md:col-span-2">
                <div class="font-medium text-white mb-4">Quick Links</div>
                <div class="space-y-2 text-sm">
                    <a href="#about" class="block hover:text-white">About Us</a>
                    <a href="#programs" class="block hover:text-white">Interactive Programs</a>
                </div>
            </div>
            <div class="md:col-span-3">
                <div class="font-medium text-white mb-4">Contact Information</div>
                <div class="space-y-4 text-sm">
                    <div class="flex items-center gap-x-3">
                        <i class="fa-solid fa-envelope w-5"></i>
                        <a href="mailto:info@phmzambia.org" class="hover:text-white">info@phmzambia.org</a>
                    </div>
                    <div class="flex items-center gap-x-3">
                        <i class="fa-solid fa-phone w-5"></i>
                        <a href="tel:+260977123456" class="hover:text-white">+260 977 123 456</a>
                    </div>
                    <div class="flex items-center gap-x-3">
                        <i class="fa-solid fa-location-dot w-5"></i>
                        <div>Lusaka, Zambia</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="text-center text-[10px] mt-16 opacity-60">
            © 2025 Pre-emptive Healthcare Movement (PHM). All content taken directly from your official document.
        </div>
    </footer>

    <script>
        // Program data (unchanged)
        const programsData = [
            {
                id: 1, icon: "fa-solid fa-stethoscope", color: "text-emerald-600",
                title: "Health Screenings", shortDesc: "Free or low-cost screenings for blood pressure, cholesterol, glucose, dental, nutrition, and mental health.",
                fullDesc: "PHM offers accessible preventive care access through free or low-cost wellness checkups. In the first year alone we aim to reach 2,000 individuals in underserved communities. Early detection prevents complications from diabetes, hypertension, heart disease, and more.",
                level: "Secondary Prevention", impact: "2,000 screenings in Year 1",
                target: "Elderly, low-income families, rural communities",
                howToJoin: "Visit any of our mobile health units or partner clinics. No appointment needed for basic screenings.",
                metrics: "Reduces emergency visits by up to 40% (projected)"
            },
            {
                id: 2, icon: "fa-solid fa-chalkboard-teacher", color: "text-amber-600",
                title: "Educational Workshops", shortDesc: "Covering preventive healthcare, nutrition, physical activity, stress management, and smoking/alcohol cessation.",
                fullDesc: "We conduct hands-on workshops and counseling sessions to enhance health literacy. Target: educate at least 1,000 community members annually on lifestyle changes.",
                level: "Primary Prevention", impact: "60% of participants report behavior change within 6 months",
                target: "All ages, especially low-income families & youth",
                howToJoin: "Sign up for monthly workshops at community centers or join our online portal (coming soon).",
                metrics: "1,000+ community members educated yearly"
            },
            {
                id: 3, icon: "fa-solid fa-syringe", color: "text-red-600",
                title: "Vaccination Campaigns", shortDesc: "Rapid response to outbreaks and efforts to increase immunization rates in underserved areas.",
                fullDesc: "PHM organizes large-scale vaccination drives in response to cholera, tuberculosis, and other outbreaks. We also run routine immunization boosters for children and adults in rural and hard-to-reach areas.",
                level: "Primary Prevention", impact: "Hundreds vaccinated per campaign",
                target: "Rural communities & outbreak-prone areas",
                howToJoin: "Watch for our community alerts or visit vaccination pop-up sites announced on local radio and WhatsApp.",
                metrics: "Alerts issued for communicable disease outbreaks"
            },
            {
                id: 4, icon: "fa-solid fa-person-walking", color: "text-sky-600",
                title: "Fitness & Wellness Programs", shortDesc: "Walking groups, exercise classes, and creative workshops (art, music) to promote physical and emotional well-being.",
                fullDesc: "Regular walking clubs, group exercise sessions, and creative wellness activities (art therapy, music for mental health) help participants adopt healthy lifestyles and reduce stress.",
                level: "Primary & Tertiary Prevention", impact: "60% adopt healthier behaviors",
                target: "All ages, especially those with mental health risk factors",
                howToJoin: "Join any of our weekly walking groups or register for creative workshops at community venues.",
                metrics: "Promotes physical activity & stress management"
            },
            {
                id: 5, icon: "fa-solid fa-wheelchair-move", color: "text-purple-600",
                title: "Rehabilitation Services", shortDesc: "Tailored programs for chronic conditions and severe mental illness to improve quality of life.",
                fullDesc: "Specialized rehabilitation including physical therapy for stroke and heart conditions, plus support groups for individuals living with severe mental illness or disabilities.",
                level: "Tertiary Prevention", impact: "Improved quality of life for participants",
                target: "Elderly, handicapped, individuals prone to mental illness",
                howToJoin: "Referrals through partner clinics or direct contact with our rehabilitation team.",
                metrics: "Tailored support for stroke, heart conditions & mental illness"
            },
            {
                id: 6, icon: "fa-solid fa-house-medical", color: "text-teal-600",
                title: "Community Outreach", shortDesc: "Home visits, social media campaigns, and partnerships to engage underserved populations.",
                fullDesc: "We reach people where they are through home visits, translated materials, social media, and strong partnerships with local leaders, schools, and faith-based organizations.",
                level: "All Prevention Levels", impact: "Stronger community support network",
                target: "Rural communities, ethnic minorities, handicapped individuals",
                howToJoin: "Follow us on social media or speak to your local community leader to request an outreach visit.",
                metrics: "Home visits + partnerships with 10+ organizations"
            }
        ]

        function renderPrograms() {
            const container = document.getElementById('programs-grid')
            container.innerHTML = ''
            programsData.forEach(program => {
                const cardHTML = `
                <div onclick="showProgramModal(${program.id})" 
                     class="program-card bg-white/10 backdrop-blur-lg border border-white/20 hover:border-white/40 rounded-3xl p-8 card-hover text-white">
                    <div class="flex justify-between items-start mb-6">
                        <i class="${program.icon} ${program.color} text-5xl"></i>
                        <span class="text-xs font-medium bg-white/20 px-3 py-1 rounded-3xl">${program.level}</span>
                    </div>
                    <h4 class="text-2xl font-semibold mb-3">${program.title}</h4>
                    <p class="text-emerald-100 mb-8">${program.shortDesc}</p>
                    <div class="flex items-center justify-between text-sm">
                        <div class="flex items-center gap-x-2">
                            <i class="fa-solid fa-chart-bar"></i>
                            <span class="font-medium">${program.impact}</span>
                        </div>
                        <button class="text-emerald-300 hover:text-white text-xs flex items-center gap-x-1 font-medium">
                            EXPLORE 
                            <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>`
                container.innerHTML += cardHTML
            })
        }

        // Enhanced modal functions with smooth animations
        let currentModal = null

        function showProgramModal(id) {
            const program = programsData.find(p => p.id === id)
            if (!program) return

            currentModal = program

            const modal = document.getElementById('program-modal')
            const wrapper = document.getElementById('modal-content-wrapper')
            const titleEl = document.getElementById('modal-title')
            const iconEl = document.getElementById('modal-icon')
            const bodyEl = document.getElementById('modal-body')

            // Reset any previous exit animation
            wrapper.classList.remove('modal-exit')

            titleEl.textContent = program.title
            iconEl.innerHTML = `<i class="${program.icon} ${program.color}"></i>`

            bodyEl.innerHTML = `
            <div class="modal-content-inner">
                <p class="text-lg leading-relaxed text-gray-700">${program.fullDesc}</p>
                
                <div class="grid grid-cols-2 gap-6 mt-10">
                    <div class="bg-white rounded-2xl p-5 shadow-sm">
                        <h5 class="uppercase text-xs tracking-widest text-emerald-600 font-medium mb-1">Prevention Level</h5>
                        <p class="font-semibold text-xl">${program.level}</p>
                    </div>
                    <div class="bg-white rounded-2xl p-5 shadow-sm">
                        <h5 class="uppercase text-xs tracking-widest text-emerald-600 font-medium mb-1">Expected Impact</h5>
                        <p class="font-semibold text-xl">${program.impact}</p>
                    </div>
                    <div class="bg-white rounded-2xl p-5 shadow-sm">
                        <h5 class="uppercase text-xs tracking-widest text-emerald-600 font-medium mb-1">Target Audience</h5>
                        <p class="font-semibold text-xl">${program.target}</p>
                    </div>
                    <div class="bg-white rounded-2xl p-5 shadow-sm">
                        <h5 class="uppercase text-xs tracking-widest text-emerald-600 font-medium mb-1">Key Metric</h5>
                        <p class="font-semibold text-xl">${program.metrics}</p>
                    </div>
                </div>
                
                <div class="mt-10 bg-emerald-50 rounded-3xl p-7">
                    <h5 class="font-semibold mb-3 flex items-center gap-x-2 text-emerald-700"><i class="fa-solid fa-info-circle"></i> How to Participate Right Now</h5>
                    <p class="text-gray-700">${program.howToJoin}</p>
                </div>
                
                <div class="mt-8 flex items-center justify-center gap-x-8 text-xs text-gray-400">
                    <div class="flex items-center"><i class="fa-solid fa-calendar mr-1.5"></i> Ongoing throughout 2025</div>
                    <div class="flex items-center"><i class="fa-solid fa-map-marker-alt mr-1.5"></i> Lusaka &amp; all rural provinces</div>
                </div>
            </div>`

            // Show modal with animation
            modal.classList.remove('hidden')
            modal.classList.add('flex')
            
            // Prevent background scroll
            document.body.style.overflow = 'hidden'
        }

        function closeModal() {
            const modal = document.getElementById('program-modal')
            const wrapper = document.getElementById('modal-content-wrapper')
            
            // Trigger exit animation
            wrapper.classList.add('modal-exit')
            
            // Re-enable scroll and hide after animation finishes
            setTimeout(() => {
                modal.classList.add('hidden')
                modal.classList.remove('flex')
                wrapper.classList.remove('modal-exit')
                document.body.style.overflow = 'visible'
                currentModal = null
            }, 320)
        }

        function handleJoinProgram() {
            if (!currentModal) return
            closeModal()
            setTimeout(() => {
                alert(`🎉 You have successfully joined the **${currentModal.title}** program!\n\nA confirmation has been sent to your email (demo). You will be notified of the next session in your area.`)
            }, 450)
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu')
            const icon = document.getElementById('mobile-icon')
            menu.classList.toggle('hidden')
            icon.classList.toggle('fa-bars')
            icon.classList.toggle('fa-xmark')
        }

        // Keyboard support: press ESC to close modal
        document.addEventListener('keydown', function(e) {
            if (e.key === "Escape") {
                const modal = document.getElementById('program-modal')
                if (modal && modal.classList.contains('flex')) {
                    closeModal()
                }
            }
        })

        // Initialize
        window.onload = function() {
            renderPrograms()
            console.log('%c✅ PHM Website with Enhanced Modal Animations Loaded! ✨\n• Bouncy slide-up entrance\n• Smooth slide-down exit\n• Backdrop fade\n• ESC key support\n• Content stagger', 'color:#10b981; font-size:14px; font-weight:700')
        }
    </script>
</body>
</html>
