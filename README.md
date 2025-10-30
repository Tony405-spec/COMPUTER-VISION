<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 400" width="1200" height="400">
    <defs>
        <!-- Neon red glow -->
        <filter id="glow">
            <feGaussianBlur stdDeviation="4" result="blur"/>
            <feMerge>
                <feMergeNode in="blur"/>
                <feMergeNode in="SourceGraphic"/>
            </feMerge>
        </filter>

        <!-- Gradient red -->
        <linearGradient id="redgrad" x1="0" y1="0" x2="1" y2="1">
            <stop stop-color="#ff0000"/>
            <stop offset="1" stop-color="#8b0000"/>
        </linearGradient>
    </defs>

    <!-- Background -->
    <rect width="100%" height="100%" fill="black"/>

    <!-- Tech grid -->
    <g stroke="#330000" opacity="0.3">
        <line x1="0" y1="100" x2="1200" y2="100"/>
        <line x1="0" y1="200" x2="1200" y2="200"/>
        <line x1="0" y1="300" x2="1200" y2="300"/>
    </g>

    <!-- T-800 red eye -->
    <circle cx="240" cy="200" r="75" fill="black" stroke="url(#redgrad)" stroke-width="4"/>
    <circle cx="240" cy="200" r="38" fill="url(#redgrad)" filter="url(#glow)"/>

    <!-- Red scanning beam across the eye -->
    <rect x="150" y="195" width="200" height="10" fill="red" filter="url(#glow)">
        <animate attributeName="x" values="150;-50;150" dur="3s" repeatCount="indefinite"/>
    </rect>

    <!-- Main neon title -->
    <text x="520" y="160"
        font-size="46"
        font-family="Orbitron, monospace"
        fill="url(#redgrad)"
        filter="url(#glow)">
        COMPUTER VISION SHORT COURSE
    </text>

    <!-- Subtitle -->
    <text x="520" y="220"
        font-size="20"
        font-family="Orbitron, monospace"
        fill="white"
        opacity="0.7">
        Deep Learning ▪ OpenCV ▪ TensorFlow ▪ PyTorch
    </text>

    <!-- Terminator style status -->
    <text x="520" y="275"
        font-size="14"
        font-family="Courier New, monospace"
        fill="red"
        opacity="0.8">
        STATUS: TRAINING MODELS ▪ CALIBRATING ▪ TARGET LOCKED
    </text>
</svg>
