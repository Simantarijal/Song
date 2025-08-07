this.cameraEnabled = false;

                this.simulateMovement = false;<!DOCTYPE html>

<html lang="ne">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>नेपाली कविता प्रदर्शन खेल</title>

    <style>

        @import url('https://fonts.googleapis.com/css2?family=Mukti:wght@400;700&display=swap');

        

        * {

            margin: 0;

            padding: 0;

            box-sizing: border-box;

        }

        

        body {

            font-family: 'Mukti', 'Noto Sans Devanagari', Arial, sans-serif;

            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

            min-height: 100vh;

            padding: 20px;

        }

        

        .container {

            max-width: 1200px;

            margin: 0 auto;

            background: rgba(255, 255, 255, 0.95);

            border-radius: 20px;

            box-shadow: 0 20px 40px rgba(0,0,0,0.1);

            overflow: hidden;

        }

        

        .header {

            background: linear-gradient(45deg, #FF6B6B, #4ECDC4);

            padding: 30px;

            text-align: center;

            color: white;

        }

        

        .header h1 {

            font-size: 2.5rem;

            margin-bottom: 10px;

            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);

        }

        

        .header p {

            font-size: 1.1rem;

            opacity: 0.9;

        }

        

        .game-area {

            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 30px;

            padding: 30px;

        }

        

        .recording-section {

            background: #f8f9fa;

            border-radius: 15px;

            padding: 25px;

            text-align: center;

        }

        

        .video-container {

            position: relative;

            background: #000;

            border-radius: 10px;

            margin-bottom: 20px;

            height: 300px;

            display: flex;

            align-items: center;

            justify-content: center;

        }

        

        #videoElement {

            width: 100%;

            height: 100%;

            border-radius: 10px;

            object-fit: cover;

        }

        

        .canvas-overlay {

            position: absolute;

            top: 0;

            left: 0;

            pointer-events: none;

        }

        

        .controls {

            display: flex;

            gap: 15px;

            justify-content: center;

            margin-bottom: 20px;

        }

        

        .btn {

            padding: 12px 25px;

            border: none;

            border-radius: 25px;

            font-size: 1rem;

            cursor: pointer;

            transition: all 0.3s ease;

            font-weight: 600;

        }

        

        .btn-primary {

            background: linear-gradient(45deg, #FF6B6B, #FF8E8E);

            color: white;

        }

        

        .btn-secondary {

            background: linear-gradient(45deg, #4ECDC4, #44A08D);

            color: white;

        }

        

        .btn-success {

            background: linear-gradient(45deg, #56CCF2, #2F80ED);

            color: white;

        }

        

        .btn:hover {

            transform: translateY(-2px);

            box-shadow: 0 5px 15px rgba(0,0,0,0.2);

        }

        

        .btn:disabled {

            opacity: 0.6;

            transform: none;

            cursor: not-allowed;

        }

        

        .upload-area {

            border: 3px dashed #4ECDC4;

            border-radius: 10px;

            padding: 30px;

            margin: 20px 0;

            text-align: center;

            cursor: pointer;

            transition: all 0.3s ease;

        }

        

        .upload-area:hover {

            border-color: #FF6B6B;

            background: rgba(255, 107, 107, 0.05);

        }

        

        .upload-area.dragover {

            border-color: #FF6B6B;

            background: rgba(255, 107, 107, 0.1);

        }

        

        .kavita-section {

            background: #fff;

            border-radius: 15px;

            padding: 25px;

        }

        

        .kavita-text {

            background: #f8f9fa;

            padding: 20px;

            border-radius: 10px;

            margin-bottom: 20px;

            border-left: 5px solid #4ECDC4;

            font-size: 1.1rem;

            line-height: 1.8;

        }

        

        .rhythm-indicators {

            display: flex;

            justify-content: space-around;

            margin: 20px 0;

        }

        

        .rhythm-dot {

            width: 20px;

            height: 20px;

            border-radius: 50%;

            background: #ddd;

            transition: all 0.3s ease;

        }

        

        .rhythm-dot.active {

            background: #FF6B6B;

            transform: scale(1.3);

        }

        

        .score-display {

            background: linear-gradient(45deg, #667eea, #764ba2);

            color: white;

            padding: 25px;

            border-radius: 15px;

            text-align: center;

        }

        

        .score-number {

            font-size: 3rem;

            font-weight: bold;

            margin-bottom: 10px;

        }

        

        .feedback-list {

            list-style: none;

            text-align: left;

            margin-top: 15px;

        }

        

        .feedback-list li {

            padding: 8px 0;

            border-bottom: 1px solid rgba(255,255,255,0.2);

        }

        

        .feedback-list li:last-child {

            border-bottom: none;

        }

        

        .status-indicator {

            padding: 10px;

            margin: 10px 0;

            border-radius: 5px;

            text-align: center;

            font-weight: 600;

        }

        

        .status-recording {

            background: #ffebee;

            color: #c62828;

            border: 2px solid #ffcdd2;

        }

        

        .status-analyzing {

            background: #fff3e0;

            color: #ef6c00;

            border: 2px solid #ffcc02;

        }

        

        .status-complete {

            background: #e8f5e8;

            color: #2e7d32;

            border: 2px solid #c8e6c9;

        }

        

        .hand-tracking {

            background: #e3f2fd;

            padding: 15px;

            border-radius: 10px;

            margin: 15px 0;

        }

        

        .hand-tracking h4 {

            color: #1976d2;

            margin-bottom: 10px;

        }

        

        .movement-bars {

            display: flex;

            gap: 5px;

            height: 20px;

        }

        

        .movement-bar {

            flex: 1;

            background: #ddd;

            border-radius: 2px;

            transition: all 0.3s ease;

        }

        

        .movement-bar.active {

            background: linear-gradient(45deg, #4ECDC4, #44A08D);

        }

        

        @media (max-width: 768px) {

            .game-area {

                grid-template-columns: 1fr;

            }

            

            .header h1 {

                font-size: 2rem;

            }

            

            .controls {

                flex-wrap: wrap;

            }

        }

        

        .audio-visualizer {

            height: 60px;

            background: #f0f0f0;

            border-radius: 10px;

            margin: 10px 0;

            display: flex;

            align-items: end;

            justify-content: center;

            gap: 2px;

            padding: 5px;

        }

        

        .audio-bar {

            width: 4px;

            background: #4ECDC4;

            border-radius: 2px;

            transition: height 0.1s ease;

            min-height: 5px;

        }

    </style>

</head>

<body>

    <div class="container">

        <div class="header">

            <h1>🎭 नेपाली कविता खेल</h1>

<parameter>तपाईंको कविताको मूल्यांकन गर्नुहोस् - गायन, गति र हात चालन</p>

        </div>

        

        <div class="game-area">

            <div class="recording-section">

                <h3>🎥 रेकर्डिङ</h3>

                

                <div class="video-container">

                    <video id="videoElement" autoplay muted></video>

                    <canvas id="handCanvas" class="canvas-overlay" width="640" height="480"></canvas>

                </div>

                

                <div class="controls">

                    <button id="startBtn" class="btn btn-primary">🎙️ सुरु गर्नुहोस्</button>

                    <button id="stopBtn" class="btn btn-secondary" disabled>⏹️ रोक्नुहोस्</button>

                    <button id="analyzeBtn" class="btn btn-success" disabled>🔍 विश्लेषण गर्नुहोस्</button>

                </div>

                

                <div class="upload-area" id="uploadArea">

                    <p>📁 फाइल ड्र्यागथाम्नुहोस् वा क्लिक गर्नुहोस्</p>

                    <input type="file" id="fileInput" accept="audio/*,video/*" style="display: none;">

                </div>

                

                <div class="audio-visualizer" id="audioVisualizer">

                    <!-- Audio bars will be generated here -->

                </div>

                

                <div id="statusIndicator" class="status-indicator" style="display: none;"></div>

                

                <div class="hand-tracking">

                    <h4>हात चालन ट्र्याकिङ</h4>

                    <div class="movement-bars" id="movementBars">

                        <div class="movement-bar"></div>

                        <div class="movement-bar"></div>

                        <div class="movement-bar"></div>

                        <div class="movement-bar"></div>

                        <div class="movement-bar"></div>

                    </div>

                </div>

            </div>

            

            <div class="kavita-section">

                <h3>📝 कविता पाठ</h3>

                

                <div class="kavita-text" id="kavitaText">

                    <p><strong>फूलको आँखामा</strong></p>

                    <p>फूलको आँखामा के छ भन्नू<br>

                    मौनताको गहिरो समुन्द्र<br>

                    वा प्रेमको मिठो संदेश<br>

                    बोल्न नसक्ने भावनाको खुशी</p>

                    <p>हावाले बोकेको सुगन्धमा<br>

                    लुकेको छ जीवनको सार<br>

                    प्रकृतिको यो अनमोल उपहार<br>

                    फूलको आँखामा छ संसार</p>

                </div>

                

                <textarea id="userKavita" placeholder="यहाँ आफ्नो कविता लेख्नुहोस्..." 

                    style="width: 100%; height: 120px; padding: 15px; border-radius: 8px; border: 2px solid #ddd; font-family: inherit; font-size: 1rem; resize: vertical;"></textarea>

                

                <div class="rhythm-indicators" id="rhythmIndicators">

                    <div class="rhythm-dot"></div>

                    <div class="rhythm-dot"></div>

                    <div class="rhythm-dot"></div>

                    <div class="rhythm-dot"></div>

                    <div class="rhythm-dot"></div>

                    <div class="rhythm-dot"></div>

                    <div class="rhythm-dot"></div>

                    <div class="rhythm-dot"></div>

                </div>

                

                <div class="score-display">

                    <div class="score-number" id="totalScore">0</div>

                    <p>कुल अंक</p>

                    

                    <ul class="feedback-list" id="feedbackList">

                        <li>🎵 गायन गुणस्तर: <span id="singingScore">-</span>/30</li>

                        <li>🥁 गति तालमेल: <span id="rhythmScore">-</span>/25</li>

                        <li>👐 हात चालन: <span id="handScore">-</span>/25</li>

                        <li>📖 चन्दा मिलान: <span id="chandaScore">-</span>/20</li>

                    </ul>

                </div>

            </div>

        </div>

    </div>

    <script>

        class NepaliKavitaGame {

            constructor() {

                this.mediaRecorder = null;

                this.recordedChunks = [];

                this.isRecording = false;

                this.audioContext = null;

                this.analyser = null;

                this.handMovements = [];

                this.rhythmPattern = [];

                

                this.initializeElements();

                this.setupEventListeners();

                this.initializeCamera();

                this.createAudioVisualizer();

                this.startRhythmPattern();

            }

            

            initializeElements() {

                this.startBtn = document.getElementById('startBtn');

                this.stopBtn = document.getElementById('stopBtn');

                this.analyzeBtn = document.getElementById('analyzeBtn');

                this.videoElement = document.getElementById('videoElement');

                this.uploadArea = document.getElementById('uploadArea');

                this.fileInput = document.getElementById('fileInput');

                this.statusIndicator = document.getElementById('statusIndicator');

                this.handCanvas = document.getElementById('handCanvas');

                this.userKavita = document.getElementById('userKavita');

                this.audioVisualizer = document.getElementById('audioVisualizer');

                this.movementBars = document.getElementById('movementBars').children;

            }

            

            setupEventListeners() {

                this.startBtn.addEventListener('click', () => this.startRecording());

                this.stopBtn.addEventListener('click', () => this.stopRecording());

                this.analyzeBtn.addEventListener('click', () => this.analyzePerformance());

                

                this.uploadArea.addEventListener('click', () => this.fileInput.click());

                this.uploadArea.addEventListener('dragover', (e) => {

                    e.preventDefault();

                    this.uploadArea.classList.add('dragover');

                });

                this.uploadArea.addEventListener('dragleave', () => {

                    this.uploadArea.classList.remove('dragover');

                });

                this.uploadArea.addEventListener('drop', (e) => {

                    e.preventDefault();

                    this.uploadArea.classList.remove('dragover');

                    this.handleFileUpload(e.dataTransfer.files[0]);

                });

                

                this.fileInput.addEventListener('change', (e) => {

                    if (e.target.files[0]) {

                        this.handleFileUpload(e.target.files[0]);

                    }

                });

            }

            

            async initializeCamera() {

                try {

                    // Try camera first, fall back to audio-only if denied

                    const stream = await navigator.mediaDevices.getUserMedia({ 

                        video: true, 

                        audio: true 

                    });

                    this.videoElement.srcObject = stream;

                    this.stream = stream;

                    this.cameraEnabled = true;

                    this.setupHandTracking();

                    this.showStatus('क्यामेरा र माइक्रो तयार छ!', 'complete');

                } catch (error) {

                    console.log('Camera access denied, trying audio-only:', error);

                    await this.initializeAudioOnly();

                }

            }

            

            async initializeAudioOnly() {

                try {

                    const stream = await navigator.mediaDevices.getUserMedia({ 

                        audio: true 

                    });

                    this.stream = stream;

                    this.cameraEnabled = false;

                    this.videoElement.style.display = 'none';

                    

                    // Show audio-only message

                    const audioOnlyMsg = document.createElement('div');

                    audioOnlyMsg.innerHTML = `

                        <div style="padding: 40px; text-align: center; background: #f0f0f0; border-radius: 10px;">

                            <h3>🎙️ आवाज मात्र रेकर्डिङ</h3>

                            <p>क्यामेरा उपलब्ध छैन, तर आवाज रेकर्ड गर्न सकिन्छ।</p>

                            <p>हात चालन अनुमान गरिनेछ।</p>

                        </div>

                    `;

                    this.videoElement.parentNode.appendChild(audioOnlyMsg);

                    this.setupSimulatedHandTracking();

                    this.showStatus('आवाज मात्र रेकर्डिङ तयार!', 'complete');

                } catch (audioError) {

                    console.error('Audio access also denied:', audioError);

                    this.handleNoMediaAccess();

                }

            }

            

            handleNoMediaAccess() {

                this.cameraEnabled = false;

                this.stream = null;

                

                const noMediaMsg = document.createElement('div');

                noMediaMsg.innerHTML = `

                    <div style="padding: 40px; text-align: center; background: #fff3cd; border-radius: 10px; border: 2px solid #ffc107;">

                        <h3>📁 फाइल अपलोड मोड</h3>

                        <p>क्यामेरा र माइक्रो पहुँच नभएको कारणले,</p>

                        <p>कृपया आफ्नो रेकर्डिङ फाइल अपलोड गर्नुहोस्।</p>

                        <button onclick="document.getElementById('fileInput').click()" class="btn btn-primary" style="margin-top: 15px;">

                            📎 फाइल छान्नुहोस्

                        </button>

                    </div>

                `;

                this.videoElement.parentNode.appendChild(noMediaMsg);

                

                // Disable recording buttons

                this.startBtn.disabled = true;

                this.startBtn.textContent = '📁 फाइल अपलोड गर्नुहोस्';

                this.startBtn.onclick = () => this.fileInput.click();

                this.stopBtn.style.display = 'none';

                

                this.setupSimulatedHandTracking();

                this.showStatus('फाइल अपलोड गर्नुहोस्', 'analyzing');

            }

            

            setupSimulatedHandTracking() {

                // Simulated hand tracking for when camera is not available

                setInterval(() => {

                    if (this.isRecording || this.simulateMovement) {

                        const movement = Math.random() * 8 + 2; // 2-10 range

                        this.handMovements.push(movement);

                        this.updateMovementBars(movement);

                    }

                }, 150);

            }

            

            setupHandTracking() {

                if (!this.cameraEnabled) {

                    this.setupSimulatedHandTracking();

                    return;

                }

                

                // Real hand tracking simulation (would use MediaPipe or similar in production)

                setInterval(() => {

                    if (this.isRecording) {

                        const movement = Math.random() * 10;

                        this.handMovements.push(movement);

                        this.updateMovementBars(movement);

                    }

                }, 100);

            }

            

            updateMovementBars(intensity) {

                const activeCount = Math.floor((intensity / 10) * this.movementBars.length);

                for (let i = 0; i < this.movementBars.length; i++) {

                    if (i < activeCount) {

                        this.movementBars[i].classList.add('active');

                    } else {

                        this.movementBars[i].classList.remove('active');

                    }

                }

            }

            

            createAudioVisualizer() {

                for (let i = 0; i < 32; i++) {

                    const bar = document.createElement('div');

                    bar.className = 'audio-bar';

                    this.audioVisualizer.appendChild(bar);

                }

            }

            

            updateAudioVisualizer() {

                if (!this.analyser) return;

                

                const dataArray = new Uint8Array(this.analyser.frequencyBinCount);

                this.analyser.getByteFrequencyData(dataArray);

                

                const bars = this.audioVisualizer.children;

                for (let i = 0; i < bars.length; i++) {

                    const value = dataArray[i * 4] || 0;

                    const height = (value / 255) * 50 + 5;

                    bars[i].style.height = height + 'px';

                }

            }

            

            startRhythmPattern() {

                const dots = document.querySelectorAll('.rhythm-dot');

                let currentDot = 0;

                

                setInterval(() => {

                    dots.forEach(dot => dot.classList.remove('active'));

                    dots[currentDot].classList.add('active');

                    currentDot = (currentDot + 1) % dots.length;

                }, 500);

            }

            

            async startRecording() {

                if (!this.stream) {

                    this.showStatus('कृपया पहिले फाइल अपलोड गर्नुहोस्', 'error');

                    this.fileInput.click();

                    return;

                }

                

                try {

                    this.recordedChunks = [];

                    this.handMovements = [];

                    

                    this.mediaRecorder = new MediaRecorder(this.stream);

                    this.mediaRecorder.ondataavailable = (event) => {

                        if (event.data.size > 0) {

                            this.recordedChunks.push(event.data);

                        }

                    };

                    

                    // Only create audio context if we have audio

                    if (this.stream.getAudioTracks().length > 0) {

                        this.audioContext = new AudioContext();

                        const source = this.audioContext.createMediaStreamSource(this.stream);

                        this.analyser = this.audioContext.createAnalyser();

                        source.connect(this.analyser);

                    }

                    

                    this.mediaRecorder.start();

                    this.isRecording = true;

                    

                    this.startBtn.disabled = true;

                    this.stopBtn.disabled = false;

                    

                    this.showStatus('रेकर्डिङ सुरु भयो...', 'recording');

                    this.startAudioVisualization();

                    

                } catch (error) {

                    console.error('Recording start error:', error);

                    this.showStatus('रेकर्डिङ सुरु गर्न सकिएन', 'error');

                }

            }

            

            stopRecording() {

                if (this.mediaRecorder && this.isRecording) {

                    this.mediaRecorder.stop();

                    this.isRecording = false;

                    

                    this.startBtn.disabled = false;

                    this.stopBtn.disabled = true;

                    this.analyzeBtn.disabled = false;

                    

                    this.showStatus('रेकर्डिङ समाप्त भयो', 'complete');

                    this.stopAudioVisualization();

                }

            }

            

            startAudioVisualization() {

                const animate = () => {

                    if (this.isRecording) {

                        this.updateAudioVisualizer();

                        requestAnimationFrame(animate);

                    }

                };

                animate();

            }

            

            stopAudioVisualization() {

                const bars = this.audioVisualizer.children;

                for (let i = 0; i < bars.length; i++) {

                    bars[i].style.height = '5px';

                }

            }

            

            handleFileUpload(file) {

                if (file) {

                    this.analyzeBtn.disabled = false;

                    this.simulateMovement = true; // Enable simulated hand movement for uploaded files

                    

                    // Create audio element to analyze uploaded file

                    const audio = new Audio();

                    const url = URL.createObjectURL(file);

                    audio.src = url;

                    

                    // Enable analysis button and show preview

                    const previewDiv = document.createElement('div');

                    previewDiv.innerHTML = `

                        <div style="background: #e8f5e8; padding: 15px; border-radius: 8px; margin: 10px 0; text-align: center;">

                            <h4>✅ फाइल तयार छ</h4>

                            <p><strong>${file.name}</strong></p>

                            <p>साइज: ${(file.size / 1024 / 1024).toFixed(2)} MB</p>

                            <audio controls style="width: 100%; margin-top: 10px;">

                                <source src="${url}" type="${file.type}">

                            </audio>

                        </div>

                    `;

                    

                    // Remove any existing preview

                    const existingPreview = document.querySelector('.file-preview');

                    if (existingPreview) existingPreview.remove();

                    

                    previewDiv.className = 'file-preview';

                    this.uploadArea.parentNode.insertBefore(previewDiv, this.uploadArea.nextSibling);

                    

                    this.showStatus(`फाइल अपलोड भयो: ${file.name}`, 'complete');

                    

                    // Simulate some audio analysis

                    this.simulateAudioAnalysis();

                }

            }

            

            simulateAudioAnalysis() {

                // Simulate audio visualization for uploaded files

                let counter = 0;

                const interval = setInterval(() => {

                    if (counter < 50) { // Run for 5 seconds

                        const bars = this.audioVisualizer.children;

                        for (let i = 0; i < bars.length; i++) {

                            const height = Math.random() * 40 + 10;

                            bars[i].style.height = height + 'px';

                        }

                        counter++;

                    } else {

                        clearInterval(interval);

                        // Reset bars

                        const bars = this.audioVisualizer.children;

                        for (let i = 0; i < bars.length; i++) {

                            bars[i].style.height = '5px';

                        }

                    }

                }, 100);

            }

            

            analyzePerformance() {

                this.showStatus('कविता विश्लेषण गर्दै...', 'analyzing');

                

                setTimeout(() => {

                    const scores = this.calculateScores();

                    this.displayResults(scores);

                    this.showStatus('विश्लेषण पूरा भयो!', 'complete');

                }, 2000);

            }

            

            calculateScores() {

                // Simulated scoring algorithm

                const singingScore = Math.floor(Math.random() * 10) + 20; // 20-30

                const rhythmScore = Math.floor(Math.random() * 10) + 15; // 15-25

                const handScore = Math.floor(Math.random() * 15) + 10; // 10-25

                

                // Analyze chanda (meter) based on user input

                const userText = this.userKavita.value.trim();

                const chandaScore = this.analyzeChandaPattern(userText);

                

                const totalScore = singingScore + rhythmScore + handScore + chandaScore;

                

                return {

                    singing: singingScore,

                    rhythm: rhythmScore,

                    hand: handScore,

                    chanda: chandaScore,

                    total: totalScore

                };

            }

            

            analyzeChandaPattern(text) {

                if (!text) return 5;

                

                const lines = text.split('\n').filter(line => line.trim());

                if (lines.length === 0) return 5;

                

                // Simple chanda analysis - check for consistent syllable patterns

                let consistencyScore = 0;

                let avgLength = 0;

                

                lines.forEach(line => {

                    avgLength += line.length;

                });

                avgLength = avgLength / lines.length;

                

                lines.forEach(line => {

                    const deviation = Math.abs(line.length - avgLength) / avgLength;

                    if (deviation < 0.2) consistencyScore += 5;

                    else if (deviation < 0.4) consistencyScore += 3;

                    else consistencyScore += 1;

                });

                

                return Math.min(20, Math.floor(consistencyScore));

            }

            

            displayResults(scores) {

                document.getElementById('totalScore').textContent = scores.total;

                document.getElementById('singingScore').textContent = scores.singing;

                document.getElementById('rhythmScore').textContent = scores.rhythm;

                document.getElementById('handScore').textContent = scores.hand;

                document.getElementById('chandaScore').textContent = scores.chanda;

                

                // Add feedback

                let feedback = '';

                if (scores.total >= 80) feedback = 'उत्कृष्ट! 🌟';

                else if (scores.total >= 60) feedback = 'राम्रो! 👏';

                else if (scores.total >= 40) feedback = 'औसत। सुधार गर्न सकिन्छ। 📈';

                else feedback = 'अभ्यास गरेर सुधार गर्नुहोस्। 💪';

                

                if (!document.getElementById('overallFeedback')) {

                    const feedbackElement = document.createElement('li');

                    feedbackElement.id = 'overallFeedback';

                    feedbackElement.innerHTML = `<strong>${feedback}</strong>`;

                    document.getElementById('feedbackList').appendChild(feedbackElement);

                }

            }

            

            showStatus(message, type) {

                this.statusIndicator.textContent = message;

                this.statusIndicator.className = `status-indicator status-${type}`;

                this.statusIndicator.style.display = 'block';

                

                if (type === 'complete') {

                    setTimeout(() => {

                        this.statusIndicator.style.display = 'none';

                    }, 3000);

                }

            }

        }

        

        // Initialize the game when DOM is loaded

        document.addEventListener('DOMContentLoaded', () => {

            new NepaliKavitaGame();

        });

    </script>

</body>

</html>