<!DOCTYPE html>
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Babu Ram Sharma (CHITASTAR59) - Cyber Profile Interface</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        cyber: {
                            bg: '#07090e',
                            darkCard: '#0d1117',
                            card: 'rgba(18, 24, 38, 0.75)',
                            border: '#21262d',
                            borderGlow: 'rgba(255, 0, 85, 0.4)',
                            text: '#c9d1d9',
                            muted: '#8b949e',
                            red: '#ff0055',
                            pink: '#ff007f',
                            cyan: '#00f3ff',
                            purple: '#9d00ff',
                            green: '#00ff66',
                            yellow: '#ffcc00'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        mono: ['Fira Code', 'monospace'],
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'glow-spin': 'spin 10s linear infinite',
                        'float': 'float 4s ease-in-out infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-6px)' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #07090e;
            color: #c9d1d9;
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
        }

        .cyber-font {
            font-family: 'Fira Code', monospace;
        }

        /* Scanline Overlay Effect */
        .scanline-overlay {
            background: linear-gradient(
                rgba(18, 16, 16, 0) 50%, 
                rgba(0, 0, 0, 0.35) 50%
            ), linear-gradient(
                90deg,
                rgba(255, 0, 0, 0.03),
                rgba(0, 255, 0, 0.01),
                rgba(0, 0, 255, 0.03)
            );
            background-size: 100% 3px, 6px 100%;
            pointer-events: none;
        }

        /* Glassmorphism Cards */
        .glass-panel {
            background: rgba(13, 17, 23, 0.75);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(48, 54, 61, 0.8);
        }

        .glass-panel-glow {
            background: rgba(16, 22, 34, 0.8);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 0, 85, 0.3);
            box-shadow: 0 0 15px rgba(255, 0, 85, 0.15), inset 0 0 15px rgba(255, 0, 85, 0.05);
        }

        .neon-border-cyan {
            border: 1px solid rgba(0, 243, 255, 0.4);
            box-shadow: 0 0 12px rgba(0, 243, 255, 0.2);
        }

        .neon-border-purple {
            border: 1px solid rgba(157, 0, 255, 0.4);
            box-shadow: 0 0 12px rgba(157, 0, 255, 0.2);
        }

        .glow-hover {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .glow-hover:hover {
            transform: translateY(-3px);
            border-color: rgba(255, 0, 85, 0.7);
            box-shadow: 0 8px 25px rgba(255, 0, 85, 0.25);
        }

        .avatar-glow-ring {
            background: linear-gradient(135deg, #ff0055, #00f3ff, #9d00ff, #ff0055);
            background-size: 300% 300%;
            animation: glowGradient 6s ease infinite;
            padding: 3px;
        }

        @keyframes glowGradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Tooltip Style */
        [data-tooltip] {
            position: relative;
        }
        [data-tooltip]:before {
            content: attr(data-tooltip);
            position: absolute;
            bottom: 125%;
            left: 50%;
            transform: translateX(-50%);
            padding: 4px 8px;
            background-color: #0d1117;
            color: #00f3ff;
            border: 1px solid #00f3ff;
            border-radius: 4px;
            font-size: 10px;
            font-family: 'Fira Code', monospace;
            white-space: nowrap;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.2s ease-in-out;
            z-index: 50;
            box-shadow: 0 0 10px rgba(0, 243, 255, 0.3);
        }
        [data-tooltip]:hover:before {
            opacity: 1;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #07090e;
        }
        ::-webkit-scrollbar-thumb {
            background: #21262d;
            border-radius: 3px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #ff0055;
        }

        /* Custom Heatmap Colors */
        .contrib-0 { background-color: #161b22; }
        .contrib-1 { background-color: #0e4429; }
        .contrib-2 { background-color: #006d32; }
        .contrib-3 { background-color: #26a641; }
        .contrib-4 { background-color: #39d353; box-shadow: 0 0 6px #39d353; }
    </style>
</head>
<body class="min-h-screen flex flex-col bg-[#07090e] text-[#c9d1d9] antialiased relative selection:bg-red-500 selection:text-white">

    <!-- SCANLINE OVERLAY TOGGLEABLE CONTAINER -->
    <div id="scanlineEffect" class="scanline-overlay fixed inset-0 z-40"></div>

    <!-- TOP CONTROL FLOATING SUITE -->
    <div class="fixed bottom-6 right-6 z-50 flex flex-col sm:flex-row items-end sm:items-center space-y-2 sm:space-y-0 sm:space-x-3">
        
        <!-- SCANLINE TOGGLE BUTTON -->
        <button onclick="toggleScanline()" class="bg-[#0d1117]/90 hover:bg-[#161b22] text-cyan-400 border border-cyan-500/50 rounded-full p-3 shadow-[0_0_15px_rgba(0,243,255,0.3)] transition transform hover:scale-110" title="Toggle Scanlines">
            <i class="fa-solid fa-tv text-base"></i>
        </button>

        <!-- TERMINAL TRIGGER BUTTON -->
        <button onclick="toggleTerminal()" class="bg-[#0d1117]/90 hover:bg-[#161b22] text-green-400 border border-green-500/50 rounded-full p-3 shadow-[0_0_15px_rgba(0,255,102,0.3)] transition transform hover:scale-110" title="Launch Cyber Terminal">
            <i class="fa-solid fa-terminal text-base"></i>
        </button>

        <!-- FLOATING EDIT DRAWER TRIGGER -->
        <button onclick="toggleEditor()" class="bg-gradient-to-r from-red-600 via-pink-600 to-purple-600 hover:from-red-500 hover:to-purple-500 text-white font-bold py-3 px-5 rounded-full shadow-[0_0_20px_rgba(255,0,85,0.6)] flex items-center space-x-2 transition transform hover:scale-105 border border-pink-400/60">
            <i class="fa-solid fa-sliders text-base"></i>
            <span class="cyber-font text-xs tracking-wider">CUSTOMIZE PROFILE</span>
        </button>
    </div>


    <!-- FLOATING LIVE PROFILE CONFIG DRAWER -->
    <div id="editorDrawer" class="fixed inset-y-0 right-0 w-full max-w-xl bg-[#0d1117] border-l border-[#30363d] z-50 transform translate-x-full transition-transform duration-300 ease-in-out shadow-2xl flex flex-col">
        <div class="p-4 border-b border-[#30363d] flex items-center justify-between bg-[#07090e]">
            <div class="flex items-center space-x-2 text-red-500">
                <i class="fa-solid fa-user-gear text-lg"></i>
                <h2 class="text-sm font-bold text-white cyber-font">PROFILE CONFIG ENGINE</h2>
            </div>
            <div class="flex items-center space-x-2">
                <button onclick="exportHTML()" class="bg-cyan-600 hover:bg-cyan-500 text-white text-xs px-3 py-1.5 rounded flex items-center space-x-1 font-mono transition">
                    <i class="fa-solid fa-download"></i>
                    <span>Export HTML</span>
                </button>
                <button onclick="toggleEditor()" class="text-gray-400 hover:text-white text-lg p-1">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>
        </div>

        <!-- Scrollable Form Controls -->
        <div class="p-5 space-y-5 overflow-y-auto flex-grow text-xs cyber-font">
            
            <!-- User Basic Identity -->
            <div class="space-y-3 bg-[#161b22] p-4 rounded-lg border border-[#30363d]">
                <h3 class="text-xs font-bold text-red-400 uppercase tracking-widest flex items-center space-x-1">
                    <i class="fa-solid fa-id-card"></i>
                    <span>1. Personal Identity</span>
                </h3>
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-gray-400 mb-1">Full Name</label>
                        <input type="text" id="input-name" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-red-500 focus:outline-none" oninput="updateProfile()">
                    </div>
                    <div>
                        <label class="block text-gray-400 mb-1">Username</label>
                        <input type="text" id="input-username" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-red-500 focus:outline-none" oninput="updateProfile()">
                    </div>
                </div>
                <div>
                    <label class="block text-gray-400 mb-1">Role / Subtitle</label>
                    <input type="text" id="input-tagline" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-red-500 focus:outline-none" oninput="updateProfile()">
                </div>
                <div>
                    <label class="block text-gray-400 mb-1">Avatar Image URL</label>
                    <input type="text" id="input-avatar" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-red-500 focus:outline-none" oninput="updateProfile()">
                </div>
            </div>

            <!-- Banner Setup -->
            <div class="space-y-3 bg-[#161b22] p-4 rounded-lg border border-[#30363d]">
                <h3 class="text-xs font-bold text-pink-400 uppercase tracking-widest flex items-center space-x-1">
                    <i class="fa-solid fa-flag"></i>
                    <span>2. Banner Customization</span>
                </h3>
                <div>
                    <label class="block text-gray-400 mb-1">Main Banner Title</label>
                    <input type="text" id="input-banner-title" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-pink-500 focus:outline-none" oninput="updateProfile()">
                </div>
                <div>
                    <label class="block text-gray-400 mb-1">Sub Title</label>
                    <input type="text" id="input-banner-sub" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-pink-500 focus:outline-none" oninput="updateProfile()">
                </div>
                <div>
                    <label class="block text-gray-400 mb-1">Domain Focus String</label>
                    <input type="text" id="input-banner-domains" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-pink-500 focus:outline-none" oninput="updateProfile()">
                </div>
            </div>

            <!-- Contacts & Social Links -->
            <div class="space-y-3 bg-[#161b22] p-4 rounded-lg border border-[#30363d]">
                <h3 class="text-xs font-bold text-cyan-400 uppercase tracking-widest flex items-center space-x-1">
                    <i class="fa-solid fa-share-nodes"></i>
                    <span>3. Socials & Connect</span>
                </h3>
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-gray-400 mb-1">Location</label>
                        <input type="text" id="input-location" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-cyan-500 focus:outline-none" oninput="updateProfile()">
                    </div>
                    <div>
                        <label class="block text-gray-400 mb-1">Email</label>
                        <input type="text" id="input-email" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-cyan-500 focus:outline-none" oninput="updateProfile()">
                    </div>
                </div>
                <div>
                    <label class="block text-gray-400 mb-1">Website URL</label>
                    <input type="text" id="input-website" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-cyan-500 focus:outline-none" oninput="updateProfile()">
                </div>
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-gray-400 mb-1">LinkedIn URL</label>
                        <input type="text" id="input-linkedin" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-cyan-500 focus:outline-none" oninput="updateProfile()">
                    </div>
                    <div>
                        <label class="block text-gray-400 mb-1">Twitter / X Handle / URL</label>
                        <input type="text" id="input-twitter" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-cyan-500 focus:outline-none" oninput="updateProfile()">
                    </div>
                </div>
            </div>

            <!-- Bio & Stats -->
            <div class="space-y-3 bg-[#161b22] p-4 rounded-lg border border-[#30363d]">
                <h3 class="text-xs font-bold text-purple-400 uppercase tracking-widest flex items-center space-x-1">
                    <i class="fa-solid fa-chart-pie"></i>
                    <span>4. Stats & Bio</span>
                </h3>
                <div>
                    <label class="block text-gray-400 mb-1">README Bio Intro</label>
                    <textarea id="input-readme-bio" rows="3" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-purple-500 focus:outline-none" oninput="updateProfile()"></textarea>
                </div>
                <div>
                    <label class="block text-gray-400 mb-1">Skill Pill Badges (Comma Separated)</label>
                    <input type="text" id="input-pills" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white focus:border-purple-500 focus:outline-none" oninput="updateProfile()">
                </div>
                <div class="grid grid-cols-3 gap-2">
                    <div>
                        <label class="block text-gray-400 mb-1">Contribs</label>
                        <input type="number" id="input-total-contrib" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white" oninput="updateProfile()">
                    </div>
                    <div>
                        <label class="block text-gray-400 mb-1">Current Streak</label>
                        <input type="number" id="input-current-streak" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white" oninput="updateProfile()">
                    </div>
                    <div>
                        <label class="block text-gray-400 mb-1">Longest Streak</label>
                        <input type="number" id="input-longest-streak" class="w-full bg-[#0d1117] border border-[#30363d] rounded p-2 text-white" oninput="updateProfile()">
                    </div>
                </div>
            </div>

        </div>
    </div>


    <!-- INTERACTIVE CYBER TERMINAL MODAL -->
    <div id="terminalModal" class="fixed inset-0 bg-black/80 backdrop-blur-md z-50 hidden flex items-center justify-center p-4">
        <div class="bg-[#0d1117] border border-green-500/50 rounded-xl w-full max-w-2xl h-[450px] flex flex-col shadow-[0_0_30px_rgba(0,255,102,0.2)] overflow-hidden">
            <!-- Terminal Titlebar -->
            <div class="bg-[#161b22] px-4 py-2 border-b border-[#30363d] flex items-center justify-between">
                <div class="flex items-center space-x-2">
                    <span class="w-3 h-3 rounded-full bg-red-500 cursor-pointer" onclick="toggleTerminal()"></span>
                    <span class="w-3 h-3 rounded-full bg-yellow-500"></span>
                    <span class="w-3 h-3 rounded-full bg-green-500"></span>
                    <span class="cyber-font text-xs text-gray-300 ml-2">bash - chitastar59@hackerai:~$</span>
                </div>
                <button onclick="toggleTerminal()" class="text-gray-400 hover:text-white"><i class="fa-solid fa-xmark"></i></button>
            </div>
            <!-- Terminal Output Area -->
            <div id="terminalOutput" class="p-4 flex-grow overflow-y-auto cyber-font text-xs space-y-2 text-green-400">
                <p class="text-gray-400">CHITASTAR Cyber Security Shell v2.5.0-release</p>
                <p class="text-gray-400">Type <span class="text-cyan-400 font-bold">'help'</span> for a list of available system commands.</p>
                <p>--------------------------------------------------</p>
            </div>
            <!-- Terminal Input Row -->
            <div class="p-3 bg-[#07090e] border-t border-[#30363d] flex items-center space-x-2 cyber-font text-xs">
                <span class="text-pink-500 font-bold">&gt;_</span>
                <input type="text" id="terminalInput" placeholder="Type a command (e.g. whoami, skills, contact)..." class="bg-transparent text-cyan-300 w-full focus:outline-none" onkeydown="handleTerminalCommand(event)">
            </div>
        </div>
    </div>


    <!-- TOP GITHUB STANDARD NAV BAR -->
    <header class="bg-[#0d1117] border-b border-[#21262d] px-4 py-2.5 flex items-center justify-between text-sm sticky top-0 z-30 backdrop-blur-md bg-opacity-90">
        <div class="flex items-center space-x-4">
            <a href="#" class="text-white hover:text-red-500 transition">
                <i class="fa-brands fa-github text-3xl"></i>
            </a>
            <nav class="hidden md:flex space-x-4 text-xs font-semibold text-gray-300">
                <a href="#" class="hover:text-red-400 transition">Product <i class="fa-solid fa-chevron-down text-[10px]"></i></a>
                <a href="#" class="hover:text-red-400 transition">Solutions <i class="fa-solid fa-chevron-down text-[10px]"></i></a>
                <a href="#" class="hover:text-red-400 transition">Resources <i class="fa-solid fa-chevron-down text-[10px]"></i></a>
                <a href="#" class="hover:text-red-400 transition">Open Source <i class="fa-solid fa-chevron-down text-[10px]"></i></a>
                <a href="#" class="hover:text-red-400 transition">Enterprise <i class="fa-solid fa-chevron-down text-[10px]"></i></a>
                <a href="#" class="hover:text-red-400 transition">Pricing</a>
            </nav>
        </div>

        <div class="flex items-center space-x-3">
            <div class="relative hidden sm:block">
                <input type="text" placeholder="Search or jump to..." class="bg-[#161b22] text-xs text-gray-300 border border-[#30363d] rounded-md py-1.5 px-3 pr-8 w-60 focus:outline-none focus:border-cyan-500 transition">
                <span class="absolute right-2 top-1.5 text-[10px] bg-[#21262d] border border-[#30363d] px-1.5 rounded text-gray-400 font-mono">/</span>
            </div>
            <button class="text-gray-300 hover:text-cyan-400 p-1"><i class="fa-regular fa-bell"></i></button>
            <button class="text-gray-300 hover:text-cyan-400 flex items-center space-x-1 p-1">
                <i class="fa-solid fa-plus text-xs"></i>
                <i class="fa-solid fa-caret-down text-[10px]"></i>
            </button>
            <img id="nav-avatar" src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=200" alt="Avatar" class="w-7 h-7 rounded-full border border-cyan-500/60 object-cover">
        </div>
    </header>


    <!-- MATRIX ANIMATED HEADER BANNER -->
    <div class="relative bg-[#07090e] border-b border-[#30363d] overflow-hidden min-h-[190px] flex items-center">
        <!-- Digital Rain Canvas -->
        <canvas id="matrixCanvas" class="absolute inset-0 z-0 opacity-25 pointer-events-none"></canvas>
        
        <!-- Glowing Gradient Background Overlay -->
        <div class="absolute inset-0 bg-radial-gradient from-red-600/10 via-purple-600/10 to-transparent pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 py-6 w-full relative z-10 flex flex-col md:flex-row items-center justify-between gap-6">
            
            <!-- Left Matrix Code Stream -->
            <div class="cyber-font text-[11px] text-cyan-400/80 space-y-1 hidden xl:block border-l-2 border-red-500 pl-3">
                <p><span class="text-pink-500">$</span> whoami</p>
                <p class="text-white font-bold">Babu Ram Sharma</p>
                <p><span class="text-pink-500">$</span> identity</p>
                <p class="text-yellow-400">&gt; CHITASTAR59</p>
                <p><span class="text-pink-500">$</span> status</p>
                <p class="text-green-400">&gt; SECURE_ONLINE</p>
            </div>

            <!-- Banner Center Graphic Title -->
            <div class="text-center">
                <div class="inline-flex items-center space-x-2 text-[10px] sm:text-xs font-mono tracking-widest text-red-500 uppercase mb-1">
                    <span>ANALYZE</span> <i class="fa-solid fa-angle-right text-pink-500"></i>
                    <span>EXPLOIT</span> <i class="fa-solid fa-angle-right text-pink-500"></i>
                    <span>SECURE</span> <i class="fa-solid fa-angle-right text-pink-500"></i>
                    <span>REPEAT</span>
                </div>
                <h1 id="display-banner-title" class="text-4xl sm:text-6xl font-black tracking-widest text-transparent bg-clip-text bg-gradient-to-r from-red-500 via-pink-500 to-purple-500 cyber-font drop-shadow-[0_0_20px_rgba(255,0,85,0.8)]">
                    CHITASTAR
                </h1>
                <p id="display-banner-sub" class="text-xs sm:text-sm font-extrabold tracking-widest text-gray-200 uppercase mt-1">
                    CYBERSECURITY RESEARCHER
                </p>
                <p id="display-banner-domains" class="text-[10px] sm:text-xs font-mono tracking-wider text-cyan-400 mt-2 bg-[#0d1117]/80 px-3 py-1 rounded-full border border-cyan-500/30 inline-block shadow-[0_0_10px_rgba(0,243,255,0.2)]">
                    WEB / API / APPLICATION SECURITY / VULNERABILITY RESEARCH
                </p>
            </div>

            <!-- Right Visual Orb & Tagline -->
            <div class="flex items-center space-x-5">
                <div class="text-right hidden sm:block cyber-font text-xs">
                    <p class="font-bold text-gray-300">BETTER</p>
                    <p class="font-bold text-red-500 drop-shadow-[0_0_8px_#ff0055]">SECURITY</p>
                    <p class="font-bold text-gray-300">THROUGH</p>
                    <p class="font-bold text-cyan-400 drop-shadow-[0_0_8px_#00f3ff]">DEEPER</p>
                    <p class="font-bold text-purple-400">UNDERSTANDING</p>
                </div>

                <!-- Interactive Rotating Orb Visual -->
                <div class="relative w-20 h-20 flex items-center justify-center">
                    <div class="absolute inset-0 rounded-full border border-red-500/40 animate-ping opacity-25"></div>
                    <div class="w-16 h-16 rounded-full border-2 border-cyan-400/80 border-dashed animate-spin flex items-center justify-center shadow-[0_0_15px_rgba(0,243,255,0.4)]" style="animation-duration: 10s;">
                        <i class="fa-solid fa-shield-halved text-2xl text-red-500 drop-shadow-[0_0_10px_#ff0055]"></i>
                    </div>
                </div>
            </div>

        </div>
    </div>


    <!-- MAIN STICKY NAVIGATION TABS BAR -->
    <div class="bg-[#0d1117] border-b border-[#21262d] sticky top-[53px] z-20 backdrop-blur-md bg-opacity-95">
        <div class="max-w-7xl mx-auto px-4 flex space-x-2 sm:space-x-6 overflow-x-auto text-sm">
            <button onclick="switchTab('overview')" id="tab-overview" class="tab-btn py-3 px-3 flex items-center space-x-2 border-b-2 border-red-500 font-bold text-white whitespace-nowrap transition">
                <i class="fa-regular fa-bookmark text-red-400"></i>
                <span>Overview</span>
            </button>
            <button onclick="switchTab('repositories')" id="tab-repositories" class="tab-btn py-3 px-3 flex items-center space-x-2 border-b-2 border-transparent font-medium text-gray-400 hover:text-cyan-300 whitespace-nowrap transition">
                <i class="fa-regular fa-folder-closed"></i>
                <span>Repositories</span>
                <span class="bg-[#21262d] text-xs text-cyan-400 px-2 py-0.5 rounded-full font-mono border border-cyan-500/30">22</span>
            </button>
            <button onclick="switchTab('projects')" id="tab-projects" class="tab-btn py-3 px-3 flex items-center space-x-2 border-b-2 border-transparent font-medium text-gray-400 hover:text-cyan-300 whitespace-nowrap transition">
                <i class="fa-solid fa-table-cells-large"></i>
                <span>Projects</span>
            </button>
            <button onclick="switchTab('packages')" id="tab-packages" class="tab-btn py-3 px-3 flex items-center space-x-2 border-b-2 border-transparent font-medium text-gray-400 hover:text-cyan-300 whitespace-nowrap transition">
                <i class="fa-solid fa-cube"></i>
                <span>Packages</span>
            </button>
            <button onclick="switchTab('stars')" id="tab-stars" class="tab-btn py-3 px-3 flex items-center space-x-2 border-b-2 border-transparent font-medium text-gray-400 hover:text-cyan-300 whitespace-nowrap transition">
                <i class="fa-regular fa-star"></i>
                <span>Stars</span>
            </button>
        </div>
    </div>


    <!-- MAIN CONTAINER AREA -->
    <main class="max-w-7xl mx-auto px-4 py-8 flex-grow w-full relative z-10">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">

            <!-- LEFT PROFILE SIDEBAR (3 COLS) -->
            <div class="lg:col-span-3 space-y-6">
                
                <!-- Avatar & Identifiers -->
                <div class="flex flex-row lg:flex-col items-center lg:items-start space-x-5 lg:space-x-0 space-y-0 lg:space-y-4">
                    <div class="relative group">
                        <div class="avatar-glow-ring rounded-full w-32 h-32 sm:w-40 sm:h-40 lg:w-48 lg:h-48 flex items-center justify-center shadow-[0_0_25px_rgba(255,0,85,0.4)]">
                            <img id="display-avatar" src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=400" alt="Avatar" class="rounded-full w-full h-full object-cover border-4 border-[#07090e]">
                        </div>
                        <div class="absolute bottom-2 right-2 bg-[#0d1117] border border-cyan-500 rounded-full p-2 text-xs text-cyan-400 shadow-[0_0_10px_rgba(0,243,255,0.5)]">
                            <i class="fa-solid fa-user-ninja"></i>
                        </div>
                    </div>

                    <div class="pt-2">
                        <div class="flex items-center space-x-2">
                            <h1 id="display-name" class="text-2xl font-black text-white tracking-wide">Babu Ram Sharma</h1>
                            <i class="fa-solid fa-circle-check text-cyan-400 text-base drop-shadow-[0_0_8px_#00f3ff]" title="Verified Cybersecurity Researcher"></i>
                        </div>
                        <h2 id="display-username" class="text-red-400 text-sm font-mono font-bold">CHITASTAR59</h2>
                    </div>
                </div>

                <!-- Tagline / Bio -->
                <p id="display-tagline" class="text-xs sm:text-sm text-gray-300 leading-relaxed font-sans border-l-2 border-red-500/80 pl-3">
                    Cybersecurity Researcher | Web & API Security | Application Security | Red Teaming | Bug Bounty Hunter | Vulnerability Research
                </p>

                <!-- Edit Profile Button -->
                <button onclick="toggleEditor()" class="w-full bg-[#161b22] hover:bg-[#21262d] border border-red-500/40 hover:border-red-500 text-gray-200 text-xs font-semibold py-2 px-3 rounded-md transition shadow-[0_0_10px_rgba(255,0,85,0.15)] flex items-center justify-center space-x-2">
                    <i class="fa-solid fa-pen-to-square text-red-400"></i>
                    <span>Edit Profile Configuration</span>
                </button>

                <!-- Followers Stats -->
                <div class="flex items-center space-x-4 text-xs text-gray-400 border-t border-[#21262d] pt-3">
                    <a href="#" class="hover:text-cyan-400 flex items-center space-x-1">
                        <i class="fa-solid fa-users text-gray-500"></i>
                        <span id="display-followers" class="font-bold text-white">4</span>
                        <span>followers</span>
                    </a>
                    <span>·</span>
                    <a href="#" class="hover:text-cyan-400 flex items-center space-x-1">
                        <span id="display-following" class="font-bold text-white">0</span>
                        <span>following</span>
                    </a>
                </div>

                <!-- Direct Contact Details -->
                <div class="space-y-2.5 text-xs text-gray-300 border-t border-[#21262d] pt-4 font-mono">
                    <div class="flex items-center space-x-2.5">
                        <i class="fa-solid fa-location-dot text-red-400 w-4"></i>
                        <span id="display-location">Dallas, Texas</span>
                    </div>
                    <div class="flex items-center space-x-2.5 truncate">
                        <i class="fa-solid fa-envelope text-pink-400 w-4"></i>
                        <a id="display-email-link" href="mailto:baburamsharma658@gmail.com" class="hover:underline text-cyan-400 truncate"><span id="display-email">baburamsharma658@gmail.com</span></a>
                    </div>
                    <div class="flex items-center space-x-2.5 truncate">
                        <i class="fa-solid fa-globe text-green-400 w-4"></i>
                        <a id="display-website-link" href="https://hackerai.oi" target="_blank" class="hover:underline text-cyan-400 truncate"><span id="display-website">hackerai.oi</span></a>
                    </div>
                </div>

                <!-- Achievements Holographic Hexagon Badges -->
                <div class="border-t border-[#21262d] pt-4 space-y-3">
                    <h3 class="text-xs font-bold text-gray-300 uppercase tracking-widest cyber-font">Achievements</h3>
                    <div class="grid grid-cols-4 gap-2">
                        <div class="flex flex-col items-center group cursor-pointer" data-tooltip="Security Master">
                            <div class="w-11 h-11 bg-[#161b22] border border-red-500/60 rounded-xl flex items-center justify-center text-red-500 group-hover:scale-110 transition shadow-[0_0_12px_rgba(255,0,85,0.4)]">
                                <i class="fa-solid fa-shield-halved text-lg"></i>
                            </div>
                            <span class="text-[9px] text-gray-400 mt-1 font-mono">Security</span>
                        </div>
                        <div class="flex flex-col items-center group cursor-pointer" data-tooltip="Vulnerability Researcher">
                            <div class="w-11 h-11 bg-[#161b22] border border-purple-500/60 rounded-xl flex items-center justify-center text-purple-400 group-hover:scale-110 transition shadow-[0_0_12px_rgba(157,0,255,0.4)]">
                                <i class="fa-solid fa-bug text-lg"></i>
                            </div>
                            <span class="text-[9px] text-gray-400 mt-1 font-mono">Research</span>
                        </div>
                        <div class="flex flex-col items-center group cursor-pointer" data-tooltip="Open Source Security">
                            <div class="w-11 h-11 bg-[#161b22] border border-cyan-500/60 rounded-xl flex items-center justify-center text-cyan-400 group-hover:scale-110 transition shadow-[0_0_12px_rgba(0,243,255,0.4)]">
                                <i class="fa-solid fa-code text-lg"></i>
                            </div>
                            <span class="text-[9px] text-gray-400 mt-1 font-mono">OpenSrc</span>
                        </div>
                        <div class="flex flex-col items-center group cursor-pointer" data-tooltip="System Builder">
                            <div class="w-11 h-11 bg-[#161b22] border border-yellow-500/60 rounded-xl flex items-center justify-center text-yellow-400 group-hover:scale-110 transition shadow-[0_0_12px_rgba(255,204,0,0.4)]">
                                <i class="fa-solid fa-terminal text-lg"></i>
                            </div>
                            <span class="text-[9px] text-gray-400 mt-1 font-mono">Builder</span>
                        </div>
                    </div>
                </div>

                <!-- Quote Cyber Box -->
                <div class="glass-panel-glow rounded-lg p-3 text-xs cyber-font relative overflow-hidden">
                    <p class="text-gray-200 leading-relaxed">
                        <span class="text-red-500 font-bold">&gt;</span> "<span id="display-quote">Security is not a product, it's a process.</span>"
                    </p>
                    <p class="text-right text-gray-400 text-[10px] mt-2 font-mono">- Unknown</p>
                </div>

                <!-- REAL-TIME CONNECT SOCIALS -->
                <div class="border-t border-[#21262d] pt-4 space-y-3">
                    <h3 class="text-xs font-bold text-gray-300 uppercase tracking-widest cyber-font">Direct Connect</h3>
                    <div class="grid grid-cols-2 gap-2 text-xs font-mono">
                        <a id="connect-linkedin" href="https://www.linkedin.com/in/babu-ram-sharma-482527350/" target="_blank" class="flex items-center space-x-2 text-gray-300 hover:text-cyan-400 bg-[#161b22] border border-[#30363d] hover:border-cyan-500 p-2 rounded transition shadow">
                            <i class="fa-brands fa-linkedin text-blue-400 text-sm"></i>
                            <span class="truncate">LinkedIn</span>
                        </a>
                        <a id="connect-twitter" href="https://x.com/CHITASTAR59" target="_blank" class="flex items-center space-x-2 text-gray-300 hover:text-cyan-400 bg-[#161b22] border border-[#30363d] hover:border-cyan-500 p-2 rounded transition shadow">
                            <i class="fa-brands fa-x-twitter text-white text-sm"></i>
                            <span class="truncate">X / Twitter</span>
                        </a>
                        <a id="connect-email" href="mailto:baburamsharma658@gmail.com" class="flex items-center space-x-2 text-gray-300 hover:text-cyan-400 bg-[#161b22] border border-[#30363d] hover:border-cyan-500 p-2 rounded transition shadow">
                            <i class="fa-regular fa-envelope text-red-400 text-sm"></i>
                            <span class="truncate">Email</span>
                        </a>
                        <a id="connect-website" href="https://hackerai.oi" target="_blank" class="flex items-center space-x-2 text-gray-300 hover:text-cyan-400 bg-[#161b22] border border-[#30363d] hover:border-cyan-500 p-2 rounded transition shadow">
                            <i class="fa-solid fa-globe text-green-400 text-sm"></i>
                            <span class="truncate">Website</span>
                        </a>
                    </div>
                </div>

            </div>


            <!-- RIGHT MAIN TAB CONTENT (9 COLS) -->
            <div id="tab-content" class="lg:col-span-9 space-y-6">

                <!-- OVERVIEW TAB -->
                <div id="overview-content" class="space-y-6">
                    
                    <!-- README.md Cyber Box -->
                    <div class="glass-panel border border-[#30363d] rounded-xl p-6 relative overflow-hidden shadow-2xl">
                        <div class="flex items-center justify-between border-b border-[#30363d] pb-3 mb-4">
                            <div class="flex items-center space-x-2 text-xs text-gray-400 cyber-font">
                                <i class="fa-regular fa-file-code text-red-500 text-sm"></i>
                                <span class="font-bold text-gray-200"><span id="readme-username">CHITASTAR59</span> / README.md</span>
                            </div>
                            <span class="text-[10px] text-cyan-400 cyber-font bg-[#161b22] px-2 py-0.5 rounded border border-cyan-500/30">markdown</span>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 items-center">
                            <div class="md:col-span-2 space-y-3">
                                <div class="flex items-center space-x-2">
                                    <i class="fa-solid fa-rocket text-red-500 text-lg"></i>
                                    <h2 class="text-xl sm:text-2xl font-bold text-white tracking-wide">Hi there, I'm <span id="readme-name">Babu Ram Sharma</span> 👋</h2>
                                </div>
                                <div id="display-readme-bio" class="text-xs sm:text-sm text-gray-300 leading-relaxed space-y-2">
                                    <p>I'm a cybersecurity researcher focused on offensive security and application security.</p>
                                    <p class="text-gray-400">I enjoy finding and understanding security weaknesses in web applications, APIs, cloud infrastructure, and modern web technologies.</p>
                                </div>

                                <!-- Dynamic Skill Badges Pills -->
                                <div id="display-pills-container" class="flex flex-wrap gap-2 pt-2">
                                    <!-- Populated dynamically via JavaScript -->
                                </div>
                            </div>

                            <!-- Threat Matrix Status Box -->
                            <div class="glass-panel-glow rounded-lg p-4 cyber-font text-xs space-y-2 text-center md:text-left">
                                <p class="text-red-500 font-bold tracking-widest text-xs flex items-center justify-between">
                                    <span>DETECT</span> <i class="fa-solid fa-radar text-[10px]"></i>
                                </p>
                                <p class="text-pink-500 font-bold tracking-widest text-xs flex items-center justify-between">
                                    <span>ANALYZE</span> <i class="fa-solid fa-magnifying-glass text-[10px]"></i>
                                </p>
                                <p class="text-cyan-400 font-bold tracking-widest text-xs flex items-center justify-between">
                                    <span>EXPLOIT</span> <i class="fa-solid fa-bolt text-[10px]"></i>
                                </p>
                                <p class="text-purple-400 font-bold tracking-widest text-xs flex items-center justify-between">
                                    <span>REMEDIATE</span> <i class="fa-solid fa-shield text-[10px]"></i>
                                </p>
                                <div class="pt-2 border-t border-red-500/30 flex items-center justify-between text-[10px]">
                                    <span class="text-gray-400">STATUS:</span>
                                    <span class="text-green-400 font-bold animate-pulse">&gt;_ [PROTECTED]</span>
                                </div>
                            </div>
                        </div>
                    </div>


                    <!-- TWO COLUMNS: TECHNICAL SKILLS & SECURITY FOCUS -->
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

                        <!-- TECHNICAL SKILLS -->
                        <div class="glass-panel border border-[#30363d] rounded-xl p-5 space-y-4">
                            <div class="flex items-center space-x-2 border-b border-[#30363d] pb-3">
                                <i class="fa-solid fa-microchip text-red-500 text-base"></i>
                                <h3 class="text-sm font-bold text-white uppercase tracking-wider cyber-font">Technical Skills</h3>
                            </div>

                            <div class="space-y-3.5">
                                <div>
                                    <p class="text-[11px] font-semibold text-gray-400 mb-2 flex items-center space-x-1.5">
                                        <i class="fa-solid fa-code text-cyan-400"></i>
                                        <span>Languages</span>
                                    </p>
                                    <div class="flex flex-wrap gap-1.5">
                                        <span class="bg-[#07090e] border border-blue-500/40 text-blue-300 text-xs px-2.5 py-1 rounded font-mono">Python</span>
                                        <span class="bg-[#07090e] border border-yellow-500/40 text-yellow-300 text-xs px-2.5 py-1 rounded font-mono">JavaScript</span>
                                        <span class="bg-[#07090e] border border-gray-500/40 text-gray-300 text-xs px-2.5 py-1 rounded font-mono">Bash</span>
                                        <span class="bg-[#07090e] border border-purple-500/40 text-purple-300 text-xs px-2.5 py-1 rounded font-mono">SQL</span>
                                    </div>
                                </div>

                                <div>
                                    <p class="text-[11px] font-semibold text-gray-400 mb-2 flex items-center space-x-1.5">
                                        <i class="fa-solid fa-wrench text-yellow-400"></i>
                                        <span>Security Tools</span>
                                    </p>
                                    <div class="flex flex-wrap gap-1.5">
                                        <span class="bg-[#07090e] border border-orange-500/40 text-orange-300 text-xs px-2.5 py-1 rounded font-mono">Burp Suite</span>
                                        <span class="bg-[#07090e] border border-blue-500/40 text-blue-300 text-xs px-2.5 py-1 rounded font-mono">OWASP ZAP</span>
                                        <span class="bg-[#07090e] border border-red-500/40 text-red-300 text-xs px-2.5 py-1 rounded font-mono">Nmap</span>
                                        <span class="bg-[#07090e] border border-cyan-500/40 text-cyan-300 text-xs px-2.5 py-1 rounded font-mono">Wireshark</span>
                                        <span class="bg-[#07090e] border border-pink-500/40 text-pink-300 text-xs px-2.5 py-1 rounded font-mono">Metasploit</span>
                                        <span class="bg-[#07090e] border border-gray-500/40 text-gray-300 text-xs px-2.5 py-1 rounded font-mono">Linux</span>
                                    </div>
                                </div>

                                <div>
                                    <p class="text-[11px] font-semibold text-gray-400 mb-2 flex items-center space-x-1.5">
                                        <i class="fa-solid fa-cubes text-purple-400"></i>
                                        <span>Frameworks & Platforms</span>
                                    </p>
                                    <div class="flex flex-wrap gap-1.5">
                                        <span class="bg-[#07090e] border border-green-500/40 text-green-300 text-xs px-2.5 py-1 rounded font-mono">Django</span>
                                        <span class="bg-[#07090e] border border-gray-500/40 text-gray-300 text-xs px-2.5 py-1 rounded font-mono">Flask</span>
                                        <span class="bg-[#07090e] border border-cyan-500/40 text-cyan-300 text-xs px-2.5 py-1 rounded font-mono">React</span>
                                        <span class="bg-[#07090e] border border-blue-500/40 text-blue-300 text-xs px-2.5 py-1 rounded font-mono">Docker</span>
                                        <span class="bg-[#07090e] border border-red-500/40 text-red-300 text-xs px-2.5 py-1 rounded font-mono">Git</span>
                                        <span class="bg-[#07090e] border border-purple-500/40 text-purple-300 text-xs px-2.5 py-1 rounded font-mono">GitHub</span>
                                        <span class="bg-[#07090e] border border-yellow-500/40 text-yellow-300 text-xs px-2.5 py-1 rounded font-mono">AWS</span>
                                    </div>
                                </div>

                                <div>
                                    <p class="text-[11px] font-semibold text-gray-400 mb-2 flex items-center space-x-1.5">
                                        <i class="fa-solid fa-terminal text-green-400"></i>
                                        <span>Other Ecosystems</span>
                                    </p>
                                    <div class="flex flex-wrap gap-1.5">
                                        <span class="bg-[#07090e] border border-blue-500/40 text-blue-300 text-xs px-2.5 py-1 rounded font-mono">VS Code</span>
                                        <span class="bg-[#07090e] border border-orange-500/40 text-orange-300 text-xs px-2.5 py-1 rounded font-mono">Postman</span>
                                        <span class="bg-[#07090e] border border-purple-500/40 text-purple-300 text-xs px-2.5 py-1 rounded font-mono">Terraform</span>
                                        <span class="bg-[#07090e] border border-blue-500/40 text-blue-300 text-xs px-2.5 py-1 rounded font-mono">Kali Linux</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- SECURITY FOCUS -->
                        <div class="glass-panel border border-[#30363d] rounded-xl p-5 space-y-4">
                            <div class="flex items-center space-x-2 border-b border-[#30363d] pb-3">
                                <i class="fa-solid fa-crosshairs text-red-500 text-base"></i>
                                <h3 class="text-sm font-bold text-white uppercase tracking-wider cyber-font">Security Focus</h3>
                            </div>

                            <div class="space-y-2.5">
                                <div class="bg-[#07090e] border border-[#30363d] hover:border-red-500/70 p-3 rounded-lg flex items-center justify-between group transition cursor-pointer">
                                    <div class="flex items-center space-x-3">
                                        <i class="fa-solid fa-shield-virus text-red-500 text-base"></i>
                                        <div>
                                            <p class="text-xs font-bold text-white group-hover:text-red-400 transition">Web Application Security</p>
                                            <p class="text-[11px] text-gray-400">OWASP Top 10, input validation, business logic</p>
                                        </div>
                                    </div>
                                    <i class="fa-solid fa-chevron-right text-xs text-gray-600 group-hover:text-red-400 transition"></i>
                                </div>

                                <div class="bg-[#07090e] border border-[#30363d] hover:border-cyan-500/70 p-3 rounded-lg flex items-center justify-between group transition cursor-pointer">
                                    <div class="flex items-center space-x-3">
                                        <i class="fa-solid fa-network-wired text-cyan-400 text-base"></i>
                                        <div>
                                            <p class="text-xs font-bold text-white group-hover:text-cyan-300 transition">API Security</p>
                                            <p class="text-[11px] text-gray-400">Authentication, authorization, object-level access</p>
                                        </div>
                                    </div>
                                    <i class="fa-solid fa-chevron-right text-xs text-gray-600 group-hover:text-cyan-300 transition"></i>
                                </div>

                                <div class="bg-[#07090e] border border-[#30363d] hover:border-purple-500/70 p-3 rounded-lg flex items-center justify-between group transition cursor-pointer">
                                    <div class="flex items-center space-x-3">
                                        <i class="fa-solid fa-key text-purple-400 text-base"></i>
                                        <div>
                                            <p class="text-xs font-bold text-white group-hover:text-purple-300 transition">Identity & Access Management</p>
                                            <p class="text-[11px] text-gray-400">Sessions, access control, identity workflows</p>
                                        </div>
                                    </div>
                                    <i class="fa-solid fa-chevron-right text-xs text-gray-600 group-hover:text-purple-300 transition"></i>
                                </div>

                                <div class="bg-[#07090e] border border-[#30363d] hover:border-yellow-500/70 p-3 rounded-lg flex items-center justify-between group transition cursor-pointer">
                                    <div class="flex items-center space-x-3">
                                        <i class="fa-solid fa-cloud text-yellow-400 text-base"></i>
                                        <div>
                                            <p class="text-xs font-bold text-white group-hover:text-yellow-300 transition">Cloud Security</p>
                                            <p class="text-[11px] text-gray-400">AWS, misconfigurations, privilege escalation</p>
                                        </div>
                                    </div>
                                    <i class="fa-solid fa-chevron-right text-xs text-gray-600 group-hover:text-yellow-300 transition"></i>
                                </div>

                                <div class="bg-[#07090e] border border-[#30363d] hover:border-green-500/70 p-3 rounded-lg flex items-center justify-between group transition cursor-pointer">
                                    <div class="flex items-center space-x-3">
                                        <i class="fa-solid fa-lock text-green-400 text-base"></i>
                                        <div>
                                            <p class="text-xs font-bold text-white group-hover:text-green-300 transition">Security Engineering</p>
                                            <p class="text-[11px] text-gray-400">Secure coding, automation, defensive tools</p>
                                        </div>
                                    </div>
                                    <i class="fa-solid fa-chevron-right text-xs text-gray-600 group-hover:text-green-300 transition"></i>
                                </div>
                            </div>
                        </div>

                    </div>


                    <!-- FEATURED PROJECTS MATRIX -->
                    <div class="glass-panel border border-[#30363d] rounded-xl p-5 space-y-4">
                        <div class="flex items-center justify-between border-b border-[#30363d] pb-3">
                            <div class="flex items-center space-x-2">
                                <i class="fa-regular fa-folder-open text-red-500 text-base"></i>
                                <h3 class="text-sm font-bold text-white uppercase tracking-wider cyber-font">Featured Repositories</h3>
                            </div>
                            <a href="#" onclick="switchTab('repositories')" class="text-xs text-cyan-400 hover:underline flex items-center space-x-1 font-mono">
                                <span>View all 22 repos</span>
                                <i class="fa-solid fa-arrow-right text-[10px]"></i>
                            </a>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">

                            <!-- Repo 1 -->
                            <div class="bg-[#07090e] border border-[#30363d] rounded-xl p-4 flex flex-col justify-between glow-hover">
                                <div>
                                    <div class="flex items-center justify-between mb-2">
                                        <div class="flex items-center space-x-2 truncate">
                                            <i class="fa-solid fa-shield-cat text-cyan-400 text-sm"></i>
                                            <a href="#" class="text-xs font-bold text-blue-400 hover:underline truncate">SWYNEX-Web-Security-Review</a>
                                        </div>
                                    </div>
                                    <p class="text-[11px] text-gray-400 line-clamp-2 mb-3">
                                        Defensive web security review of OWASP Juice Shop. Security headers, config checks, Python script + manual analysis.
                                    </p>
                                </div>
                                <div class="flex flex-wrap gap-1 font-mono">
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Python</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Security</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">OWASP</span>
                                </div>
                            </div>

                            <!-- Repo 2 -->
                            <div class="bg-[#07090e] border border-[#30363d] rounded-xl p-4 flex flex-col justify-between glow-hover">
                                <div>
                                    <div class="flex items-center justify-between mb-2">
                                        <div class="flex items-center space-x-2 truncate">
                                            <i class="fa-solid fa-gears text-purple-400 text-sm"></i>
                                            <a href="#" class="text-xs font-bold text-blue-400 hover:underline truncate">API-Security-Lab</a>
                                        </div>
                                    </div>
                                    <p class="text-[11px] text-gray-400 line-clamp-2 mb-3">
                                        API security testing and analysis. Auth, authorization, IDOR, rate limiting test cases.
                                    </p>
                                </div>
                                <div class="flex flex-wrap gap-1 font-mono">
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Python</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">API</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Security</span>
                                </div>
                            </div>

                            <!-- Repo 3 -->
                            <div class="bg-[#07090e] border border-[#30363d] rounded-xl p-4 flex flex-col justify-between glow-hover">
                                <div>
                                    <div class="flex items-center justify-between mb-2">
                                        <div class="flex items-center space-x-2 truncate">
                                            <i class="fa-solid fa-robot text-red-400 text-sm"></i>
                                            <a href="#" class="text-xs font-bold text-blue-400 hover:underline truncate">Security-Automation-Toolkit</a>
                                        </div>
                                    </div>
                                    <p class="text-[11px] text-gray-400 line-clamp-2 mb-3">
                                        Python tools for automated security checks, header analysis, and vulnerability reporting.
                                    </p>
                                </div>
                                <div class="flex flex-wrap gap-1 font-mono">
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Python</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Automation</span>
                                </div>
                            </div>

                            <!-- Repo 4 -->
                            <div class="bg-[#07090e] border border-[#30363d] rounded-xl p-4 flex flex-col justify-between glow-hover">
                                <div>
                                    <div class="flex items-center justify-between mb-2">
                                        <div class="flex items-center space-x-2 truncate">
                                            <i class="fa-regular fa-file-lines text-yellow-400 text-sm"></i>
                                            <a href="#" class="text-xs font-bold text-blue-400 hover:underline truncate">Vulnerability-Research-Notes</a>
                                        </div>
                                    </div>
                                    <p class="text-[11px] text-gray-400 line-clamp-2 mb-3">
                                        Technical write-ups and PoCs for real-world web and infrastructure vulnerabilities.
                                    </p>
                                </div>
                                <div class="flex flex-wrap gap-1 font-mono">
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Research</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Security</span>
                                </div>
                            </div>

                            <!-- Repo 5 -->
                            <div class="bg-[#07090e] border border-[#30363d] rounded-xl p-4 flex flex-col justify-between glow-hover">
                                <div>
                                    <div class="flex items-center justify-between mb-2">
                                        <div class="flex items-center space-x-2 truncate">
                                            <i class="fa-solid fa-book text-green-400 text-sm"></i>
                                            <a href="#" class="text-xs font-bold text-blue-400 hover:underline truncate">AppSec-Knowledge-Base</a>
                                        </div>
                                    </div>
                                    <p class="text-[11px] text-gray-400 line-clamp-2 mb-3">
                                        Application security concepts, cheat sheets, testing methodologies and references.
                                    </p>
                                </div>
                                <div class="flex flex-wrap gap-1 font-mono">
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Documentation</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">AppSec</span>
                                </div>
                            </div>

                            <!-- Repo 6 -->
                            <div class="bg-[#07090e] border border-[#30363d] rounded-xl p-4 flex flex-col justify-between glow-hover">
                                <div>
                                    <div class="flex items-center justify-between mb-2">
                                        <div class="flex items-center space-x-2 truncate">
                                            <i class="fa-solid fa-code text-pink-400 text-sm"></i>
                                            <a href="#" class="text-xs font-bold text-blue-400 hover:underline truncate">Secure-Coding-Examples</a>
                                        </div>
                                    </div>
                                    <p class="text-[11px] text-gray-400 line-clamp-2 mb-3">
                                        Secure coding practices and side-by-side vulnerability fix examples.
                                    </p>
                                </div>
                                <div class="flex flex-wrap gap-1 font-mono">
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Python</span>
                                    <span class="bg-[#161b22] text-gray-300 text-[10px] px-2 py-0.5 rounded border border-[#30363d]">Secure Code</span>
                                </div>
                            </div>

                        </div>
                    </div>


                    <!-- GITHUB STATS & RESEARCH METHODOLOGY GRID -->
                    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

                        <!-- LEFT 7 COLS: STATS & HEATMAP -->
                        <div class="lg:col-span-7 space-y-6">

                            <!-- Heatmap Box -->
                            <div class="glass-panel border border-[#30363d] rounded-xl p-5 space-y-4">
                                <div class="flex items-center space-x-2 border-b border-[#30363d] pb-3">
                                    <i class="fa-solid fa-chart-line text-red-500 text-base"></i>
                                    <h3 class="text-sm font-bold text-white uppercase tracking-wider cyber-font">GitHub Statistics</h3>
                                </div>

                                <!-- Metric Counters -->
                                <div class="grid grid-cols-3 gap-2 text-center bg-[#07090e] border border-[#30363d] p-3 rounded-lg cyber-font">
                                    <div>
                                        <p class="text-[10px] text-gray-400 uppercase">Contributions</p>
                                        <p id="display-total-contrib" class="text-xl font-bold text-white">66</p>
                                        <p class="text-[9px] text-gray-500">Feb 15 – Present</p>
                                    </div>
                                    <div>
                                        <p class="text-[10px] text-gray-400 uppercase">Current Streak</p>
                                        <p class="text-xl font-bold text-orange-400 flex items-center justify-center space-x-1">
                                            <i class="fa-solid fa-fire text-xs"></i>
                                            <span id="display-current-streak">2</span>
                                        </p>
                                        <p class="text-[9px] text-gray-500">Apr 3 – Apr 4</p>
                                    </div>
                                    <div>
                                        <p class="text-[10px] text-gray-400 uppercase">Longest Streak</p>
                                        <p class="text-xl font-bold text-red-500 flex items-center justify-center space-x-1">
                                            <i class="fa-solid fa-fire text-xs"></i>
                                            <span id="display-longest-streak">2</span>
                                        </p>
                                        <p class="text-[9px] text-gray-500">Dec 20 – Dec 21</p>
                                    </div>
                                </div>

                                <!-- Contribution Heatmap -->
                                <div class="overflow-x-auto pb-2">
                                    <div class="text-[10px] text-gray-400 mb-2 flex justify-between font-mono">
                                        <span>Jan</span><span>Feb</span><span>Mar</span><span>Apr</span><span>May</span><span>Jun</span><span>Jul</span><span>Aug</span><span>Sep</span><span>Oct</span><span>Nov</span><span>Dec</span>
                                    </div>
                                    <div id="contribution-grid" class="grid grid-rows-7 grid-flow-col gap-1 min-w-[500px]">
                                        <!-- JS populated -->
                                    </div>
                                    <div class="flex items-center justify-end space-x-2 text-[10px] text-gray-400 mt-3 font-mono">
                                        <span>Less</span>
                                        <span class="w-2.5 h-2.5 rounded-sm contrib-0 border border-[#30363d]"></span>
                                        <span class="w-2.5 h-2.5 rounded-sm contrib-1"></span>
                                        <span class="w-2.5 h-2.5 rounded-sm contrib-2"></span>
                                        <span class="w-2.5 h-2.5 rounded-sm contrib-3"></span>
                                        <span class="w-2.5 h-2.5 rounded-sm contrib-4"></span>
                                        <span>More</span>
                                    </div>
                                </div>
                            </div>

                            <!-- Languages Donut Box -->
                            <div class="glass-panel border border-[#30363d] rounded-xl p-5 space-y-4">
                                <h3 class="text-sm font-bold text-white border-b border-[#30363d] pb-3 cyber-font">Most Used Languages</h3>
                                <div class="flex flex-col sm:flex-row items-center justify-around gap-6">
                                    <!-- Donut Chart -->
                                    <div class="relative w-36 h-36 flex items-center justify-center">
                                        <div id="dynamic-donut" class="w-full h-full rounded-full shadow-[0_0_20px_rgba(0,0,0,0.8)]"></div>
                                        <div class="absolute w-22 h-22 bg-[#07090e] rounded-full flex flex-col items-center justify-center border border-[#30363d] font-mono">
                                            <span id="donut-center-pct" class="text-sm font-bold text-white">42.3%</span>
                                            <span class="text-[10px] text-cyan-400">Python</span>
                                        </div>
                                    </div>

                                    <!-- Legend -->
                                    <div class="space-y-2 text-xs font-mono">
                                        <div class="flex items-center space-x-2">
                                            <span class="w-3 h-3 rounded-full bg-[#3178c6] shadow-[0_0_5px_#3178c6]"></span>
                                            <span class="text-gray-200 font-semibold w-24">Python</span>
                                            <span id="legend-python" class="text-cyan-400">42.3%</span>
                                        </div>
                                        <div class="flex items-center space-x-2">
                                            <span class="w-3 h-3 rounded-full bg-[#f7df1e] shadow-[0_0_5px_#f7df1e]"></span>
                                            <span class="text-gray-200 font-semibold w-24">JavaScript</span>
                                            <span id="legend-js" class="text-cyan-400">28.7%</span>
                                        </div>
                                        <div class="flex items-center space-x-2">
                                            <span class="w-3 h-3 rounded-full bg-[#e34c26] shadow-[0_0_5px_#e34c26]"></span>
                                            <span class="text-gray-200 font-semibold w-24">HTML</span>
                                            <span id="legend-html" class="text-cyan-400">12.1%</span>
                                        </div>
                                        <div class="flex items-center space-x-2">
                                            <span class="w-3 h-3 rounded-full bg-[#563d7c] shadow-[0_0_5px_#563d7c]"></span>
                                            <span class="text-gray-200 font-semibold w-24">CSS</span>
                                            <span id="legend-css" class="text-cyan-400">8.4%</span>
                                        </div>
                                        <div class="flex items-center space-x-2">
                                            <span class="w-3 h-3 rounded-full bg-[#89e051] shadow-[0_0_5px_#89e051]"></span>
                                            <span class="text-gray-200 font-semibold w-24">Other</span>
                                            <span id="legend-other" class="text-cyan-400">8.5%</span>
                                        </div>
                                    </div>
                                </div>
                            </div>

                        </div>

                        <!-- RIGHT 5 COLS: RESEARCH METHODOLOGY TIMELINE -->
                        <div class="lg:col-span-5 space-y-6">
                            
                            <div class="glass-panel border border-[#30363d] rounded-xl p-5 space-y-4 h-full flex flex-col justify-between">
                                <div>
                                    <div class="flex items-center space-x-2 border-b border-[#30363d] pb-3 mb-4">
                                        <i class="fa-solid fa-flask text-pink-500 text-base"></i>
                                        <h3 class="text-sm font-bold text-white uppercase tracking-wider cyber-font">Research & Methodology</h3>
                                    </div>

                                    <div class="space-y-2.5 text-xs font-mono">
                                        <div class="flex items-start space-x-3 bg-[#07090e] p-2.5 rounded-lg border border-[#30363d] hover:border-red-500/60 transition group">
                                            <span class="w-5 h-5 rounded-full bg-red-500/20 text-red-400 flex items-center justify-center font-bold text-[10px] group-hover:bg-red-500 group-hover:text-white transition">1</span>
                                            <span class="text-gray-300 pt-0.5">Define scope and authorization</span>
                                        </div>
                                        <div class="flex items-start space-x-3 bg-[#07090e] p-2.5 rounded-lg border border-[#30363d] hover:border-red-500/60 transition group">
                                            <span class="w-5 h-5 rounded-full bg-red-500/20 text-red-400 flex items-center justify-center font-bold text-[10px] group-hover:bg-red-500 group-hover:text-white transition">2</span>
                                            <span class="text-gray-300 pt-0.5">Map the attack surface</span>
                                        </div>
                                        <div class="flex items-start space-x-3 bg-[#07090e] p-2.5 rounded-lg border border-[#30363d] hover:border-red-500/60 transition group">
                                            <span class="w-5 h-5 rounded-full bg-red-500/20 text-red-400 flex items-center justify-center font-bold text-[10px] group-hover:bg-red-500 group-hover:text-white transition">3</span>
                                            <span class="text-gray-300 pt-0.5">Analyze authentication & authorization</span>
                                        </div>
                                        <div class="flex items-start space-x-3 bg-[#07090e] p-2.5 rounded-lg border border-[#30363d] hover:border-red-500/60 transition group">
                                            <span class="w-5 h-5 rounded-full bg-red-500/20 text-red-400 flex items-center justify-center font-bold text-[10px] group-hover:bg-red-500 group-hover:text-white transition">4</span>
                                            <span class="text-gray-300 pt-0.5">Test security controls (authorized env)</span>
                                        </div>
                                        <div class="flex items-start space-x-3 bg-[#07090e] p-2.5 rounded-lg border border-[#30363d] hover:border-red-500/60 transition group">
                                            <span class="w-5 h-5 rounded-full bg-red-500/20 text-red-400 flex items-center justify-center font-bold text-[10px] group-hover:bg-red-500 group-hover:text-white transition">5</span>
                                            <span class="text-gray-300 pt-0.5">Collect reproducible evidence</span>
                                        </div>
                                        <div class="flex items-start space-x-3 bg-[#07090e] p-2.5 rounded-lg border border-[#30363d] hover:border-red-500/60 transition group">
                                            <span class="w-5 h-5 rounded-full bg-red-500/20 text-red-400 flex items-center justify-center font-bold text-[10px] group-hover:bg-red-500 group-hover:text-white transition">6</span>
                                            <span class="text-gray-300 pt-0.5">Assess impact & prioritize findings</span>
                                        </div>
                                        <div class="flex items-start space-x-3 bg-[#07090e] p-2.5 rounded-lg border border-[#30363d] hover:border-red-500/60 transition group">
                                            <span class="w-5 h-5 rounded-full bg-red-500/20 text-red-400 flex items-center justify-center font-bold text-[10px] group-hover:bg-red-500 group-hover:text-white transition">7</span>
                                            <span class="text-gray-300 pt-0.5">Document remediation & validation</span>
                                        </div>
                                    </div>
                                </div>

                                <!-- Terminal Footer Motif -->
                                <div class="mt-4 pt-3 border-t border-[#30363d] text-center cyber-font text-xs text-red-400">
                                    <p class="animate-pulse">&gt;_ Keep Learning / Keep Building / Keep Securing</p>
                                </div>
                            </div>

                        </div>

                    </div>

                </div>

                <!-- REPOSITORIES TAB -->
                <div id="repositories-content" class="hidden space-y-4">
                    <div class="flex flex-col sm:flex-row items-center justify-between gap-3 bg-[#0d1117] p-3 rounded-lg border border-[#30363d]">
                        <input type="text" id="repoSearchInput" placeholder="Filter repositories by name..." oninput="filterRepos()" class="bg-[#07090e] border border-[#30363d] text-xs px-3 py-2 rounded w-full max-w-xs focus:outline-none focus:border-red-500 text-white font-mono">
                        <div class="flex space-x-2">
                            <button onclick="filterRepoType('all')" class="bg-[#161b22] text-xs px-3 py-1.5 rounded border border-[#30363d] text-gray-300 hover:bg-[#21262d] font-mono">All</button>
                            <button onclick="filterRepoType('python')" class="bg-[#161b22] text-xs px-3 py-1.5 rounded border border-[#30363d] text-gray-300 hover:bg-[#21262d] font-mono">Python</button>
                            <button onclick="filterRepoType('security')" class="bg-[#161b22] text-xs px-3 py-1.5 rounded border border-[#30363d] text-gray-300 hover:bg-[#21262d] font-mono">Security</button>
                        </div>
                    </div>

                    <div id="repo-list" class="space-y-3">
                        <!-- Dynamic Repos Populated via JS -->
                    </div>
                </div>

                <!-- GENERIC FALLBACK TAB CONTENT -->
                <div id="generic-tab-content" class="hidden glass-panel border border-[#30363d] rounded-xl p-16 text-center text-gray-400">
                    <i class="fa-solid fa-code-branch text-5xl mb-4 text-red-500"></i>
                    <h3 class="text-xl font-bold text-white mb-2" id="generic-tab-title">TAB SECTION</h3>
                    <p class="text-xs text-gray-400 font-mono">Connected to live profile repository dashboard.</p>
                </div>

            </div>

        </div>
    </main>

    <!-- FOOTER TAGLINE BANNER -->
    <footer class="bg-[#0d1117] border-t border-[#21262d] py-8 mt-12 relative z-10">
        <div class="max-w-7xl mx-auto px-4 text-center space-y-2">
            <p class="cyber-font text-base font-bold tracking-widest text-red-500">
                SECURITY IS A JOURNEY
            </p>
            <p class="cyber-font text-xs text-gray-400">
                &gt;_ Not a destination.
            </p>
            <div class="pt-4 flex justify-center items-center space-x-6 text-xs text-gray-500 font-mono">
                <a href="#" class="hover:text-cyan-400">Terms</a>
                <a href="#" class="hover:text-cyan-400">Privacy</a>
                <a href="#" class="hover:text-cyan-400">Security</a>
                <a href="#" class="hover:text-cyan-400">Docs</a>
                <a href="mailto:baburamsharma658@gmail.com" class="hover:text-cyan-400">Contact Babu Ram Sharma</a>
            </div>
        </div>
    </footer>


    <!-- JAVASCRIPT PROFILE & INTERACTION LOGIC -->
    <script>
        // Default User State with Provided Custom Details
        let profileState = {
            name: "Babu Ram Sharma",
            username: "CHITASTAR59",
            tagline: "Cybersecurity Researcher | Web & API Security | Application Security | Red Teaming | Bug Bounty Hunter | Vulnerability Research",
            avatar: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=400",
            bannerTitle: "CHITASTAR",
            bannerSub: "CYBERSECURITY RESEARCHER",
            bannerDomains: "WEB / API / APPLICATION SECURITY / VULNERABILITY RESEARCH",
            location: "Dallas, Texas",
            email: "baburamsharma658@gmail.com",
            website: "hackerai.oi",
            linkedin: "https://www.linkedin.com/in/babu-ram-sharma-482527350/",
            twitter: "https://x.com/CHITASTAR59",
            followers: 4,
            following: 0,
            readmeBio: "I'm a cybersecurity researcher focused on offensive security and application security. I enjoy finding and understanding security weaknesses in web applications, APIs, cloud infrastructure, and modern web technologies.",
            pills: "Web Security, API Security, Application Security, Red Teaming, Bug Bounty, Vulnerability Research",
            quote: "Security is not a product, it's a process.",
            totalContrib: 66,
            currentStreak: 2,
            longestStreak: 2,
            pythonPct: 42.3,
            jsPct: 28.7,
            htmlPct: 12.1
        };

        // All Repos Data
        const reposData = [
            { name: 'SWYNEX-Web-Security-Review', desc: 'Defensive web security review of OWASP Juice Shop. Security headers, config checks, Python script + manual analysis.', lang: 'Python', stars: 12, category: 'security' },
            { name: 'API-Security-Lab', desc: 'API security testing and analysis framework. Auth, authorization, IDOR, rate limiting.', lang: 'Python', stars: 18, category: 'security' },
            { name: 'Security-Automation-Toolkit', desc: 'Python tools for automated security checks, header analysis, and reporting.', lang: 'Python', stars: 24, category: 'python' },
            { name: 'Vulnerability-Research-Notes', desc: 'Technical write-ups and PoCs for real-world web vulnerabilities.', lang: 'Markdown', stars: 45, category: 'security' },
            { name: 'AppSec-Knowledge-Base', desc: 'Application security concepts, cheat sheets, testing methodologies and references.', lang: 'HTML', stars: 19, category: 'security' },
            { name: 'Secure-Coding-Examples', desc: 'Secure coding practices and common vulnerability fix examples.', lang: 'JavaScript', stars: 31, category: 'python' }
        ];

        // Populate Input Form Fields
        function initFormValues() {
            document.getElementById('input-name').value = profileState.name;
            document.getElementById('input-username').value = profileState.username;
            document.getElementById('input-tagline').value = profileState.tagline;
            document.getElementById('input-avatar').value = profileState.avatar;
            document.getElementById('input-banner-title').value = profileState.bannerTitle;
            document.getElementById('input-banner-sub').value = profileState.bannerSub;
            document.getElementById('input-banner-domains').value = profileState.bannerDomains;
            document.getElementById('input-location').value = profileState.location;
            document.getElementById('input-email').value = profileState.email;
            document.getElementById('input-website').value = profileState.website;
            document.getElementById('input-linkedin').value = profileState.linkedin;
            document.getElementById('input-twitter').value = profileState.twitter;
            document.getElementById('input-readme-bio').value = profileState.readmeBio;
            document.getElementById('input-pills').value = profileState.pills;
            document.getElementById('input-total-contrib').value = profileState.totalContrib;
            document.getElementById('input-current-streak').value = profileState.currentStreak;
            document.getElementById('input-longest-streak').value = profileState.longestStreak;
        }

        // Live Profile Updates Triggered on Input
        function updateProfile() {
            profileState.name = document.getElementById('input-name').value || "Babu Ram Sharma";
            profileState.username = document.getElementById('input-username').value || "CHITASTAR59";
            profileState.tagline = document.getElementById('input-tagline').value || "";
            profileState.avatar = document.getElementById('input-avatar').value || "https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=400";
            profileState.bannerTitle = document.getElementById('input-banner-title').value || "CHITASTAR";
            profileState.bannerSub = document.getElementById('input-banner-sub').value || "CYBERSECURITY RESEARCHER";
            profileState.bannerDomains = document.getElementById('input-banner-domains').value || "WEB / API / APPLICATION SECURITY";
            profileState.location = document.getElementById('input-location').value || "Dallas, Texas";
            profileState.email = document.getElementById('input-email').value || "baburamsharma658@gmail.com";
            profileState.website = document.getElementById('input-website').value || "hackerai.oi";
            profileState.linkedin = document.getElementById('input-linkedin').value || "https://www.linkedin.com/in/babu-ram-sharma-482527350/";
            profileState.twitter = document.getElementById('input-twitter').value || "https://x.com/CHITASTAR59";
            profileState.readmeBio = document.getElementById('input-readme-bio').value || "";
            profileState.pills = document.getElementById('input-pills').value || "";
            profileState.totalContrib = document.getElementById('input-total-contrib').value || 0;
            profileState.currentStreak = document.getElementById('input-current-streak').value || 0;
            profileState.longestStreak = document.getElementById('input-longest-streak').value || 0;

            // DOM Updates
            document.getElementById('display-name').innerText = profileState.name;
            document.getElementById('readme-name').innerText = profileState.name;
            document.getElementById('display-username').innerText = profileState.username;
            document.getElementById('readme-username').innerText = profileState.username;
            document.getElementById('display-tagline').innerText = profileState.tagline;

            document.getElementById('display-avatar').src = profileState.avatar;
            document.getElementById('nav-avatar').src = profileState.avatar;

            document.getElementById('display-banner-title').innerText = profileState.bannerTitle;
            document.getElementById('display-banner-sub').innerText = profileState.bannerSub;
            document.getElementById('display-banner-domains').innerText = profileState.bannerDomains;

            document.getElementById('display-location').innerText = profileState.location;
            document.getElementById('display-email').innerText = profileState.email;
            document.getElementById('display-email-link').href = `mailto:${profileState.email}`;
            document.getElementById('connect-email').href = `mailto:${profileState.email}`;

            let formattedWeb = profileState.website.replace(/^https?:\/\//, '');
            document.getElementById('display-website').innerText = formattedWeb;
            document.getElementById('display-website-link').href = profileState.website.startsWith('http') ? profileState.website : `https://${profileState.website}`;
            document.getElementById('connect-website').href = profileState.website.startsWith('http') ? profileState.website : `https://${profileState.website}`;

            document.getElementById('connect-linkedin').href = profileState.linkedin;
            document.getElementById('connect-twitter').href = profileState.twitter.startsWith('http') ? profileState.twitter : `https://x.com/${profileState.twitter}`;

            document.getElementById('display-readme-bio').innerText = profileState.readmeBio;
            document.getElementById('display-total-contrib').innerText = profileState.totalContrib;
            document.getElementById('display-current-streak').innerText = profileState.currentStreak;
            document.getElementById('display-longest-streak').innerText = profileState.longestStreak;

            // Render Skill Pills
            const pillsArr = profileState.pills.split(',').map(p => p.trim()).filter(p => p.length > 0);
            const pillsContainer = document.getElementById('display-pills-container');
            const colors = ['red', 'cyan', 'purple', 'yellow', 'green'];
            pillsContainer.innerHTML = pillsArr.map((pill, idx) => {
                const c = colors[idx % colors.length];
                return `<span class="bg-[#07090e] border border-${c}-500/50 text-${c}-400 text-xs px-3 py-1 rounded-full font-mono flex items-center space-x-1 shadow-[0_0_8px_rgba(0,0,0,0.5)]">
                    <i class="fa-solid fa-shield-halved text-[10px]"></i>
                    <span>${pill}</span>
                </span>`;
            }).join('');

            renderDonutChart();
        }

        // Donut Chart Render
        function renderDonutChart() {
            const py = profileState.pythonPct;
            const js = profileState.jsPct;
            const html = profileState.htmlPct;
            const css = 8.4;
            const remaining = Math.max(0, (100 - (py + js + html + css)).toFixed(1));

            const p1 = py;
            const p2 = p1 + js;
            const p3 = p2 + html;
            const p4 = p3 + css;

            const donut = document.getElementById('dynamic-donut');
            if (donut) {
                donut.style.background = `conic-gradient(
                    #3178c6 0% ${p1}%,
                    #f7df1e ${p1}% ${p2}%,
                    #e34c26 ${p2}% ${p3}%,
                    #563d7c ${p3}% ${p4}%,
                    #89e051 ${p4}% 100%
                )`;
            }

            document.getElementById('donut-center-pct').innerText = `${py}%`;
            document.getElementById('legend-python').innerText = `${py}%`;
            document.getElementById('legend-js').innerText = `${js}%`;
            document.getElementById('legend-html').innerText = `${html}%`;
            document.getElementById('legend-css').innerText = `8.4%`;
            document.getElementById('legend-other').innerText = `${remaining}%`;
        }

        // Scanline Effect Toggle
        function toggleScanline() {
            const el = document.getElementById('scanlineEffect');
            el.classList.toggle('hidden');
        }

        // Terminal Drawer Toggle
        function toggleTerminal() {
            const modal = document.getElementById('terminalModal');
            modal.classList.toggle('hidden');
            if (!modal.classList.contains('hidden')) {
                document.getElementById('terminalInput').focus();
            }
        }

        // Terminal Command Processing
        function handleTerminalCommand(e) {
            if (e.key === 'Enter') {
                const input = document.getElementById('terminalInput');
                const cmd = input.value.trim().toLowerCase();
                const output = document.getElementById('terminalOutput');

                const cmdLine = document.createElement('p');
                cmdLine.className = 'text-white font-bold';
                cmdLine.innerHTML = `<span class="text-pink-500">&gt;_</span> ${input.value}`;
                output.appendChild(cmdLine);

                const response = document.createElement('p');
                response.className = 'text-cyan-300 pl-4 border-l border-cyan-500/40';

                switch(cmd) {
                    case 'help':
                        response.innerHTML = `Available commands: <br>
                        - <b class="text-yellow-400">whoami</b> : Display researcher details<br>
                        - <b class="text-yellow-400">skills</b> : List core security skills<br>
                        - <b class="text-yellow-400">contact</b> : Output email and LinkedIn<br>
                        - <b class="text-yellow-400">website</b> : Launch hackerai.oi<br>
                        - <b class="text-yellow-400">clear</b> : Clear shell window`;
                        break;
                    case 'whoami':
                        response.innerText = `${profileState.name} (${profileState.username}) - Cybersecurity Researcher & Vulnerability Expert.`;
                        break;
                    case 'skills':
                        response.innerText = `Web App Security, API Penetration Testing, Red Teaming, OWASP Top 10, Python Security Tools, Cloud Auditing.`;
                        break;
                    case 'contact':
                        response.innerText = `Email: ${profileState.email} | LinkedIn: ${profileState.linkedin} | Twitter: ${profileState.twitter}`;
                        break;
                    case 'website':
                        response.innerText = `Opening https://${profileState.website}...`;
                        window.open(`https://${profileState.website}`, '_blank');
                        break;
                    case 'clear':
                        output.innerHTML = '';
                        input.value = '';
                        return;
                    default:
                        response.innerText = `Command not recognized: '${cmd}'. Type 'help' for menu.`;
                }

                output.appendChild(response);
                input.value = '';
                output.scrollTop = output.scrollHeight;
            }
        }

        // Drawer Toggle
        function toggleEditor() {
            document.getElementById('editorDrawer').classList.toggle('translate-x-full');
        }

        // Export Clean Web Application HTML
        function exportHTML() {
            const pageDoc = "<!DOCTYPE html>\n" + document.documentElement.outerHTML;
            const blob = new Blob([pageDoc], { type: 'text/html' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `${profileState.username}_cyber_profile.html`;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
        }

        // Generate Dynamic Contribution Matrix Heatmap
        function generateContributions() {
            const grid = document.getElementById('contribution-grid');
            if (!grid) return;

            for (let i = 0; i < 364; i++) {
                const cell = document.createElement('div');
                cell.className = 'w-2.5 h-2.5 rounded-sm ';
                
                const rand = Math.random();
                if (rand > 0.88) cell.className += 'contrib-4';
                else if (rand > 0.72) cell.className += 'contrib-3';
                else if (rand > 0.55) cell.className += 'contrib-2';
                else if (rand > 0.40) cell.className += 'contrib-1';
                else cell.className += 'contrib-0 border border-[#21262d]';

                cell.setAttribute('data-tooltip', `Day ${i + 1}: ${Math.floor(rand * 10)} security commits`);
                grid.appendChild(cell);
            }
        }

        // Tab Navigation Switcher
        function switchTab(tabName) {
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('border-red-500', 'text-white', 'font-bold');
                btn.classList.add('border-transparent', 'text-gray-400');
            });

            const activeBtn = document.getElementById(`tab-${tabName}`);
            if (activeBtn) {
                activeBtn.classList.remove('border-transparent', 'text-gray-400');
                activeBtn.classList.add('border-red-500', 'text-white', 'font-bold');
            }

            document.getElementById('overview-content').classList.add('hidden');
            document.getElementById('repositories-content').classList.add('hidden');
            document.getElementById('generic-tab-content').classList.add('hidden');

            if (tabName === 'overview') {
                document.getElementById('overview-content').classList.remove('hidden');
            } else if (tabName === 'repositories') {
                renderRepositories(reposData);
                document.getElementById('repositories-content').classList.remove('hidden');
            } else {
                document.getElementById('generic-tab-title').innerText = tabName.toUpperCase() + " DASHBOARD";
                document.getElementById('generic-tab-content').classList.remove('hidden');
            }
        }

        // Render Repository List
        function renderRepositories(repos) {
            const container = document.getElementById('repo-list');
            if (!container) return;

            container.innerHTML = repos.map(repo => `
                <div class="glass-panel border border-[#30363d] rounded-xl p-4 flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 hover:border-cyan-500/60 transition">
                    <div>
                        <div class="flex items-center space-x-2">
                            <i class="fa-regular fa-folder-closed text-cyan-400"></i>
                            <a href="#" class="text-sm font-bold text-blue-400 hover:underline font-mono">${repo.name}</a>
                            <span class="text-[10px] bg-[#161b22] text-gray-400 border border-[#30363d] px-2 py-0.5 rounded-full font-mono">Public</span>
                        </div>
                        <p class="text-xs text-gray-300 mt-1.5">${repo.desc}</p>
                        <div class="flex items-center space-x-4 text-[11px] text-gray-400 mt-2 font-mono">
                            <span class="flex items-center space-x-1">
                                <span class="w-2.5 h-2.5 rounded-full bg-blue-500"></span>
                                <span>${repo.lang}</span>
                            </span>
                            <span><i class="fa-regular fa-star text-yellow-500"></i> ${repo.stars}</span>
                            <span>Updated recently</span>
                        </div>
                    </div>
                    <button class="bg-[#161b22] border border-[#30363d] hover:border-yellow-500 text-xs text-gray-200 px-3 py-1.5 rounded-md flex items-center space-x-1 font-mono">
                        <i class="fa-regular fa-star text-yellow-500"></i>
                        <span>Star</span>
                    </button>
                </div>
            `).join('');
        }

        function filterRepos() {
            const query = document.getElementById('repoSearchInput').value.toLowerCase();
            const filtered = reposData.filter(r => r.name.toLowerCase().includes(query) || r.desc.toLowerCase().includes(query));
            renderRepositories(filtered);
        }

        function filterRepoType(type) {
            if (type === 'all') renderRepositories(reposData);
            else {
                const filtered = reposData.filter(r => r.category === type || r.lang.toLowerCase() === type);
                renderRepositories(filtered);
            }
        }

        // Digital Rain Canvas Animation Engine
        function startMatrixRain() {
            const canvas = document.getElementById('matrixCanvas');
            if (!canvas) return;
            const ctx = canvas.getContext('2d');

            canvas.width = canvas.parentElement.offsetWidth;
            canvas.height = canvas.parentElement.offsetHeight;

            const chars = '01ABCDEFHIJKLMNOPQRSTUVWXYZCHITASTAR59$%#@&';
            const fontSize = 12;
            const columns = Math.floor(canvas.width / fontSize);
            const drops = Array(columns).fill(1);

            function draw() {
                ctx.fillStyle = 'rgba(7, 9, 14, 0.1)';
                ctx.fillRect(0, 0, canvas.width, canvas.height);

                ctx.fillStyle = '#00f3ff';
                ctx.font = `${fontSize}px Fira Code`;

                for (let i = 0; i < drops.length; i++) {
                    const text = chars.charAt(Math.floor(Math.random() * chars.length));
                    ctx.fillText(text, i * fontSize, drops[i] * fontSize);

                    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                        drops[i] = 0;
                    }
                    drops[i]++;
                }
            }

            setInterval(draw, 40);

            window.addEventListener('resize', () => {
                canvas.width = canvas.parentElement.offsetWidth;
                canvas.height = canvas.parentElement.offsetHeight;
            });
        }

        // Window Load Handler
        window.onload = function() {
            initFormValues();
            updateProfile();
            generateContributions();
            startMatrixRain();
        };
    </script>
</body>
</html>
