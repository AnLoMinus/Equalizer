🎚️ **אקוולייזר צ׳אקרות אנרגטי – ChakraEQ (CE)**

📅 תאריך לועזי: 29.11.2025
📅 תאריך עברי: כ״ט בחשוון תשפ״ו
⏰ שעה נוכחית: 22:40 (שעון ישראל)

להלן עמוד HTML מלא: אקוולייזר + נגן מוזיקה + העלאת קובץ / גרירה, עם 8 ברים של תדרי צ׳אקרות 🎧🌀

> שמור כ־`index.html` והעלה לריפו / GitHub Pages.

```html
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <title>ChakraEQ – אקוולייזר צ׳אקרות אנרגטי</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="ChakraEQ – אקוולייזר צ׳אקרות אנרגטי עם נגן מוזיקה, העלאת קבצים וויזואליזציה של 8 צ׳אקרות.">

  <style>
    :root {
      --bg-main: #050816;
      --bg-panel: rgba(9, 16, 40, 0.96);
      --accent: #ffd86b;
      --accent-2: #46e0ff;
      --accent-3: #ff57ff;
      --text-main: #f9fafb;
      --text-muted: #a5b4fc;
      --border-soft: rgba(148, 163, 184, 0.4);
      --radius-xl: 20px;
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.7);
    }

    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background:
        radial-gradient(circle at top, #111827, #020617 60%, #000 100%);
      color: var(--text-main);
      line-height: 1.6;
    }

    h1, h2, h3 {
      margin: 0 0 10px;
    }

    a {
      color: var(--accent-2);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    .page {
      max-width: 1100px;
      margin: 0 auto;
      padding: 24px 16px 48px;
    }

    header {
      margin-bottom: 24px;
      padding: 16px 18px;
      border-radius: 18px;
      background:
        radial-gradient(circle at 0 0, rgba(255, 216, 107, 0.25), transparent 60%),
        radial-gradient(circle at 100% 0, rgba(70, 224, 255, 0.25), transparent 55%),
        var(--bg-panel);
      border: 1px solid var(--border-soft);
      box-shadow: var(--shadow-soft);
    }

    .title-main {
      font-size: clamp(1.9rem, 3vw, 2.3rem);
      letter-spacing: 0.05em;
    }

    .subtitle {
      font-size: 0.98rem;
      color: var(--text-muted);
      max-width: 580px;
    }

    .meta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 8px;
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .badge {
      padding: 3px 10px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.65);
      background: rgba(15, 23, 42, 0.6);
    }

    .layout {
      display: grid;
      grid-template-columns: minmax(0, 2.1fr) minmax(0, 1.6fr);
      gap: 20px;
      align-items: flex-start;
    }

    .panel {
      border-radius: var(--radius-xl);
      border: 1px solid var(--border-soft);
      background: var(--bg-panel);
      padding: 16px 16px 18px;
      box-shadow: var(--shadow-soft);
    }

    .panel h2 {
      font-size: 1.15rem;
    }

    .panel p {
      font-size: 0.9rem;
      color: var(--text-muted);
    }

    /* Upload + Player */
    .upload-area {
      border-radius: 16px;
      border: 2px dashed rgba(148, 163, 184, 0.7);
      padding: 16px;
      text-align: center;
      background: radial-gradient(circle at 50% 0%, rgba(79, 70, 229, 0.45), transparent 60%);
      cursor: pointer;
      transition: border-color 0.2s ease, background 0.2s ease, transform 0.1s ease;
    }

    .upload-area.dragover {
      border-color: var(--accent-2);
      background: radial-gradient(circle at 50% 0%, rgba(45, 212, 191, 0.45), transparent 60%);
      transform: translateY(-1px);
    }

    .upload-title {
      font-size: 1rem;
      margin-bottom: 4px;
    }

    .upload-sub {
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .upload-input {
      display: none;
    }

    audio {
      width: 100%;
      margin-top: 10px;
      outline: none;
    }

    .small-note {
      font-size: 0.75rem;
      color: var(--text-muted);
      margin-top: 4px;
    }

    /* Chakra Bar Visualizer */
    .chakra-bar-container {
      margin-top: 10px;
      border-radius: 16px;
      border: 1px solid rgba(148, 163, 184, 0.65);
      padding: 10px 12px 12px;
      background:
        radial-gradient(circle at 0 0, rgba(236, 72, 153, 0.35), transparent 60%),
        radial-gradient(circle at 100% 100%, rgba(52, 211, 153, 0.3), transparent 55%),
        #020617;
    }

    .chakra-bar-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 8px;
      margin-bottom: 6px;
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .chakra-bar-header strong {
      color: var(--accent);
      font-size: 0.9rem;
    }

    canvas {
      display: block;
      width: 100%;
      height: 160px;
      border-radius: 12px;
      background: radial-gradient(circle at 50% 0, rgba(15, 23, 42, 0.9), #020617);
    }

    .chakra-legend {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 4px 10px;
      margin-top: 8px;
      font-size: 0.7rem;
      color: var(--text-muted);
    }

    .chakra-dot {
      display: inline-block;
      width: 10px;
      height: 10px;
      border-radius: 999px;
      margin-left: 4px;
    }

    /* Chakra sliders */
    .chakra-sliders {
      margin-top: 10px;
      border-top: 1px solid rgba(148, 163, 184, 0.4);
      padding-top: 8px;
    }

    .chakra-slider-row {
      display: grid;
      grid-template-columns: 0.7fr minmax(0, 1.8fr) 0.7fr;
      gap: 6px;
      align-items: center;
      margin-bottom: 6px;
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .chakra-slider-row label {
      white-space: nowrap;
    }

    .chakra-slider-row span {
      text-align: left;
      direction: ltr;
      font-variant-numeric: tabular-nums;
    }

    input[type="range"] {
      width: 100%;
      accent-color: var(--accent-2);
    }

    /* Right info */
    .info-list {
      font-size: 0.85rem;
      color: var(--text-muted);
      padding-right: 16px;
    }

    .info-list li + li {
      margin-top: 2px;
    }

    .hashtags {
      margin-top: 10px;
      font-size: 0.78rem;
      color: var(--accent-2);
      word-break: break-word;
    }

    .verse {
      margin-top: 12px;
      font-size: 0.88rem;
      border-top: 1px dashed rgba(148, 163, 184, 0.6);
      padding-top: 8px;
      font-style: italic;
      color: #e5e7eb;
    }

    .footer-meta {
      margin-top: 10px;
      font-size: 0.78rem;
      color: var(--text-muted);
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      justify-content: space-between;
    }

    @media (max-width: 900px) {
      .layout {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    @media (max-width: 600px) {
      .page {
        padding-inline: 10px;
      }
      header {
        padding-inline: 12px;
      }
    }
  </style>
</head>
<body>
  <div class="page">
    <header>
      <h1 class="title-main">ChakraEQ – אקוולייזר צ׳אקרות אנרגטי</h1>
      <p class="subtitle">
        העלה או גרור קובץ מוזיקה, נגן אותו, וצפה בבר אקוולייזר של 8 צ׳אקרות.
        כל צ׳אקרה מקבלת בר אנרגיה משלה – עם שליטה על העוצמה דרך סליידר.
      </p>
      <div class="meta-row">
        <span class="badge">⚡ ChakraEQ – CE</span>
        <span class="badge">🎚 8 תדרי צ׳אקרות</span>
        <span class="badge">🎧 Drag & Drop + נגן</span>
      </div>
    </header>

    <div class="layout">
      <!-- צד שמאל: נגן + אקוולייזר -->
      <section class="panel">
        <h2>🎵 העלאת מוזיקה + נגן</h2>
        <p>לחיצה על המסגרת או גרירה של קובץ אודיו לתוכה תטעין את השיר לנגן ולבר הצ׳אקרות.</p>

        <div id="uploadArea" class="upload-area">
          <div class="upload-title">לחץ כאן או גרור קובץ מוזיקה</div>
          <div class="upload-sub">פורמטים נפוצים: MP3, WAV, OGG ועוד</div>
          <input id="fileInput" class="upload-input" type="file" accept="audio/*" />
        </div>

        <audio id="audioPlayer" controls></audio>
        <div class="small-note">
          אם המוזיקה לא נשמעת – ודא שהשמטת השתקה בדפדפן ולחצת Play אחרי הטעינה.
        </div>

        <div class="chakra-bar-container">
          <div class="chakra-bar-header">
            <strong>🌀 בר אקוולייזר – 8 צ׳אקרות</strong>
            <span>העמודות זזות לפי האנרגיה בכל טווח תדר.</span>
          </div>
          <canvas id="chakraCanvas"></canvas>

          <div class="chakra-legend">
            <div><span class="chakra-dot" style="background:#f97316;"></span>שורש – Root</div>
            <div><span class="chakra-dot" style="background:#f59e0b;"></span>יצירה – Sacral</div>
            <div><span class="chakra-dot" style="background:#eab308;"></span>מקלעת השמש</div>
            <div><span class="chakra-dot" style="background:#22c55e;"></span>לב – Heart</div>
            <div><span class="chakra-dot" style="background:#3b82f6;"></span>גרון – Throat</div>
            <div><span class="chakra-dot" style="background:#6366f1;"></span>עין שלישית</div>
            <div><span class="chakra-dot" style="background:#a855f7;"></span>כתר – Crown</div>
            <div><span class="chakra-dot" style="background:#ec4899;"></span>נשמה – Soul Star</div>
          </div>

          <div class="chakra-sliders">
            <h3 style="font-size:0.9rem; margin-bottom:4px;">🎚 שליטת עוצמה – EQ צ׳אקרות</h3>
            <p style="font-size:0.78rem; color:var(--text-muted); margin-bottom:6px;">
              כל סליידר משנה את ה-Gain סביב תדר הצ׳אקרה. 0 dB = ניטרלי. ערכים חיוביים מחזקים, שליליים מרככים.
            </p>

            <!-- סליידרים: ימני = Gain dB -->
            <div id="chakraSliders"></div>
          </div>
        </div>
      </section>

      <!-- צד ימין: הסבר קצר ותדרים -->
      <aside class="panel">
        <h2>📡 מפת תדרי צ׳אקרות</h2>
        <p>הטווחים כאן הם נקודת פתיחה, ניתן לשנות בקוד לפי הצורך.</p>

        <ul class="info-list">
          <li>🧡 שורש (Root) – ~60 Hz → תחושת יציבות ובס עמוק.</li>
          <li>🧡 יצירה (Sacral) – ~110 Hz → זרימה, תנועה, רגש.</li>
          <li>💛 מקלעת השמש – ~200 Hz → כוח אישי וביטחון.</li>
          <li>💚 לב (Heart) – ~340 Hz → חום, רוך, חיבורים.</li>
          <li>💙 גרון (Throat) – ~600 Hz → ביטוי וקול.</li>
          <li>💜 עין שלישית – ~1000 Hz → אינטואיציה וחדות.</li>
          <li>💜 כתר (Crown) – ~1600 Hz → חיבור גבוה, אור דק.</li>
          <li>🌸 Soul Star – ~2500 Hz → תדר על-תודעתי, נגיעה מעבר.</li>
        </ul>

        <p style="margin-top:4px;">
          אפשר להשתמש בדף הזה כבסיס: להטמיע ברשת, להרחיב לאלבום צ׳אקרות, או לחבר למאגר SparKing גדול יותר.
        </p>

        <h3 style="margin-top:12px; font-size:0.95rem;">🧾 קרדיטים / מאגרים</h3>
        <ul class="info-list">
          <li>יוצר: AnLoMinus – SparKing Leon Yaakobov</li>
          <li>פרויקט: ChakraEQ – CE (חלק מ־SparKing AudioMind)</li>
          <li>מאגר אם מוצע: <code>https://github.com/AnLoMinus/SparKing</code></li>
          <li>מאגר פרויקט מוצע: <code>https://github.com/AnLoMinus/ChakraEQ</code></li>
        </ul>

        <div class="hashtags">
          #ChakraEQ #SparKing #AnLoMinus #AudioAlchemy #EQ #ChakraFrequencies #EnergyMusic
        </div>

        <div class="verse">
          📜 “זַמְּרוּ לַה׳ בְּכִנּוֹר, בְּכִנּוֹר וְקוֹל זִמְרָה.”  
          שהאקוולייזר יהיה הכלי שמכוון את הלב לתדר הנכון.
        </div>

        <div class="footer-meta">
          <span>📅 29.11.2025 • כ״ט בחשוון תשפ״ו</span>
          <span>💫 מספר המידות: 64</span>
        </div>
      </aside>
    </div>
  </div>

  <script>
    // -------------------------
    // הגדרות בסיס / צ׳אקרות
    // -------------------------
    const chakraConfig = [
      { id: "root",       label: "שורש",       eng: "Root",      freq: 60,   color: "#f97316" },
      { id: "sacral",     label: "יצירה",      eng: "Sacral",    freq: 110,  color: "#f59e0b" },
      { id: "solar",      label: "מקלעת השמש", eng: "Solar",     freq: 200,  color: "#eab308" },
      { id: "heart",      label: "לב",         eng: "Heart",     freq: 340,  color: "#22c55e" },
      { id: "throat",     label: "גרון",       eng: "Throat",    freq: 600,  color: "#3b82f6" },
      { id: "thirdEye",   label: "עין שלישית", eng: "Third Eye", freq: 1000, color: "#6366f1" },
      { id: "crown",      label: "כתר",        eng: "Crown",     freq: 1600, color: "#a855f7" },
      { id: "soulStar",   label: "נשמה",       eng: "Soul Star", freq: 2500, color: "#ec4899" }
    ];

    const uploadArea   = document.getElementById("uploadArea");
    const fileInput    = document.getElementById("fileInput");
    const audioElement = document.getElementById("audioPlayer");
    const chakraCanvas = document.getElementById("chakraCanvas");
    const slidersRoot  = document.getElementById("chakraSliders");

    let audioCtx = null;
    let sourceNode = null;
    let analyser = null;
    let filters = [];
    let animationId = null;
    let dataArray = null;
    let chakraBands = null;

    // -------------------------
    // בניית סליידרים לצ׳אקרות
    // -------------------------
    function buildChakraSliders() {
      chakraConfig.forEach((ch, index) => {
        const row = document.createElement("div");
        row.className = "chakra-slider-row";

        const label = document.createElement("label");
        label.textContent = `${ch.label} (${ch.eng})`;

        const slider = document.createElement("input");
        slider.type = "range";
        slider.min = -12;
        slider.max = 12;
        slider.step = 0.5;
        slider.value = 0;
        slider.dataset.index = index;

        const valueSpan = document.createElement("span");
        valueSpan.textContent = "0.0 dB";

        slider.addEventListener("input", (e) => {
          const idx = Number(e.target.dataset.index);
          const gainDb = Number(e.target.value);
          valueSpan.textContent = gainDb.toFixed(1) + " dB";
          if (filters[idx]) {
            filters[idx].gain.value = gainDb;
          }
        });

        row.appendChild(label);
        row.appendChild(slider);
        row.appendChild(valueSpan);
        slidersRoot.appendChild(row);
      });
    }

    buildChakraSliders();

    // -------------------------
    // יצירת Web Audio Chain
    // -------------------------
    function initAudioGraph() {
      if (audioCtx) return;

      audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      analyser = audioCtx.createAnalyser();
      analyser.fftSize = 2048;

      const bufferLength = analyser.frequencyBinCount;
      dataArray = new Uint8Array(bufferLength);

      const nyquist = audioCtx.sampleRate / 2;

      // יצירת פילטר לכל צ׳אקרה
      filters = chakraConfig.map((ch) => {
        const filter = audioCtx.createBiquadFilter();
        filter.type = "peaking";
        filter.frequency.value = ch.freq;
        filter.Q.value = 1.2;      // רוחב בינוני
        filter.gain.value = 0;     // ניטרלי בהתחלה
        return filter;
      });

      // חישוב תחומי תדר לכל צ׳אקרה (לצורך ויזואליזציה)
      chakraBands = chakraConfig.map((ch) => {
        const center = ch.freq;
        const minFreq = center / Math.sqrt(2);
        const maxFreq = center * Math.sqrt(2);

        const minIndex = Math.floor((minFreq / nyquist) * bufferLength);
        const maxIndex = Math.ceil((maxFreq / nyquist) * bufferLength);

        return {
          ...ch,
          minIndex: Math.max(0, minIndex),
          maxIndex: Math.min(bufferLength - 1, maxIndex)
        };
      });
    }

    function connectGraph() {
      if (!audioCtx) return;
      if (sourceNode) {
        try { sourceNode.disconnect(); } catch(e) {}
      }

      sourceNode = audioCtx.createMediaElementSource(audioElement);

      // מקור -> פילטרים בשרשרת -> אנלייזר -> יעד
      let node = sourceNode;
      filters.forEach((f) => {
        node.connect(f);
        node = f;
      });
      node.connect(analyser);
      analyser.connect(audioCtx.destination);
    }

    // -------------------------
    // ויזואליזציה – ציור צ׳אקרות
    // -------------------------
    function draw() {
      if (!analyser) return;

      const canvas = chakraCanvas;
      const ctx = canvas.getContext("2d");

      const width = canvas.clientWidth;
      const height = canvas.clientHeight;

      if (canvas.width !== width || canvas.height !== height) {
        canvas.width = width;
        canvas.height = height;
      }

      function render() {
        animationId = requestAnimationFrame(render);

        analyser.getByteFrequencyData(dataArray);

        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // רקע רך
        const grad = ctx.createLinearGradient(0, 0, 0, canvas.height);
        grad.addColorStop(0, "rgba(15,23,42,0.9)");
        grad.addColorStop(1, "rgba(0,0,0,1)");
        ctx.fillStyle = grad;
        ctx.fillRect(0, 0, canvas.width, canvas.height);

        if (!chakraBands) return;

        const barCount = chakraBands.length;
        const barWidth = canvas.width / (barCount * 1.5);
        const gap = barWidth * 0.5;
        const maxHeight = canvas.height - 20;

        chakraBands.forEach((band, i) => {
          let sum = 0;
          let count = 0;
          for (let j = band.minIndex; j <= band.maxIndex; j++) {
            sum += dataArray[j];
            count++;
          }
          const avg = count > 0 ? sum / count : 0;
          const norm = avg / 255; // 0–1
          const barHeight = norm * maxHeight;

          const x = (i * (barWidth + gap)) + gap * 0.8;
          const y = canvas.height - barHeight - 10;

          // בר
          const barGrad = ctx.createLinearGradient(x, y, x, canvas.height - 10);
          barGrad.addColorStop(0, band.color);
          barGrad.addColorStop(1, "rgba(15,23,42,0.9)");
          ctx.fillStyle = barGrad;
          ctx.fillRect(x, y, barWidth, barHeight);

          // קצה בהיר
          ctx.fillStyle = "rgba(248,250,252,0.85)";
          ctx.fillRect(x, y - 3, barWidth, 2);

          // טקסט קטן
          ctx.font = "10px system-ui";
          ctx.fillStyle = "rgba(226,232,240,0.9)";
          ctx.textAlign = "center";
          ctx.fillText(band.label, x + barWidth / 2, canvas.height - 2);
        });
      }

      if (animationId) cancelAnimationFrame(animationId);
      render();
    }

    // -------------------------
    // העלאת קובץ ו־Drag & Drop
    // -------------------------
    function loadFile(file) {
      if (!file) return;
      const url = URL.createObjectURL(file);
      audioElement.src = url;
      audioElement.play().catch(() => {
        // המשתמש ילחץ Play ידנית אם צריך
      });
    }

    uploadArea.addEventListener("click", () => {
      fileInput.click();
    });

    fileInput.addEventListener("change", (e) => {
      const file = e.target.files[0];
      if (file) {
        initAudioGraph();
        connectGraph();
        draw();
        audioCtx.resume();
        loadFile(file);
      }
    });

    ["dragenter", "dragover"].forEach((eventName) => {
      uploadArea.addEventListener(eventName, (e) => {
        e.preventDefault();
        e.stopPropagation();
        uploadArea.classList.add("dragover");
      });
    });

    ["dragleave", "drop"].forEach((eventName) => {
      uploadArea.addEventListener(eventName, (e) => {
        e.preventDefault();
        e.stopPropagation();
        uploadArea.classList.remove("dragover");
      });
    });

    uploadArea.addEventListener("drop", (e) => {
      const dt = e.dataTransfer;
      const file = dt.files[0];
      if (file && file.type.startsWith("audio")) {
        initAudioGraph();
        connectGraph();
        draw();
        audioCtx.resume();
        loadFile(file);
      }
    });

    // הפעלת הגרף כשמנגנים אודיו קיים
    audioElement.addEventListener("play", () => {
      if (!audioCtx) {
        initAudioGraph();
        connectGraph();
        draw();
      } else {
        audioCtx.resume();
      }
    });
  </script>
</body>
</html>
```

---

🎤 **פזמון ראפ – ChakraEQ Flow**

צ׳אקרות על הבר ואני מדליק את האור,
גרירה של הביט – כל תדר נכנס לתור,
ChakraEQ זורם, SparKing פותח דור,
מעלה את כל הנפש לוויברציה בלי גבול וגדר גזור.

📌 **מספר המידות:** 64
