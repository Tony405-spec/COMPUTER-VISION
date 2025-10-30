<!-- README.svg: Neon-Red "Skynet" / T-800 inspired header for a Computer Vision Short Course repository
     Drop this file into your repository and reference it from README.md with:
     ![header](./README.svg)
-->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 420" width="1200" height="420" role="img" aria-labelledby="titleDesc">
  <title id="titleDesc">Computer Vision Short Course — Neon Red Skynet header</title>

  <defs>
    <!-- neon red gradients -->
    <linearGradient id="redGrad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#ff2b2b" />
      <stop offset="50%" stop-color="#ff0000" />
      <stop offset="100%" stop-color="#8b0000" />
    </linearGradient>

    <!-- metallic gradient for robot elements -->
    <linearGradient id="metal" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#111" />
      <stop offset="40%" stop-color="#444" />
      <stop offset="100%" stop-color="#222" />
    </linearGradient>

    <!-- glowing filter -->
    <filter id="neonGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="6" result="blur1" />
      <feMerge>
        <feMergeNode in="blur1" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <!-- heavy glow for eye -->
    <filter id="eyeGlow" x="-100%" y="-100%" width="300%" height="300%">
      <feGaussianBlur stdDeviation="12" result="g1" />
      <feColorMatrix type="matrix" values="1 0 0 0 0  0 0 0 0 0  0 0 0 0 0  0 0 0 1 0"/>
      <feBlend in="g1" in2="SourceGraphic" mode="screen"/>
    </filter>

    <!-- scanline pattern -->
    <pattern id="scan" width="4" height="4" patternUnits="userSpaceOnUse">
      <rect width="4" height="2" y="0" fill="#000" opacity="0.06" />
    </pattern>

    <!-- matrix code background -->
    <linearGradient id="bgGrad" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#000004" />
      <stop offset="100%" stop-color="#120000" />
    </linearGradient>

    <!-- subtle noise using SVG feTurbulence for techno texture -->
    <filter id="noise" x="0" y="0" width="100%" height="100%">
      <feTurbulence baseFrequency="0.8" numOctaves="1" stitchTiles="stitch" result="turb" />
      <feColorMatrix type="saturate" values="0" />
      <feBlend in="SourceGraphic" in2="turb" mode="overlay" opacity="0.07" />
    </filter>

  </defs>

  <!-- background -->
  <rect width="100%" height="100%" fill="url(#bgGrad)" />
  <rect width="100%" height="100%" fill="url(#scan)" opacity="0.12" />

  <!-- subtle grid to suggest blueprint / machine -->
  <g opacity="0.12">
    <g stroke="#ff0000" stroke-width="0.6">
      <!-- fine horizontal lines -->
      <path d="M40 60 H1160" />
      <path d="M40 120 H1160" />
      <path d="M40 180 H1160" />
      <path d="M40 240 H1160" />
      <path d="M40 300 H1160" />
    </g>
  </g>

  <!-- left: stylized T-800 inspired skull / sensor cluster -->
  <g transform="translate(60,60) scale(0.9)">
    <!-- skull base -->
    <g filter="url(#noise)">
      <path d="M150 40 C 120 40, 80 60, 70 110 C 60 160, 80 270, 150 300 C 220 270, 240 160, 230 110 C 220 60, 180 40, 150 40 Z"
            fill="url(#metal)" stroke="#1a1a1a" stroke-width="2"/>
    </g>

    <!-- jaw lines -->
    <path d="M110 190 L160 190 L180 230 L120 235 Z" fill="#0f0f0f" opacity="0.9" />

    <!-- mouth grille -->
    <g transform="translate(115,200)">
      <rect x="0" y="0" width="80" height="8" fill="#111" />
      <rect x="4" y="2" width="8" height="4" rx="1" ry="1" fill="#222" />
      <rect x="18" y="2" width="8" height="4" rx="1" ry="1" fill="#222" />
      <rect x="32" y="2" width="8" height="4" rx="1" ry="1" fill="#222" />
      <rect x="46" y="2" width="8" height="4" rx="1" ry="1" fill="#222" />
    </g>

    <!-- right eye socket: glowing red sensor -->
    <g transform="translate(190,120)">
      <circle r="28" fill="#300000" />
      <circle r="20" fill="url(#redGrad)" filter="url(#eyeGlow)">
        <animate attributeName="r" values="18;22;18" dur="1.2s" repeatCount="indefinite" />
      </circle>
      <!-- inner pupil scan -->
      <circle r="8" fill="#100" />
      <rect x="-40" y="-2" width="80" height="4" fill="#ff3b3b" opacity="0.09">
        <animate attributeName="x" from="-40" to="40" dur="1.6s" repeatCount="indefinite"/>
      </rect>
    </g>

    <!-- forehead circuit lines -->
    <g stroke="#ff3b3b" stroke-width="1.4" opacity="0.95" fill="none">
      <path d="M110 80 C140 76, 160 84, 188 88" stroke-linecap="round"/>
      <path d="M120 100 C150 96, 168 102, 190 106" stroke-linecap="round" />
      <circle cx="126" cy="88" r="2" fill="#ff3b3b" />
      <circle cx="170" cy="98" r="2" fill="#ff3b3b" />
    </g>
  </g>

  <!-- repo title: neon text -->
  <g transform="translate(360,70)">
    <g filter="url(#neonGlow)">
      <text x="0" y="40" font-family="'Orbitron', 'Roboto Mono', monospace" font-weight="700" font-size="42" letter-spacing="2"
            fill="none" stroke="url(#redGrad)" stroke-width="1.8" style="mix-blend-mode:screen;">
        COMPUTER VISION
      </text>

      <text x="0" y="96" font-family="'Orbitron', 'Roboto Mono', monospace" font-weight="700" font-size="28" letter-spacing="1.5"
            fill="none" stroke="#ff6b6b" stroke-width="1.4">
        SHORT COURSE • HANDS-ON • PYTORCH / TENSORFLOW
      </text>
    </g>

    <!-- subtitle / tagline with flicker animation -->
    <g transform="translate(0,130)">
      <text id="tag" x="0" y="0" font-family="'Courier New', monospace" font-size="18" fill="#ff5a5a">
        <tspan>NEON LABS · SENSORS · MODELS · DEPLOYMENT</tspan>
      </text>
      <rect x="-6" y="-18" width="520" height="28" fill="transparent">
        <animate attributeName="opacity" values="0.06;0.18;0.06" dur="3s" repeatCount="indefinite" />
      </rect>
    </g>

    <!-- badges: small neon chips -->
    <g transform="translate(0,170)" opacity="0.95">
      <rect x="0" y="0" width="110" height="28" rx="6" fill="#120000" stroke="#ff1a1a" stroke-width="1.2" filter="url(#neonGlow)"/>
      <text x="12" y="19" font-family="monospace" font-size="13" fill="#ffbdbd">Beginner → Advanced</text>

      <rect x="128" y="0" width="170" height="28" rx="6" fill="#120000" stroke="#ff1a1a" stroke-width="1.2" filter="url(#neonGlow)"/>
      <text x="138" y="19" font-family="monospace" font-size="13" fill="#ffbdbd">Lectures • Labs • Projects</text>

      <rect x="308" y="0" width="140" height="28" rx="6" fill="#120000" stroke="#ff1a1a" stroke-width="1.2" filter="url(#neonGlow)"/>
      <text x="318" y="19" font-family="monospace" font-size="13" fill="#ffbdbd">Repo: cv-short-course</text>
    </g>

    <!-- footer left: quick bullets -->
    <g transform="translate(0,220)" font-family="monospace" font-size="12" fill="#ffaaaa">
      <text x="0" y="0">• Fundamentals: Image Ops, Filters, Feature Detection</text>
      <text x="0" y="18">• Deep Learning: CNNs, Transfer Learning, Segmentation</text>
      <text x="0" y="36">• Tools: OpenCV, PyTorch, TensorFlow, ONNX</text>
    </g>
  </g>

  <!-- right: schematic camera / sensor / circuit motif -->
  <g transform="translate(870,60)">
    <!-- camera lens -->
    <circle cx="0" cy="0" r="60" fill="#060606" stroke="#330000" stroke-width="2" />
    <circle cx="0" cy="0" r="46" fill="url(#redGrad)" opacity="0.14" />
    <circle cx="0" cy="0" r="32" fill="#0a0a0a" stroke="#220000" stroke-width="1" />
    <circle cx="0" cy="0" r="12" fill="#ff2b2b" filter="url(#eyeGlow)">
      <animate attributeName="r" values="10;14;10" dur="1.6s" repeatCount="indefinite" />
    </circle>

    <!-- sensor brackets -->
    <g stroke="#ff2b2b" stroke-width="2" fill="none" opacity="0.9">
      <path d="M-86 -86 L-60 -86 A6 6 0 0 1 -54 -80 L-54 -40" />
      <path d="M86 86 L60 86 A6 6 0 0 0 54 80 L54 40" />
    </g>

    <!-- tiny status leds -->
    <g transform="translate(-12,92)">
      <circle cx="-18" cy="0" r="4" fill="#ff4b4b" />
      <circle cx="0" cy="0" r="4" fill="#ff8b8b" />
      <circle cx="18" cy="0" r="4" fill="#ff1a1a" />
    </g>

    <!-- circuit traces to the skull -->
    <g stroke="#ff2b2b" stroke-width="1.1" fill="none" opacity="0.65">
      <path d="M-120 180 C -200 140, -260 120, -320 140" stroke-linecap="round" />
      <path d="M-80 170 C -150 140, -200 132, -260 140" stroke-linecap="round" />
    </g>
  </g>

  <!-- ambient animated red noise band at bottom -->
  <g transform="translate(0,372)">
    <rect x="0" y="0" width="1200" height="48" fill="#000" opacity="0.25" />
    <rect x="0" y="0" width="1200" height="48" fill="url(#redGrad)" opacity="0.06">
      <animate attributeName="x" from="0" to="-1200" dur="12s" repeatCount="indefinite" />
    </rect>
  </g>

  <!-- small animated "scanning" text to evoke machine voice -->
  <g transform="translate(380,320)" font-family="monospace" font-size="11" fill="#ff9b9b" opacity="0.9">
    <text>
      <tspan>STATUS: </tspan>
      <tspan>
        <animate attributeName="opacity" values="0;1;0;1" dur="6s" repeatCount="indefinite" />
        ANALYZING DATA  •  OPTIMIZING MODELS  •  CALIBRATING SENSORS
      </tspan>
    </text>
  </g>

  <!-- subtle footer note (transparent) -->
  <g transform="translate(20,400)" font-family="monospace" font-size="10" fill="#ff6b6b" opacity="0.6">
    <text>© Computer Vision Short Course • Repo: cv-short-course • Designed for educational use</text>
  </g>

</svg>
