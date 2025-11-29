🎚️ **אומנות האקוולייזר – ToneCraft (TC)**

📅 תאריך לועזי: 29.11.2025
📅 תאריך עברי: ט׳ בכסלו תשפ״ו
⏰ שעה נוכחית: 22:17 (שעון ישראל)

להלן קובץ `index.html` מלא בעברית, מוכן להעלאה לריפו GitHub ולהרצה על GitHub Pages:

```html
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>אומנות האקוולייזר – ToneCraft (TC)</title>
  <meta name="description" content="ToneCraft – אומנות האקוולייזר: מדריך מלא בעברית למפיקים, זמרים ואולפן ביתי." />

  <style>
    :root {
      --bg-main: #050816;
      --bg-panel: rgba(9, 16, 40, 0.9);
      --accent: #ffcc4d;
      --accent-2: #44e0ff;
      --accent-3: #ff57ff;
      --text-main: #f5f5f5;
      --text-muted: #a6b0c3;
      --border-soft: rgba(255, 255, 255, 0.08);
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.65);
      --radius-xl: 20px;
      --max-width: 1100px;
    }

    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #171c3f, #050816 55%, #02030a 100%);
      color: var(--text-main);
      line-height: 1.7;
    }

    a {
      color: var(--accent-2);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    /* Top Nav */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(16px);
      background: linear-gradient(
        90deg,
        rgba(5, 8, 22, 0.96),
        rgba(10, 18, 42, 0.9),
        rgba(5, 8, 22, 0.96)
      );
      border-bottom: 1px solid var(--border-soft);
    }

    .nav-inner {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 10px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
    }

    .logo-wrap {
      display: flex;
      align-items: center;
      gap: 10px;
      white-space: nowrap;
    }

    .logo-circle {
      width: 34px;
      height: 34px;
      border-radius: 999px;
      background: radial-gradient(circle at 20% 0%, #ffe885, #ff9b4a 40%, #ff57ff 80%, #4bd5ff 100%);
      box-shadow:
        0 0 18px rgba(255, 204, 77, 0.7),
        0 0 36px rgba(68, 224, 255, 0.5);
    }

    .logo-text-main {
      font-weight: 700;
      letter-spacing: 0.04em;
      font-size: 0.95rem;
      text-transform: uppercase;
    }

    .logo-text-sub {
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: flex-start;
      gap: 10px;
      font-size: 0.8rem;
    }

    nav a {
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid transparent;
      color: var(--text-muted);
      text-decoration: none;
      transition: all 0.2s ease;
    }

    nav a:hover {
      border-color: var(--accent-2);
      color: var(--accent-2);
      background: rgba(68, 224, 255, 0.06);
    }

    /* Layout */
    main {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 20px 20px 60px;
    }

    section {
      margin: 32px 0;
    }

    h1, h2, h3 {
      letter-spacing: 0.03em;
    }

    h1 {
      font-size: clamp(2.2rem, 3vw, 2.7rem);
      margin-bottom: 12px;
    }

    h2 {
      font-size: clamp(1.4rem, 2.3vw, 1.7rem);
      margin: 0 0 10px;
    }

    h3 {
      font-size: 1.05rem;
      margin: 18px 0 6px;
    }

    p {
      margin: 6px 0 10px;
      color: var(--text-muted);
    }

    .hero {
      margin-top: 18px;
      display: grid;
      grid-template-columns: minmax(0, 3fr) minmax(0, 2.4fr);
      gap: 24px;
      align-items: stretch;
    }

    .hero-left {
      padding: 24px 24px 22px;
      border-radius: var(--radius-xl);
      background:
        radial-gradient(circle at 0% 0%, rgba(255, 204, 77, 0.16), transparent 55%),
        radial-gradient(circle at 100% 0%, rgba(68, 224, 255, 0.16), transparent 50%),
        var(--bg-panel);
      box-shadow: var(--shadow-soft);
      border: 1px solid var(--border-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-pill {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 4px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.18);
      font-size: 0.75rem;
      color: var(--text-muted);
      background: rgba(3, 7, 18, 0.6);
      margin-bottom: 10px;
    }

    .hero-sub {
      font-size: 0.95rem;
      max-width: 90%;
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 10px;
    }

    .tag {
      font-size: 0.7rem;
      padding: 4px 9px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.35);
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.06em;
    }

    .hero-right {
      border-radius: var(--radius-xl);
      border: 1px solid var(--border-soft);
      background:
        radial-gradient(circle at 50% 0%, rgba(255, 87, 255, 0.26), transparent 65%),
        radial-gradient(circle at 90% 90%, rgba(68, 224, 255, 0.22), transparent 60%),
        #050818;
      box-shadow: var(--shadow-soft);
      padding: 18px 18px 16px;
      position: relative;
      overflow: hidden;
    }

    .hero-card-title {
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 0.15em;
      color: var(--text-muted);
      margin-bottom: 6px;
    }

    .hero-card-main {
      font-size: 1.05rem;
      margin-bottom: 4px;
    }

    .hero-card-sub {
      font-size: 0.8rem;
      color: var(--text-muted);
      margin-bottom: 10px;
    }

    .hero-meta {
      font-size: 0.72rem;
      color: var(--text-muted);
      padding-top: 6px;
      border-top: 1px solid rgba(148, 163, 184, 0.3);
      display: flex;
      flex-direction: column;
      gap: 2px;
    }

    .panel {
      border-radius: var(--radius-xl);
      border: 1px solid var(--border-soft);
      background: var(--bg-panel);
      padding: 18px 18px 16px;
      box-shadow: var(--shadow-soft);
    }

    .two-col {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1.1fr);
      gap: 18px;
    }

    .three-col {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 14px;
    }

    .pill-title {
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--accent-2);
      margin-bottom: 4px;
    }

    ul {
      padding-right: 18px;
      margin: 6px 0 10px;
      color: var(--text-muted);
      font-size: 0.9rem;
    }

    li + li {
      margin-top: 2px;
    }

    .table-wrap {
      overflow-x: auto;
      margin-top: 10px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.85rem;
      border-radius: 12px;
      overflow: hidden;
      direction: rtl;
    }

    thead {
      background: radial-gradient(circle at 0 0, rgba(255, 204, 77, 0.3), rgba(15, 23, 42, 0.98));
    }

    th, td {
      padding: 8px 10px;
      text-align: right;
      border-bottom: 1px solid rgba(30, 64, 175, 0.45);
    }

    th {
      font-weight: 600;
      font-size: 0.8rem;
    }

    tbody tr:nth-child(even) {
      background: rgba(15, 23, 42, 0.85);
    }

    .checklist {
      list-style: none;
      padding-right: 0;
    }

    .checklist li::before {
      content: "✔ ";
      color: var(--accent);
      margin-left: 4px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 3px 9px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.6);
      font-size: 0.74rem;
      color: var(--text-muted);
      margin-left: 6px;
      margin-bottom: 6px;
    }

    .credit-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      align-items: center;
      font-size: 0.86rem;
      color: var(--text-muted);
    }

    .hashtag-row {
      font-size: 0.84rem;
      color: var(--accent-2);
      margin-top: 8px;
      word-break: break-word;
    }

    .verse {
      margin-top: 12px;
      padding-top: 10px;
      border-top: 1px dashed rgba(148, 163, 184, 0.55);
      font-size: 0.9rem;
      font-style: italic;
    }

    .footer-meta {
      margin-top: 10px;
      font-size: 0.8rem;
      color: var(--text-muted);
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: space-between;
    }

    @media (max-width: 900px) {
      .hero {
        grid-template-columns: minmax(0, 1fr);
      }
      .two-col {
        grid-template-columns: minmax(0, 1fr);
      }
      .three-col {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    @media (max-width: 600px) {
      main {
        padding: 16px 14px 40px;
      }
      .hero-left, .hero-right, .panel {
        padding: 16px 14px 14px;
      }
      h1 {
        font-size: 1.9rem;
      }
    }
  </style>
</head>
<body>
  <!-- ניווט עליון -->
  <header>
    <div class="nav-inner">
      <div class="logo-wrap">
        <div class="logo-circle" aria-hidden="true"></div>
        <div>
          <div class="logo-text-main">ToneCraft – EQ Realm</div>
          <div class="logo-text-sub">אומנות האקוולייזר • SparKing Audio</div>
        </div>
      </div>
      <nav>
        <a href="#overview">סקירה</a>
        <a href="#types">סוגי EQ</a>
        <a href="#map">מפת תדרים</a>
        <a href="#practice">פרקטיקה</a>
        <a href="#workflow">שיטת עבודה</a>
        <a href="#mistakes">טעויות</a>
        <a href="#glossary">מילון</a>
        <a href="#todo">צ’קליסט</a>
        <a href="#credits">קרדיטים</a>
      </nav>
    </div>
  </header>

  <main>
    <!-- Hero -->
    <section id="overview" class="hero">
      <div class="hero-left">
        <div class="hero-pill">
          <span>🎚️ אקוולייזר • ToneCraft</span>
          <span>⚡ SparKing Producers</span>
        </div>
        <h1>אומנות האקוולייזר – לפסל את הצליל</h1>
        <p class="hero-sub">
          ToneCraft – EQ Realm הוא האתר שלך להבנת אקוולייזר בעברית פשוטה:
          איך לנקות, לעצב ולהאיר כל צליל – מהקלטת ווקאל באולפן ביתי ועד מאסטרינג לשיר מלא.
        </p>
        <div class="hero-tags">
          <span class="tag">Beat Makers</span>
          <span class="tag">זמרים</span>
          <span class="tag">אולפן ביתי</span>
          <span class="tag">SparKing AudioMind</span>
        </div>
      </div>

      <aside class="hero-right" aria-label="מידע מהיר על EQ">
        <div class="hero-card-title">תמצית EQ</div>
        <div class="hero-card-main">קודם חותכים רעש – ואז מחזקים אור.</div>
        <p class="hero-card-sub">
          🎧 EQ הוא לא סתם פלאגין – זו דרך חשיבה. כל שינוי בתדר משנה רגש, עומק וחדות של המוזיקה.
        </p>
        <div class="two-col" style="gap:12px; margin-top:6px;">
          <div>
            <h3>🎛 עמוד זה נותן לך</h3>
            <ul>
              <li>הסבר ברור מה זה EQ.</li>
              <li>סוגי אקוולייזרים ויתרונותיהם.</li>
              <li>מפת תדרים לפי תחושה.</li>
              <li>מתכוני EQ לווקאל, תופים ובאס.</li>
            </ul>
          </div>
          <div>
            <h3>🧭 נתוני בסיס</h3>
            <ul>
              <li>פרויקט: ToneCraft (TC) בתוך SparKing.</li>
              <li>שפה: עברית מלאה, כיוון RTL.</li>
              <li>פורמט: index.html ל-GitHub Pages.</li>
            </ul>
          </div>
        </div>

        <div class="hero-meta">
          <span>📅 תאריך לועזי: 29.11.2025</span>
          <span>📅 תאריך עברי: ט׳ בכסלו תשפ״ו</span>
          <span>⏰ שעה ליצירת הדף: 22:17 (שעון ישראל)</span>
        </div>
      </aside>
    </section>

    <!-- סוגי EQ -->
    <section id="types">
      <div class="panel">
        <div class="pill-title">מדור 1</div>
        <h2>🎛 מה זה אקוולייזר?</h2>
        <p>
          אקוולייזר (EQ) הוא הפסל של הצליל שלך. הוא שולט בעוצמת התדרים – נמוכים, אמצעיים וגבוהים –
          כדי לנקות בוץ, להאיר נוכחות ולתת מקום לכל כלי במיקס.
        </p>

        <div class="two-col" style="margin-top:10px;">
          <div>
            <h3>🧱 סוגי EQ מרכזיים</h3>
            <ul>
              <li><strong>Parametric EQ</strong> – שליטה מלאה בתדר, Gain ו-Q, לעבודה מדויקת.</li>
              <li><strong>Graphic EQ</strong> – שורה של פיידרים בתדרים קבועים, מעולה ללייב וחדרים.</li>
              <li><strong>Shelving EQ</strong> – High/Low Shelf, להוספת חום או אוויר בקצה הספקטרום.</li>
              <li><strong>High/Low-Pass Filters</strong> – פילטרים לחיתוך קיצוני של נמוכים/גבוהים.</li>
            </ul>
          </div>
          <div>
            <h3>🎚 Parametric EQ – המלך של האולפן</h3>
            <p>
              Parametric EQ מאפשר לבחור תדר מדויק, לקבוע כמה להרים/להוריד, ולהחליט אם הטיפול צר
              (כירורגי) או רחב (מוזיקלי). זה הכלי העיקרי לעיצוב סאונד מקצועי.
            </p>
            <ul>
              <li>🧪 אידיאלי להסרת רעשים נקודתיים.</li>
              <li>🎨 מעולה לעיצוב צבע של ווקאל וכלים.</li>
              <li>🎚 חובה כמעט על כל ערוץ חשוב במיקס.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- מפת תדרים -->
    <section id="map">
      <div class="panel">
        <div class="pill-title">מדור 2</div>
        <h2>🌈 מפת תדרים – איך הצליל מרגיש</h2>
        <p>
          כל טווח תדר מביא איתו תחושה אחרת. הבנת המפה הופכת כל תזוזה ב-EQ לפעולה מודעת ולא לניחוש.
        </p>

        <div class="table-wrap">
          <table>
            <thead>
              <tr>
                <th>🎚 טווח (Hz)</th>
                <th>🧠 מה חי כאן</th>
                <th>💫 איך זה מרגיש</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>20–60 Hz</td>
                <td>סאב עמוק</td>
                <td>רטט בבטן, תחושת חלל קוסמי</td>
              </tr>
              <tr>
                <td>60–120 Hz</td>
                <td>באס ראשי</td>
                <td>משקל, כוח, גרוב</td>
              </tr>
              <tr>
                <td>120–250 Hz</td>
                <td>גוף הכלים</td>
                <td>חמימות, אך עלול להיות בוצי</td>
              </tr>
              <tr>
                <td>250–500 Hz</td>
                <td>Low Mids</td>
                <td>מלאות לעומת “קופסתיות”</td>
              </tr>
              <tr>
                <td>500–2 kHz</td>
                <td>נוכחות</td>
                <td>פוקוס, מובנות של דיבור ושירה</td>
              </tr>
              <tr>
                <td>2–5 kHz</td>
                <td>תקיפה וחדות</td>
                <td>Edge, אנרגיה, לפעמים חדות צורבת</td>
              </tr>
              <tr>
                <td>5–8 kHz</td>
                <td>ניצוץ ופרטים</td>
                <td>שימר, פריכות, “שי” בהיי־הטס</td>
              </tr>
              <tr>
                <td>8–16 kHz</td>
                <td>אוויר</td>
                <td>מרחב, ברק, תחושת “יקר”</td>
              </tr>
            </tbody>
          </table>
        </div>

        <p>
          🪄 טיפ: לפעמים עדיף לחתוך אזור שמעמיס במקום להרים עוד ועוד תדרים אחרים.
        </p>
      </div>
    </section>

    <!-- פרקטיקה -->
    <section id="practice">
      <div class="panel">
        <div class="pill-title">מדור 3</div>
        <h2>🎤 מתכוני EQ פרקטיים</h2>
        <p>
          אלו נקודות התחלה – לא חוקים קשיחים. תמיד להקשיב להקלטה, לז’אנר ולוייב של השיר.
        </p>

        <div class="three-col">
          <div>
            <h3>🎙 ווקאל</h3>
            <ul>
              <li>✂ High-Pass: סביב 80–120 Hz להסרת רעידות ורעש נמוך.</li>
              <li>🎯 נוכחות: +1–3 dB באזור 2–4 kHz לשיפור מובנות.</li>
              <li>✨ אוויר: High Shelf עדין ב־10–14 kHz לליטוש ופתיחת הראש.</li>
              <li>🧼 אם בוצי: Cut עדין ב־200–350 Hz.</li>
            </ul>
          </div>
          <div>
            <h3>🥁 תופים</h3>
            <ul>
              <li><strong>Kick</strong>: Punch ב־60–100 Hz, Attack ב־2–4 kHz.</li>
              <li><strong>Snare</strong>: גוף ב־150–250 Hz, Crack ב־3–5 kHz.</li>
              <li><strong>Hi-Hats</strong>: Sparkle ב־8–10 kHz.</li>
              <li>High-Pass על מיקרופונים שלא צריכים באס עמוק.</li>
            </ul>
          </div>
          <div>
            <h3>🎸 באס וסינתים</h3>
            <ul>
              <li>Sub: 40–80 Hz – בוחרים נקודת מרכז ומחזקים בעדינות.</li>
              <li>גוף: 100–200 Hz, תלוי בכלי ובמיקס.</li>
              <li>Definition: 800 Hz–1.5 kHz, כדי שיישמע גם ברמקולים קטנים.</li>
              <li>Pad/Synth: High-Pass סביב 150–300 Hz לפינוי מקום לבאס ולקיק.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- שיטת עבודה -->
    <section id="workflow">
      <div class="panel">
        <div class="pill-title">מדור 4</div>
        <h2>🧪 שיטת Sweep & Sculpt – לעבוד חכם עם EQ</h2>
        <p>שיטה פשוטה לניקוי רעשים וחיתוך בעיות בלי להרוס את המוזיקליות.</p>

        <ol style="padding-right:18px; color:var(--text-muted); font-size:0.92rem;">
          <li>בחר ערוץ אחד (למשל ווקאל) והקשב לרגע ב-Solo.</li>
          <li>פתח Band, הרם אותו בערך +6–8 dB והגדר Q צר.</li>
          <li>הזז את התדר לאט – איפה שזה הכי צורם/מחריד ➜ שם הבעיה.</li>
          <li>עכשיו במקום Boost, עשה Cut עדין של 2–4 dB באותו תדר.</li>
          <li>חזור על הפעולה לעוד נקודות בעייתיות, לאט ובסבלנות.</li>
          <li>כבה/הפעל את האקוולייזר כל כמה שניות – אם אין שיפור ברור, אל תוסיף טיפול סתם.</li>
          <li>סיום: האזן שוב לכל המיקס, לא רק ל-Solo. המטרה היא שיר מרגיש, לא גרף יפה.</li>
        </ol>
      </div>
    </section>

    <!-- טעויות -->
    <section id="mistakes">
      <div class="panel">
        <div class="pill-title">מדור 5</div>
        <h2>🚫 טעויות נפוצות באקוולייזר – ומה לעשות במקום</h2>

        <div class="two-col">
          <div>
            <h3>❌ להרים הכול</h3>
            <p>Boost על כל תדר שנשמע טוב עד שהמיקס הופך לעייף וצורם.</p>
            <ul>
              <li>✅ תעדיף כמה Cuts חכמים על פני המון Boost.</li>
              <li>✅ תן מקום לשקט – גם הוא חלק מהעוצמה.</li>
            </ul>

            <h3>❌ לתקן ביצוע גרוע עם EQ</h3>
            <p>לנסות “להציל” שירה לא יציבה רק עם אקוולייזר.</p>
            <ul>
              <li>✅ קודם כל: ביצוע והקלטה טובים.</li>
              <li>✅ אחר כך: EQ עדין כדי ללטש, לא כדי להסתיר.</li>
            </ul>
          </div>
          <div>
            <h3>❌ לעשות הכול על המאסטר</h3>
            <p>לשים EQ אגרסיבי רק על ה-Master Bus ולקוות שיסדר את כל הבעיות.</p>
            <ul>
              <li>✅ רוב העבודה: על ערוצים בודדים ו-Bus Groups.</li>
              <li>✅ מאסטר: שינויים קטנים, מדויקים, מודעים.</li>
            </ul>

            <h3>❌ לא להשתמש ב-Bypass</h3>
            <p>לעבוד דקות ארוכות בלי להשוות למצב הקודם.</p>
            <ul>
              <li>✅ כל כמה שניות – ON/OFF, לשאול: באמת יותר טוב?</li>
              <li>✅ אם ההבדל לא מורגש לטובה – אולי אין צורך ב-EQ.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- מילון -->
    <section id="glossary">
      <div class="panel">
        <div class="pill-title">מדור 6</div>
        <h2>📚 מילון מונחי EQ קטן</h2>

        <div class="two-col">
          <div>
            <h3>מושגי בסיס</h3>
            <ul>
              <li><strong>Frequency (Hz)</strong> – כמה מהר גל הקול רוטט; קובע את גובה הצליל.</li>
              <li><strong>Gain (dB)</strong> – כמה אנחנו מגבירים או מנמיכים אזור בתדר.</li>
              <li><strong>Q (Bandwidth)</strong> – רוחב הטיפול: צר = כירורגי, רחב = רך ומוזיקלי.</li>
              <li><strong>Cut</strong> – הורדה של תדר מסוים.</li>
              <li><strong>Boost</strong> – הגברה של תדר מסוים.</li>
            </ul>
          </div>
          <div>
            <h3>סוגי פילטרים</h3>
            <ul>
              <li><strong>High-Pass Filter</strong> – מעביר גבוהים, חותך נמוכים.</li>
              <li><strong>Low-Pass Filter</strong> – מעביר נמוכים, חותך גבוהים.</li>
              <li><strong>High/Low Shelf</strong> – מגביר/מנמיך אזור רחב בקצה העליון/התחתון.</li>
              <li><strong>Bell</strong> – “פעמון” קלאסי לעיצוב תדר נקודתי.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- צ'קליסט -->
    <section id="todo">
      <div class="panel">
        <div class="pill-title">מדור 7</div>
        <h2>✅ EQ To-Do – צ’קליסט אימון</h2>
        <p>תוכל להפוך את הרשימה הזאת לדף עבודה, לקלפים, או להרגל שבועי קבוע.</p>

        <ul class="checklist">
          <li>בחר שיר שאתה אוהב ונסה לזהות: איפה הבאס יושב? איפה הווקאל יושב בתדרים?</li>
          <li>קח הקלטת ווקאל גולמית ויישם: High-Pass, ניקוי בוץ, הוספת אוויר.</li>
          <li>עבוד על זוג Kick + Bass עד שהם משלימים אחד את השני ולא נלחמים.</li>
          <li>בחר פלאגין EQ אחד ולמד אותו לעומק במקום לקפוץ בין עשרות.</li>
          <li>פתח “EQ Journal” – רשום מתכונים שעבדו לך לכל סוג כלי.</li>
          <li>הכן A/B: מיקס בלי EQ מול מיקס עם EQ – בדיקה בעיניים סגורות.</li>
        </ul>
      </div>
    </section>

    <!-- קרדיטים -->
    <section id="credits">
      <div class="panel">
        <div class="pill-title">מדור 8</div>
        <h2>🌀 קרדיטים • פרויקט • ברכה</h2>

        <div class="credit-row">
          <span class="badge">יוצר: AnLoMinus – SparKing Leon Yaakobov</span>
          <span class="badge">שם הפרויקט: ToneCraft – TC (EQ Realm)</span>
          <span class="badge">יקום: SparKing AudioMind</span>
        </div>

        <p style="margin-top:8px;">
          🔗 ריפו מומלץ:
        </p>
        <ul>
          <li><strong>ריפו עיקרי:</strong> <code>github.com/AnLoMinus/ToneCraft-EQ</code></li>
          <li><strong>ריפו-אב:</strong> <code>github.com/AnLoMinus/SparKing</code></li>
        </ul>

        <div class="hashtag-row">
          #ToneCraft #EQ #Equalizer #SparKing #AnLoMinus #Mixing #SoundDesign #אקוולייזר #אולפן_ביתי
        </div>

        <div class="verse">
          📜 “כָּל הַנְּשָׁמָה תְּהַלֵּל יָהּ הַלְלוּיָהּ.” (תהילים ק״נ)  
          <br />
          כל נשימה, כל תדר, כל מיקס – הזדמנות להפוך את הצליל להלל של אור.
        </div>

        <div class="footer-meta">
          <span>📅 תאריך לועזי: 29.11.2025</span>
          <span>📅 תאריך עברי: ט׳ בכסלו תשפ״ו</span>
          <span>⏰ שעה נוכחית: 22:17 (שעון ישראל)</span>
          <span>💫 מספר המידות: 72</span>
        </div>
      </div>
    </section>
  </main>
</body>
</html>
```

---

🎤 **פזמון ראפ – ToneCraft עברית**

אקוולייזר בידי, אני מגלף את האור,
חותך את כל הבוץ, משאיר רק לב טהור,
ToneCraft במיקס, SparKing מדליק את הדור,
כל תדר במקום – זה פסל־צליל חי וקור.

---
