<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 400" width="1200" height="400" role="img" aria-labelledby="titleDesc">
  <title id="titleDesc">Computer Vision Short Course — Skynet T-800 neon header (GitHub-safe)</title>

  <defs>
    <!-- neon red gradient -->
    <linearGradient id="gRed" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#ff3b3b"/>
      <stop offset="60%" stop-color="#ff0000"/>
      <stop offset="100%" stop-color="#8b0000"/>
    </linearGradient>

    <!-- dark metallic gradient for skull (simple - gradients are permitted) -->
    <linearGradient id="gMetal" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#1a1a1a"/>
      <stop offset="100%" stop-color="#0b0b0b"/>
    </linearGradient>
  </defs>

  <!-- background -->
  <rect width="1200" height="400" fill="#040204"/>

  <!-- subtle horizontal bands for tech vibe -->
  <rect x="0" y="60" width="1200" height="8" fill="#070707" opacity="0.18"/>
  <rect x="0" y="110" width="1200" height="6" fill="#070707" opacity="0.12"/>
  <rect x="0" y="170" width="1200" height="6" fill="#070707" opacity="0.10"/>
  <rect x="0" y="250" width="1200" height="6" fill="#070707" opacity="0.10"/>

  <!-- left: stylized T-800 skull (geometric, no filters) -->
  <g transform="translate(70,30) scale(0.9)">
    <!-- skull base -->
    <path d="M150 40 C 120 40, 80 60, 70 110 C 60 160, 80 270, 150 300 C 220 270, 240 160, 230 110 C 220 60, 180 40, 150 40 Z"
          fill="url(#gMetal)" stroke="#0e0e0e" stroke-width="2"/>

    <!-- jaw -->
    <path d="M110 190 L160 190 L180 230 L120 235 Z" fill="#0b0b0b" />

    <!-- mouth grille -->
    <rect x="115" y="200" width="80" height="8" fill="#111"/>
    <g fill="#151515">
      <rect x="119" y="202" width="8" height="4" rx="1"/>
      <rect x="137" y="202" width="8" height="4" rx="1"/>
      <rect x="155" y="202" width="8" height="4" rx="1"/>
      <rect x="173" y="202" width="8" height="4" rx="1"/>
    </g>

    <!-- forehead circuitry lines -->
    <g stroke="#ff3b3b" stroke-width="1.2" fill="none" opacity="0.95">
      <path d="M110 80 C140 76, 160 84, 188 88"/>
      <path d="M120 100 C150 96, 168 102, 190 106"/>
    </g>

    <!-- right eye socket (glow simulated by layered shapes, not filters) -->
    <g transform="translate(190,120)">
      <circle r="28" fill="#230202" stroke="url(#gRed)" stroke-width="2"/>
      <circle r="20" fill="url(#gRed)"/>
      <circle r="8" fill="#070707"/>
      <!-- subtle scan line -->
      <rect x="-40" y="-1.5" width="80" height="3" fill="#ff4b4b" opacity="0.07"/>
    </g>
  </g>

  <!-- right: camera lens / sensor -->
  <g transform="translate(880,60)">
    <circle cx="0" cy="0" r="60" fill="#060606" stroke="#220000" stroke-width="2"/>
    <circle cx="0" cy="0" r="36" fill="url(#gRed)" opacity="0.18"/>
    <circle cx="0" cy="0" r="12" fill="#ff2b2b" />
    <!-- status LEDs -->
    <circle cx="-14" cy="92" r="4" fill="#ff4b4b"/>
    <circle cx="0" cy="92" r="4" fill="#ff8b8b"/>
    <circle cx="14" cy="92" r="4" fill="#ff1a1a"/>
  </g>

  <!-- title block (neon red text using gradient fill) -->
  <g transform="translate(360,70)">
    <text x="0" y="48" font-family="Orbitron, 'Roboto Mono', monospace" font-size="44" font-weight="700" fill="url(#gRed)">
      COMPUTER VISION
    </text>

    <text x="0" y="96" font-family="Orbitron, 'Roboto Mono', monospace" font-size="26" font-weight="700" fill="#ff7a7a">
      SHORT COURSE • HANDS-ON • PYTORCH / TENSORFLOW
    </text>

    <text x="0" y="140" font-family="Courier, monospace" font-size="14" fill="#ff9b9b" opacity="0.9">
      NEON LABS · SENSORS · MODELS · DEPLOYMENT
    </text>

    <!-- small neon badges -->
    <rect x="0" y="168" width="120" height="28" rx="6" fill="#120000" stroke="#ff1a1a" stroke-width="1"/>
    <text x="12" y="188" font-family="monospace" font-size="12" fill="#ffcfcf">Beginner → Advanced</text>

    <rect x="140" y="168" width="170" height="28" rx="6" fill="#120000" stroke="#ff1a1a" stroke-width="1"/>
    <text x="150" y="188" font-family="monospace" font-size="12" fill="#ffcfcf">Lectures • Labs • Projects</text>

    <rect x="330" y="168" width="160" height="28" rx="6" fill="#120000" stroke="#ff1a1a" stroke-width="1"/>
    <text x="340" y="188" font-family="monospace" font-size="12" fill="#ffcfcf">Repo: cv-short-course</text>
  </g>

  <!-- bottom status line -->
  <g transform="translate(20,360)" font-family="monospace" font-size="11" fill="#ff8b8b" opacity="0.85">
    <text>© Computer Vision Short Course • Designed for educational use</text>
  </g>
</svg>

