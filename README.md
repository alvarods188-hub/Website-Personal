# Website-Personal
[index.html](https://github.com/user-attachments/files/23550721/index.html.html)
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Problem Solver - Solusi Cerdas untuk Setiap Masalah</title>
    <style>
        *
            {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #6366f1;
            --secondary: #8b5cf6;
            --accent: #ec4899;
            --dark: #0f172a;
            --light: #f8fafc;
            --success: #10b981;
            --warning: #f59e0b;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: var(--light);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Animated Background */
        .animated-bg {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
            background: linear-gradient(45deg, #0f172a, #1e293b, #334155);
        }

        .particles {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            animation: float 15s infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) translateX(0); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100vh) translateX(100px); opacity: 0; }
        }

        /* Header */
        header {
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        }

        nav {
            max-width: 1400px;
            margin: 0 auto;
            padding: 1.2rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.6rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 8px;
        }

        .nav-links a:hover {
            background: rgba(255, 255, 255, 0.1);
            color: var(--accent);
        }

        /* Hero */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 8rem 2rem 4rem;
        }

        .hero-content {
            max-width: 1000px;
            animation: fadeInUp 1s ease;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 {
            font-size: 4.5rem;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, #fff 0%, #a78bfa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.2;
        }

        .subtitle {
            font-size: 1.5rem;
            color: #cbd5e1;
            margin-bottom: 3rem;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1.2rem 3rem;
            font-size: 1.1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            box-shadow: 0 10px 40px rgba(99, 102, 241, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 50px rgba(99, 102, 241, 0.5);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.15);
            color: white;
            border: 2px solid rgba(255, 255, 255, 0.3);
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.25);
            transform: translateY(-3px);
        }

        /* Section */
        .section {
            max-width: 1400px;
            margin: 6rem auto;
            padding: 0 2rem;
        }

        .section-title {
            font-size: 3rem;
            text-align: center;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-subtitle {
            text-align: center;
            color: #94a3b8;
            font-size: 1.2rem;
            margin-bottom: 4rem;
        }

        /* Tools Grid */
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .tool-card {
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 25px;
            padding: 2.5rem;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .tool-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.4);
            background: rgba(255, 255, 255, 0.12);
        }

        .tool-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .tool-icon {
            font-size: 3rem;
        }

        .tool-title {
            font-size: 1.8rem;
            color: var(--light);
        }

        /* Password Generator */
        .password-display {
            background: rgba(0, 0, 0, 0.4);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 15px;
            padding: 1.5rem;
            font-size: 1.5rem;
            font-family: monospace;
            text-align: center;
            margin-bottom: 1.5rem;
            word-break: break-all;
            min-height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .password-controls {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .control-group {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .slider {
            width: 100%;
            height: 8px;
            border-radius: 5px;
            background: rgba(255, 255, 255, 0.2);
            outline: none;
            margin-top: 0.5rem;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            cursor: pointer;
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            cursor: pointer;
        }

        input[type="checkbox"] {
            width: 20px;
            height: 20px;
            cursor: pointer;
        }

        /* QR Code Generator */
        .qr-input {
            width: 100%;
            background: rgba(0, 0, 0, 0.4);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 15px;
            padding: 1.2rem;
            color: white;
            font-size: 1.1rem;
            margin-bottom: 1rem;
        }

        .qr-input:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 20px rgba(99, 102, 241, 0.3);
        }

        .qr-display {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            margin-top: 1.5rem;
            text-align: center;
            min-height: 250px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Color Converter */
        .color-preview {
            height: 150px;
            border-radius: 15px;
            margin-bottom: 1.5rem;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .color-inputs {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .color-input-group {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .color-label {
            width: 100px;
            font-weight: 600;
        }

        input[type="text"].color-value {
            flex: 1;
            background: rgba(0, 0, 0, 0.4);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            padding: 0.8rem;
            color: white;
            font-family: monospace;
        }

        /* Unit Converter */
        .converter-grid {
            display: grid;
            grid-template-columns: 1fr auto 1fr;
            gap: 1rem;
            align-items: center;
        }

        .convert-input {
            width: 100%;
            background: rgba(0, 0, 0, 0.4);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            padding: 1rem;
            color: white;
            font-size: 1.2rem;
            text-align: center;
        }

        select {
            width: 100%;
            background: rgba(0, 0, 0, 0.4);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            padding: 0.8rem;
            color: white;
            font-size: 1rem;
            margin-top: 0.5rem;
        }

        select option {
            background: var(--dark);
        }

        .swap-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .swap-btn:hover {
            transform: rotate(180deg) scale(1.1);
        }

        /* Text Tools */
        textarea {
            width: 100%;
            min-height: 150px;
            background: rgba(0, 0, 0, 0.4);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 15px;
            padding: 1.2rem;
            color: white;
            font-size: 1.1rem;
            resize: vertical;
            font-family: inherit;
        }

        textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 20px rgba(99, 102, 241, 0.3);
        }

        .text-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
            margin-top: 1rem;
        }

        .stat-box {
            background: rgba(0, 0, 0, 0.4);
            border-radius: 10px;
            padding: 1rem;
            text-align: center;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: var(--primary);
        }

        .stat-label {
            color: #94a3b8;
            font-size: 0.9rem;
            margin-top: 0.5rem;
        }

        .text-buttons {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
            margin-top: 1rem;
        }

        .text-btn {
            padding: 0.8rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            color: white;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }

        .text-btn:hover {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            transform: translateY(-2px);
        }

        /* Calculator */
        .calculator {
            background: rgba(0, 0, 0, 0.4);
            border-radius: 20px;
            padding: 1.5rem;
        }

        .calc-display {
            background: rgba(0, 0, 0, 0.6);
            border-radius: 15px;
            padding: 2rem;
            font-size: 2.5rem;
            text-align: right;
            margin-bottom: 1.5rem;
            min-height: 80px;
            word-wrap: break-word;
            font-family: monospace;
        }

        .calc-buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1rem;
        }

        .calc-btn {
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            border-radius: 15px;
            color: white;
            font-size: 1.3rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
        }

        .calc-btn:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: scale(1.05);
        }

        .calc-btn.operator {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }

        .calc-btn.equals {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            grid-column: span 2;
        }

        .calc-btn.clear {
            background: linear-gradient(135deg, #f59e0b 0%, #ef4444 100%);
        }

        /* Timer/Stopwatch */
        .timer-display {
            font-size: 5rem;
            font-weight: bold;
            text-align: center;
            margin: 2rem 0;
            font-family: monospace;
            color: var(--primary);
        }

        .timer-controls {
            display: flex;
            gap: 1rem;
            justify-content: center;
        }

        .timer-btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 15px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            color: white;
        }

        .timer-btn.start {
            background: var(--success);
        }

        .timer-btn.stop {
            background: var(--warning);
        }

        .timer-btn.reset {
            background: #ef4444;
        }

        .timer-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        /* Footer */
        footer {
            background: rgba(0, 0, 0, 0.5);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding: 4rem 2rem 2rem;
            margin-top: 6rem;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
        }

        .footer-section h3 {
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            color: var(--light);
        }

        .footer-section p {
            color: #94a3b8;
            line-height: 1.8;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.8rem;
        }

        .footer-section a {
            color: #94a3b8;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: var(--primary);
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-icon {
            width: 45px;
            height: 45px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .social-icon:hover {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            transform: translateY(-5px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            margin-top: 3rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #94a3b8;
        }

        /* Scroll to Top */
        .scroll-top {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 55px;
            height: 55px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border: none;
            border-radius: 50%;
            color: white;
            font-size: 1.8rem;
            cursor: pointer;
            opacity: 0;
            transition: all 0.3s ease;
            z-index: 999;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .scroll-top.visible {
            opacity: 1;
        }

        .scroll-top:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 40px rgba(99, 102, 241, 0.5);
        }

        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            .subtitle { font-size: 1.2rem; }
            .tools-grid { grid-template-columns: 1fr; }
            .nav-links { display: none; }
            .timer-display { font-size: 3rem; }
            .text-stats, .text-buttons { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="animated-bg">
        <div class="particles" id="particles"></div>
    </div>

    <header>
        <nav>
            <div class="logo">🚀 AI Problem Solver</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#tools">Tools</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Solusi AI untuk Setiap Masalah</h1>
            <p class="subtitle">Tools canggih berbasis AI yang siap membantu menyelesaikan berbagai masalah sehari-hari Anda secara instant dan efisien</p>
            <div class="cta-buttons">
                <a href="#tools" class="btn btn-primary">Mulai Sekarang</a>
                <a href="#about" class="btn btn-secondary">Pelajari Lebih Lanjut</a>
            </div>
        </div>
    </section>

    <section class="section" id="tools">
        <h2 class="section-title">🛠️ Tools Siap Pakai</h2>
        <p class="section-subtitle">Koleksi lengkap tools praktis untuk produktivitas maksimal</p>

        <div class="tools-grid">
            <!-- Password Generator -->
            <div class="tool-card">
                <div class="tool-header">
                    <div class="tool-icon">🔐</div>
                    <h3 class="tool-title">Password Generator</h3>
                </div>
                <div class="password-display" id="passwordDisplay">Klik Generate untuk membuat password</div>
                <div class="password-controls">
                    <div class="control-group">
                        <label>Panjang: <span id="lengthValue">16</span></label>
                        <input type="range" class="slider" id="passwordLength" min="8" max="32" value="16" oninput="document.getElementById('lengthValue').textContent = this.value">
                    </div>
                    <label class="checkbox-group">
                        <input type="checkbox" id="useUppercase" checked>
                        <span>Huruf Besar (A-Z)</span>
                    </label>
                    <label class="checkbox-group">
                        <input type="checkbox" id="useLowercase" checked>
                        <span>Huruf Kecil (a-z)</span>
                    </label>
                    <label class="checkbox-group">
                        <input type="checkbox" id="useNumbers" checked>
                        <span>Angka (0-9)</span>
                    </label>
                    <label class="checkbox-group">
                        <input type="checkbox" id="useSymbols" checked>
                        <span>Simbol (!@#$%)</span>
                    </label>
                    <button class="btn btn-primary" onclick="generatePassword()">Generate Password</button>
                    <button class="btn btn-secondary" onclick="copyPassword()">Copy ke Clipboard</button>
                </div>
            </div>

            <!-- QR Code Generator -->
            <div class="tool-card">
                <div class="tool-header">
                    <div class="tool-icon">📱</div>
                    <h3 class="tool-title">QR Code Generator</h3>
                </div>
                <input type="text" class="qr-input" id="qrInput" placeholder="Masukkan URL, teks, atau nomor WhatsApp...">
                <button class="btn btn-primary" onclick="generateQR()">Generate QR Code</button>
                <div class="qr-display" id="qrDisplay">QR Code akan muncul di sini</div>
            </div>

            <!-- Color Converter -->
            <div class="tool-card">
                <div class="tool-header">
                    <div class="tool-icon">🎨</div>
                    <h3 class="tool-title">Color Converter</h3>
                </div>
                <div class="color-preview" id="colorPreview" style="background: #667eea;"></div>
                <div class="color-inputs">
                    <div class="color-input-group">
                        <label class="color-label">HEX:</label>
                        <input type="text" class="color-value" id="hexInput" value="#667eea" oninput="convertColor('hex')">
                    </div>
                    <div class="color-input-group">
                        <label class="color-label">RGB:</label>
                        <input type="text" class="color-value" id="rgbInput" value="rgb(102, 126, 234)" oninput="convertColor('rgb')">
                    </div>
                    <div class="color-input-group">
                        <label class="color-label">HSL:</label>
                        <input type="text" class="color-value" id="hslInput" value="hsl(232, 77%, 66%)" oninput="convertColor('hsl')">
                    </div>
                </div>
            </div>

            <!-- Unit Converter -->
            <div class="tool-card">
                <div class="tool-header">
                    <div class="tool-icon">📏</div>
                    <h3 class="tool-title">Unit Converter</h3>
                </div>
                <div class="converter-grid">
                    <div>
                        <input type="number" class="convert-input" id="fromValue" value="1" oninput="convertUnit()">
                        <select id="fromUnit" onchange="convertUnit()">
                            <option value="m">Meter</option>
                            <option value="km">Kilometer</option>
                            <option value="cm">Centimeter</option>
                            <option value="mm">Millimeter</option>
                            <option value="mi">Mile</option>
                            <option value="ft">Feet</option>
                            <option value="in">Inch</option>
                        </select>
                    </div>
                    <button class="swap-btn" onclick="swapUnits()">⇄</button>
                    <div>
                        <input type="number" class="convert-input" id="toValue" readonly>
                        <select id="toUnit" onchange="convertUnit()">
                            <option value="m">Meter</option>
                            <option value="km" selected>Kilometer</option>
                            <option value="cm">Centimeter</option>
                            <option value="mm">Millimeter</option>
                            <option value="mi">Mile</option>
                            <option value="ft">Feet</option>
                            <option value="in">Inch</option>
                        </select>
                    </div>
                </div>
            </div>

            <!-- Text Analyzer -->
            <div class="tool-card">
                <div class="tool-header">
                    <div class="tool-icon">📝</div>
                    <h3 class="tool-title">Text Analyzer & Tools</h3>
                </div>
                <textarea id="textInput" placeholder="Ketik atau paste teks Anda di sini..." oninput="analyzeText()"></textarea>
                <div class="text-stats">
                    <div class="stat-box">
                        <div class="stat-number" id="charCount">0</div>
                        <div class="stat-label">Karakter</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number" id="wordCount">0</div>
                        <div class="stat-label">Kata</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number" id="sentenceCount">0</div>
                        <div class="stat-label">Kalimat</div>
                    </div>
                </div>
                <div class="text-buttons">
                    <button class="text-btn" onclick="transformText('upper')">UPPERCASE</button>
                    <button class="text-btn" onclick="transformText('lower')">lowercase</button>
                    <button class="text-btn" onclick="transformText('title')">Title Case</button>
                    <button class="text-btn" onclick="transformText('reverse')">Reverse</button>
                    <button class="text-btn" onclick="transformText('remove')">Remove Space</button>
                    <button class="text-btn" onclick="copyText()">Copy Text</button>
                </div>
            </div>

            <!-- Calculator -->
            <div class="tool-card">
                <div class="tool-header">
                    <div class="tool-icon">🔢</div>
                    <h3 class="tool-title">Smart Calculator</h3>
                </div>
                <div class="calculator">
                    <div class="calc-display" id="calcDisplay">0</div>
                    <div class="calc-buttons">
                        <button class="calc-btn clear" onclick="clearCalc()">C</button>
                        <button class="calc-btn" onclick="appendCalc('(')">(</button>
                        <button class="calc-btn" onclick="appendCalc(')')">)</button>
                        <button class="calc-btn operator" onclick="appendCalc('/')">÷</button>
                        
                        <button class="calc-btn" onclick="appendCalc('7')">7</button>
                        <button class="calc-btn" onclick="appendCalc('8')">8</button>
                        <button class="calc-btn" onclick="appendCalc('9')">9</button>
                        <button class="calc-btn operator" onclick="appendCalc('*')">×</button>
                        
                        <button class="calc-btn" onclick="appendCalc('4')">4</button>
                        <button class="calc-btn" onclick="appendCalc('5')">5</button>
                        <button class="calc-btn" onclick="appendCalc('6')">6</button>
                        <button class="calc-btn operator" onclick="appendCalc('-')">−</button>
                        
                        <button class="calc-btn" onclick="appendCalc('1')">1</button>
                        <button class="calc-btn" onclick="appendCalc('2')">2</button>
                        <button class="calc-btn" onclick="appendCalc('3')">3</button>
                        <button class="calc-btn operator" onclick="appendCalc('+')">+</button>
                        
                        <button class="calc-btn" onclick="appendCalc('0')">0</button>
                        <button class="calc-btn" onclick="appendCalc('.')">.</button>
                        <button class="calc-btn equals" onclick="calculateResult()">=</button>
                    </div>
                </div>
            </div>

            <!-- Timer & Stopwatch -->
            <div class="tool-card">
                <div class="tool-header">
                    <div class="tool-icon">⏱️</div>
                    <h3 class="tool-title">Timer & Stopwatch</h3>
                </div>
                <div class="timer-display" id="timerDisplay">00:00:00</div>
                <div class="timer-controls">
                    <button class="timer-btn start" onclick="startTimer()">Start</button>
                    <button class="timer-btn stop" onclick="stopTimer()">Stop</button>
                    <button class="timer-btn reset" onclick="resetTimer()">Reset</button>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <h2 class="section-title">Tentang AI Problem Solver</h2>
        <p class="section-subtitle">Platform inovatif yang menggabungkan kecerdasan buatan dengan tools praktis</p>
        
        <div style="max-width: 800px; margin: 0 auto; background: rgba(255, 255, 255, 0.08); border: 1px solid rgba(255, 255, 255, 0.15); border-radius: 25px; padding: 3rem; backdrop-filter: blur(10px);">
            <p style="font-size: 1.2rem; line-height: 2; color: #cbd5e1; text-align: justify;">
                <strong style="color: #fff; font-size: 1.3rem;">AI Problem Solver</strong> adalah platform revolusioner yang dirancang untuk membantu manusia menyelesaikan berbagai masalah sehari-hari dengan cepat dan efisien. Kami percaya bahwa teknologi AI harus accessible, mudah digunakan, dan memberikan solusi nyata untuk kebutuhan praktis.
                <br><br>
                Dengan koleksi tools yang terus berkembang, kami menyediakan solusi untuk kebutuhan seperti keamanan password, konversi unit, analisis teks, dan banyak lagi. Semua tools kami dirancang dengan antarmuka yang intuitif dan responsif, sehingga siapa saja dapat menggunakannya tanpa kesulitan.
                <br><br>
                <strong style="color: #fff;">Visi kami</strong> adalah menciptakan ekosistem digital di mana AI dan manusia bekerja sama secara harmonis untuk meningkatkan produktivitas, kreativitas, dan kualitas hidup. Setiap tool yang kami kembangkan dirancang dengan fokus pada user experience, kecepatan, dan keakuratan.
            </p>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="footer-content">
            <div class="footer-section">
                <h3>🚀 AI Problem Solver</h3>
                <p>Platform terpercaya untuk menyelesaikan berbagai masalah dengan bantuan teknologi AI yang canggih dan mudah digunakan.</p>
                <div class="social-links">
                    <div class="social-icon">📘</div>
                    <div class="social-icon">🐦</div>
                    <div class="social-icon">📷</div>
                    <div class="social-icon">💼</div>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#tools">Tools</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Popular Tools</h3>
                <ul>
                    <li><a href="#tools">Password Generator</a></li>
                    <li><a href="#tools">QR Code Generator</a></li>
                    <li><a href="#tools">Color Converter</a></li>
                    <li><a href="#tools">Unit Converter</a></li>
                    <li><a href="#tools">Text Analyzer</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Contact Us</h3>
                <ul>
                    <li>📧 alvarods@gmail.com</li>
                    <li>📱 +62 811-9915-730</li>
                    <li>📍 Bali, Indonesia</li>
                    <li>🕐 24/7 Support</li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2025 AI Problem Solver. All rights reserved. Made with ❤️ in Indonesia</p>
        </div>
    </footer>

    <button class="scroll-top" id="scrollTop" onclick="scrollToTop()">↑</button>

    <script>
        // Create animated particles
        const particlesContainer = document.getElementById('particles');
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.left = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 15 + 's';
            particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
            particlesContainer.appendChild(particle);
        }

        // Scroll effects
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            const scrollTop = document.getElementById('scrollTop');
            
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
                scrollTop.classList.add('visible');
            } else {
                header.classList.remove('scrolled');
                scrollTop.classList.remove('visible');
            }
        });

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Password Generator
        function generatePassword() {
            const length = document.getElementById('passwordLength').value;
            const useUppercase = document.getElementById('useUppercase').checked;
            const useLowercase = document.getElementById('useLowercase').checked;
            const useNumbers = document.getElementById('useNumbers').checked;
            const useSymbols = document.getElementById('useSymbols').checked;

            let charset = '';
            if (useUppercase) charset += 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
            if (useLowercase) charset += 'abcdefghijklmnopqrstuvwxyz';
            if (useNumbers) charset += '0123456789';
            if (useSymbols) charset += '!@#$%^&*()_+-=[]{}|;:,.<>?';

            if (charset === '') {
                alert('Pilih minimal satu jenis karakter!');
                return;
            }

            let password = '';
            for (let i = 0; i < length; i++) {
                password += charset.charAt(Math.floor(Math.random() * charset.length));
            }

            document.getElementById('passwordDisplay').textContent = password;
        }

        function copyPassword() {
            const password = document.getElementById('passwordDisplay').textContent;
            if (password === 'Klik Generate untuk membuat password') {
                alert('Generate password terlebih dahulu!');
                return;
            }
            navigator.clipboard.writeText(password);
            alert('Password berhasil di-copy ke clipboard!');
        }

        // QR Code Generator
        function generateQR() {
            const text = document.getElementById('qrInput').value;
            if (!text) {
                alert('Masukkan teks atau URL terlebih dahulu!');
                return;
            }
            const qrDisplay = document.getElementById('qrDisplay');
            qrDisplay.innerHTML = `<img src="https://api.qrserver.com/v1/create-qr-code/?size=250x250&data=${encodeURIComponent(text)}" alt="QR Code" style="max-width: 100%;">`;
        }

        // Color Converter
        function convertColor(from) {
            const hexInput = document.getElementById('hexInput');
            const rgbInput = document.getElementById('rgbInput');
            const hslInput = document.getElementById('hslInput');
            const preview = document.getElementById('colorPreview');

            try {
                if (from === 'hex') {
                    let hex = hexInput.value;
                    if (!hex.startsWith('#')) hex = '#' + hex;
                    preview.style.background = hex;
                    const rgb = hexToRgb(hex);
                    rgbInput.value = `rgb(${rgb.r}, ${rgb.g}, ${rgb.b})`;
                    const hsl = rgbToHsl(rgb.r, rgb.g, rgb.b);
                    hslInput.value = `hsl(${hsl.h}, ${hsl.s}%, ${hsl.l}%)`;
                }
            } catch (e) {
                console.error('Invalid color format');
            }
        }

        function hexToRgb(hex) {
            const result = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(hex);
            return result ? {
                r: parseInt(result[1], 16),
                g: parseInt(result[2], 16),
                b: parseInt(result[3], 16)
            } : null;
        }

        function rgbToHsl(r, g, b) {
            r /= 255; g /= 255; b /= 255;
            const max = Math.max(r, g, b), min = Math.min(r, g, b);
            let h, s, l = (max + min) / 2;

            if (max === min) {
                h = s = 0;
            } else {
                const d = max - min;
                s = l > 0.5 ? d / (2 - max - min) : d / (max + min);
                switch (max) {
                    case r: h = ((g - b) / d + (g < b ? 6 : 0)) / 6; break;
                    case g: h = ((b - r) / d + 2) / 6; break;
                    case b: h = ((r - g) / d + 4) / 6; break;
                }
            }

            return {
                h: Math.round(h * 360),
                s: Math.round(s * 100),
                l: Math.round(l * 100)
            };
        }

        // Unit Converter
        const unitConversions = {
            m: 1, km: 0.001, cm: 100, mm: 1000,
            mi: 0.000621371, ft: 3.28084, in: 39.3701
        };

        function convertUnit() {
            const fromValue = parseFloat(document.getElementById('fromValue').value);
            const fromUnit = document.getElementById('fromUnit').value;
            const toUnit = document.getElementById('toUnit').value;

            const meters = fromValue / unitConversions[fromUnit];
            const result = meters * unitConversions[toUnit];

            document.getElementById('toValue').value = result.toFixed(6);
        }

        function swapUnits() {
            const fromUnit = document.getElementById('fromUnit');
            const toUnit = document.getElementById('toUnit');
            const temp = fromUnit.value;
            fromUnit.value = toUnit.value;
            toUnit.value = temp;
            convertUnit();
        }

        // Text Analyzer
        function analyzeText() {
            const text = document.getElementById('textInput').value;
            document.getElementById('charCount').textContent = text.length;
            document.getElementById('wordCount').textContent = text.trim() ? text.trim().split(/\s+/).length : 0;
            document.getElementById('sentenceCount').textContent = text.split(/[.!?]+/).filter(s => s.trim()).length;
        }

        function transformText(type) {
            const textArea = document.getElementById('textInput');
            let text = textArea.value;

            switch(type) {
                case 'upper': textArea.value = text.toUpperCase(); break;
                case 'lower': textArea.value = text.toLowerCase(); break;
                case 'title': textArea.value = text.replace(/\w\S*/g, txt => txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase()); break;
                case 'reverse': textArea.value = text.split('').reverse().join(''); break;
                case 'remove': textArea.value = text.replace(/\s+/g, ''); break;
            }
            analyzeText();
        }

        function copyText() {
            const text = document.getElementById('textInput').value;
            navigator.clipboard.writeText(text);
            alert('Teks berhasil di-copy!');
        }

        // Calculator
        let calcExpression = '';

        function appendCalc(value) {
            calcExpression += value;
            document.getElementById('calcDisplay').textContent = calcExpression || '0';
        }

        function clearCalc() {
            calcExpression = '';
            document.getElementById('calcDisplay').textContent = '0';
        }

        function calculateResult() {
            try {
                const result = eval(calcExpression);
                document.getElementById('calcDisplay').textContent = result;
                calcExpression = result.toString();
            } catch (e) {
                document.getElementById('calcDisplay').textContent = 'Error';
                calcExpression = '';
            }
        }

        // Timer & Stopwatch
        let timerInterval;
        let timerSeconds = 0;
        let isRunning = false;

        function startTimer() {
            if (!isRunning) {
                isRunning = true;
                timerInterval = setInterval(() => {
                    timerSeconds++;
                    updateTimerDisplay();
                }, 1000);
            }
        }

        function stopTimer() {
            isRunning = false;
            clearInterval(timerInterval);
        }

        function resetTimer() {
            stopTimer();
            timerSeconds = 0;
            updateTimerDisplay();
        }

        function updateTimerDisplay() {
            const hours = Math.floor(timerSeconds / 3600);
            const minutes = Math.floor((timerSeconds % 3600) / 60);
            const seconds = timerSeconds % 60;
            document.getElementById('timerDisplay').textContent = 
                `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }

        // Initialize
        convertUnit();
    </script>
</body>
</html>
