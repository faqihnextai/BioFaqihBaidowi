<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Faqih Baidowi - Interactive Profile</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8fafc;
            color: #1e293b;
            overflow-x: hidden;
        }
        
        .profile-card {
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .profile-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
        }
        
        .skill-badge {
            transition: all 0.2s ease;
        }
        
        .skill-badge:hover {
            transform: scale(1.05);
        }
        
        #snake-game {
            border: 2px solid #0ea5e9;
            border-radius: 8px;
        }
        
        .character {
            position: absolute;
            width: 80px;
            height: 80px;
            background-image: url('https://opengameart.org/sites/default/files/Green-Cap-Character-16x18.png');
            background-size: cover;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .typewriter h1 {
            overflow: hidden;
            border-right: .15em solid #0ea5e9;
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: .15em;
            animation: 
                typing 3.5s steps(40, end),
                blink-caret .75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #0ea5e9; }
        }
    </style>
</head>
<body class="min-h-screen">
    <!-- Language Toggle -->
    <div class="text-center mb-4">
        <button id="toggle-language" class="px-4 py-2 bg-sky-600 text-white rounded hover:bg-sky-700 transition">Switch to Indonesian</button>
    </div>

    <!-- Floating Characters -->
    <div class="character" style="top: 100px; left: 50px;"></div>
    <div class="character" style="top: 300px; right: 100px;"></div>
    <div class="character" style="bottom: 150px; left: 200px;"></div>
    
    <div class="container mx-auto px-4 py-12">
        <!-- Header with Typewriter Effect -->
        <div class="typewriter text-center mb-12">
            <h1 id="header-title" class="text-4xl font-bold text-sky-600">Hello, I'm Faqih Baidowi</h1>
        </div>
        
        <div class="flex flex-col lg:flex-row gap-8">
            <!-- Profile Card -->
            <div class="profile-card lg:w-1/3 p-8 rounded-xl">
                <div class="flex flex-col items-center">
                    <div class="w-32 h-32 rounded-full bg-sky-100 mb-4 overflow-hidden">
                        <img src="https://avatars.githubusercontent.com/u/12345678?v=4" alt="Profile" class="w-full h-full object-cover">
                    </div>
                    <h2 class="text-2xl font-bold text-sky-800">Faqih Baidowi</h2>
                    <p class="text-sky-600 mb-4">Teacher & Developer</p>
                    
                    <div class="w-full mb-6">
                        <h3 class="font-semibold text-sky-700 mb-2">Contact</h3>
                        <ul class="space-y-1">
                            <li class="flex items-center">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-sky-500 mr-2" viewBox="0 0 20 20" fill="currentColor">
                                    <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z" />
                                </svg>
                                +62 895-41188-1772
                            </li>
                            <li class="flex items-center">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-sky-500 mr-2" viewBox="0 0 20 20" fill="currentColor">
                                    <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z" />
                                    <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z" />
                                </svg>
                                faqihloh@gmail.com
                            </li>
                            <li class="flex items-center">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-sky-500 mr-2" viewBox="0 0 20 20" fill="currentColor">
                                    <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" />
                                </svg>
                                Tangerang, Banten, Indonesia
                            </li>
                        </ul>
                    </div>
                    
                    <div class="w-full">
                        <h3 class="font-semibold text-sky-700 mb-2">Social Media</h3>
                        <div class="flex justify-center space-x-4">
                            <a href="#" class="text-sky-600 hover:text-sky-800 transition">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                                    <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                                </svg>
                            </a>
                            <a href="#" class="text-sky-600 hover:text-sky-800 transition">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                                    <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
                                </svg>
                            </a>
                            <a href="#" class="text-sky-600 hover:text-sky-800 transition">
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                                    <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
                                </svg>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Main Content -->
            <div class="lg:w-2/3 space-y-8">
                <!-- About Me -->
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <h2 id="about-title" class="text-2xl font-bold text-sky-700 mb-4">About Me</h2>
                    <p id="about-text" class="text-slate-700 mb-4">
                        I'm an Informatics Teacher at elementary school who's also active as a developer, specializing in teaching and developing applications based on Python, PHP, HTML, CSS, and JavaScript. I'm known as a hard worker who can effectively handle various tasks.
                    </p>
                    <p id="about-text-2" class="text-slate-700">
                        My vision is to achieve objective goals without external intervention, focusing on the real impact of every work I develop. I've built various digital solutions like QR Code attendance systems, e-commerce websites, and Android applications.
                    </p>
                </div>
                
                <!-- Snake Game -->
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <h2 class="text-2xl font-bold text-sky-700 mb-4">Play Snake Game While Reading!</h2>
                    <div class="flex flex-col md:flex-row gap-6">
                        <div class="md:w-1/2">
                            <canvas id="snake-game" width="300" height="300" class="w-full"></canvas>
                            <div class="mt-4 flex justify-between">
                                <button id="start-game" class="px-4 py-2 bg-sky-600 text-white rounded hover:bg-sky-700 transition">Start Game</button>
                                <div class="text-sky-600 font-semibold">Score: <span id="score">0</span></div>
                            </div>
                        </div>
                        <div class="md:w-1/2">
                            <h3 class="text-lg font-semibold text-sky-700 mb-2">Controls:</h3>
                            <ul class="list-disc pl-5 text-slate-700 space-y-1">
                                <li>Use <span class="font-semibold">Arrow Keys</span> to move</li>
                                <li>Eat the <span class="text-red-500 font-semibold">red food</span> to grow</li>
                                <li>Avoid hitting walls or yourself</li>
                            </ul>
                            <h3 class="text-lg font-semibold text-sky-700 mt-4 mb-2">Fun Fact:</h3>
                            <p class="text-slate-700">
                                Did you know? The Snake game concept originated in 1976 with the arcade game Blockade. It became widely popular when Nokia included it on their mobile phones in the late 1990s.
                            </p>
                        </div>
                    </div>
                </div>
                
                <!-- Skills -->
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <h2 class="text-2xl font-bold text-sky-700 mb-4">Skills & Expertise</h2>
                    <div class="grid grid-cols-2 md:grid-cols-3 gap-3">
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">Teaching</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">Web Development</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">Mobile App Dev</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">Python</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">PHP</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">JavaScript</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">HTML/CSS</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">QR Code Systems</div>
                        <div class="skill-badge bg-sky-100 text-sky-800 px-4 py-2 rounded-full text-center font-medium">E-commerce</div>
                    </div>
                </div>
                
                <!-- Experience & Education -->
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <h2 class="text-2xl font-bold text-sky-700 mb-4">Experience & Education</h2>
                    <ul class="list-disc pl-5 text-slate-700 space-y-1">
                        <li>Wakil Bagian Kesehatan — Pondok Pesantren Daarul Rahman (2021/2022)</li>
                        <li>Panitia Acara Peralatan kelulusan SDI Daarul Huda (2023/2024)</li>
                        <li>
