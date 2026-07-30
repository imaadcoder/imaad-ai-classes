<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Aetheria AI Academy</title>
  <meta name="description" content="Aetheria AI Academy offers premium AI, web, data, creative, and business courses with magical guidance and expert support." />
  <meta name="theme-color" content="#070b1f" />
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 128 128'%3E%3Cdefs%3E%3ClinearGradient id='g' x1='0' y1='0' x2='1' y2='1'%3E%3Cstop offset='0%25' stop-color='%2338bdf8'/%3E%3Cstop offset='100%25' stop-color='%238b5cf6'/%3E%3C/linearGradient%3E%3C/defs%3E%3Crect width='128' height='128' rx='32' fill='%23070b1f'/%3E%3Cpath d='M64 20l16 36 38 4-29 24 9 38-34-20-34 20 9-38-29-24 38-4z' fill='url(%23g)'/%3E%3C/svg%3E" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet" />
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
  <style>
    :root{
      --bg:#060816;
      --bg-2:#0b1328;
      --panel:rgba(11,19,40,0.88);
      --panel-2:rgba(18,28,56,0.95);
      --text:#f7f9ff;
      --muted:#c7d0e6;
      --accent:#38bdf8;
      --accent-2:#8b5cf6;
      --accent-3:#22d3ee;
      --border:rgba(255,255,255,0.12);
      --shadow:0 20px 60px rgba(0,0,0,0.35);
      --radius:24px;
      --radius-sm:16px;
      --transition:0.28s ease;
    }

    *{box-sizing:border-box;margin:0;padding:0}
    html{scroll-behavior:smooth}
    body{
      font-family:'Inter',sans-serif;
      color:var(--text);
      background:
        radial-gradient(circle at top left, rgba(56,189,248,0.18), transparent 32%),
        radial-gradient(circle at 90% 10%, rgba(139,92,246,0.22), transparent 26%),
        radial-gradient(circle at bottom center, rgba(34,211,238,0.16), transparent 30%),
        linear-gradient(135deg, var(--bg) 0%, var(--bg-2) 45%, #111b35 100%);
      min-height:100vh;
      overflow-x:hidden;
      line-height:1.6;
    }

    a{color:inherit;text-decoration:none}
    img{display:block;max-width:100%}
    button,input,textarea,select{font:inherit}
    button{cursor:pointer;border:none}
    .skip-link{
      position:absolute;left:-999px;top:auto;
      background:#fff;color:#000;padding:8px 12px;border-radius:8px;z-index:9999;
    }
    .skip-link:focus{left:12px;top:12px}

    .aurora{
      position:fixed;inset:0;pointer-events:none;z-index:-1;
      background:
        radial-gradient(circle at 15% 20%, rgba(56,189,248,0.12), transparent 24%),
        radial-gradient(circle at 85% 15%, rgba(139,92,246,0.16), transparent 24%),
        radial-gradient(circle at 50% 100%, rgba(34,211,238,0.14), transparent 28%);
      filter:blur(30px);
      animation: drift 18s ease-in-out infinite alternate;
    }
    @keyframes drift{0%{transform:translate3d(0,0,0)}100%{transform:translate3d(20px,-18px,0)}}

    .container{width:min(1210px,92%);margin:0 auto}
    .section{padding:76px 0}
    .section-title{
      display:flex;justify-content:space-between;align-items:end;gap:12px;flex-wrap:wrap;
      margin-bottom:22px;
    }
    .section-title h2{
      font-family:'Playfair Display',serif;font-size:1.6rem;font-weight:700;letter-spacing:0.2px
    }
    .section-title p{color:var(--muted);max-width:600px}

    .glass{
      background:var(--panel);
      border:1px solid var(--border);
      box-shadow:var(--shadow);
      backdrop-filter:blur(18px);
      -webkit-backdrop-filter:blur(18px);
    }

    .loader{
      position:fixed;inset:0;display:grid;place-items:center;background:rgba(6,8,22,0.96);z-index:9999;transition:opacity .5s ease,visibility .5s ease;
    }
    .loader.hidden{opacity:0;visibility:hidden}
    .loader-box{
      width:min(420px,90%);padding:26px;border-radius:28px;border:1px solid var(--border);background:rgba(11,19,40,0.9);text-align:center;box-shadow:var(--shadow)
    }
    .loader-mark{
      width:72px;height:72px;border-radius:22px;margin:0 auto 14px;
      display:grid;place-items:center;
      background:linear-gradient(135deg,var(--accent),var(--accent-2));
      box-shadow:0 12px 28px rgba(56,189,248,0.28);
      animation:pulse 1.3s ease-in-out infinite;
    }
    .loader-mark svg{width:40px;height:40px;fill:#fff}
    .loader h3{font-size:1.1rem;margin-bottom:6px}
    .loader p{color:var(--muted);font-size:0.95rem}

    @keyframes pulse{0%,100%{transform:scale(1)}50%{transform:scale(1.06)}}

    header{
      position:sticky;top:0;z-index:1000;
      background:rgba(6,8,22,0.78);
      backdrop-filter:blur(16px);
      -webkit-backdrop-filter:blur(16px);
      border-bottom:1px solid var(--border);
    }
    .nav{
      display:flex;justify-content:space-between;align-items:center;padding:14px 0;
    }
    .brand{
      display:flex;align-items:center;gap:12px;min-width:0;
    }
    .brand-mark{
      width:46px;height:46px;border-radius:16px;
      display:grid;place-items:center;
      background:linear-gradient(135deg,var(--accent),var(--accent-2));
      box-shadow:0 10px 24px rgba(56,189,248,0.24);
      flex-shrink:0;
    }
    .brand-mark svg{width:26px;height:26px;fill:#fff}
    .brand-text{
      line-height:1.05;white-space:nowrap;
    }
    .brand-title{
      font-family:'Playfair Display',serif;font-size:1.02rem;font-weight:700;letter-spacing:0.04em;
    }
    .brand-sub{
      font-size:0.72rem;letter-spacing:0.26em;text-transform:uppercase;color:#cbd5e1;opacity:0.9;
    }

    .nav-links{
      display:flex;align-items:center;gap:14px;color:var(--muted);
    }
    .nav-links a{transition:color var(--transition),transform var(--transition)}
    .nav-links a:hover{color:#fff;transform:translateY(-1px)}
    .menu-btn{
      display:none;background:rgba(255,255,255,0.06);border:1px solid var(--border);color:#fff;padding:10px 12px;border-radius:12px;
    }

    .btn{
      display:inline-flex;align-items:center;justify-content:center;gap:8px;
      padding:12px 16px;border-radius:999px;font-weight:700;border:1px solid transparent;transition:transform var(--transition),box-shadow var(--transition),background var(--transition),border-color var(--transition);
    }
    .btn:hover{transform:translateY(-2px)}
    .btn-primary{
      background:linear-gradient(90deg,var(--accent),var(--accent-2));
      color:#fff;box-shadow:0 14px 28px rgba(56,189,248,0.24);
    }
    .btn-secondary{
      background:rgba(255,255,255,0.06);border-color:var(--border);color:var(--text);
    }

    .hero{
      padding:90px 0 40px;
      position:relative;
      overflow:hidden;
    }
    .hero-grid{
      display:grid;grid-template-columns:1.08fr .92fr;gap:24px;align-items:center;
    }
    .eyebrow{
      display:inline-flex;align-items:center;gap:8px;padding:8px 12px;border-radius:999px;
      background:rgba(255,255,255,0.06);border:1px solid var(--border);color:#e6f5ff;margin-bottom:16px;font-size:0.82rem;text-transform:uppercase;letter-spacing:0.22em;
    }
    .hero h1{
      font-family:'Playfair Display',serif;font-size:clamp(2.1rem,4vw,3.6rem);line-height:1.08;margin-bottom:12px;
      letter-spacing:-0.02em;
    }
    .hero h1 .magic{
      background:linear-gradient(90deg,var(--accent),#ffffff 35%, var(--accent-2));
      -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;color:transparent;
      display:inline-block;
    }
    .hero .lead{
      color:var(--muted);font-size:1.04rem;max-width:700px;margin-bottom:18px;
    }
    .hero-actions{display:flex;flex-wrap:wrap;gap:12px;margin-bottom:22px}
    .hero-stats{
      display:flex;flex-wrap:wrap;gap:12px;
    }
    .hero-stat{
      min-width:122px;padding:12px 14px;border-radius:16px;border:1px solid var(--border);background:rgba(255,255,255,0.06);
    }
    .hero-stat strong{display:block;color:#fff;font-size:1.06rem}
    .hero-stat span{color:var(--muted);font-size:0.9rem}

    .hero-card{
      padding:28px;border-radius:28px;position:relative;overflow:hidden;
      border:1px solid var(--border);background:linear-gradient(145deg,rgba(18,28,56,0.95),rgba(11,18,36,0.95));
      box-shadow:var(--shadow);
    }
    .hero-card::before{
      content:"";position:absolute;inset:0;padding:1px;border-radius:inherit;
      background:linear-gradient(120deg,rgba(56,189,248,0.26),transparent 30%,rgba(139,92,246,0.24));
      -webkit-mask:linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);-webkit-mask-composite:xor;mask-composite:exclude;pointer-events:none;
    }
    .hero-card h3{
      font-size:1.2rem;margin-bottom:12px;color:#fff;
    }
    .hero-card ul{padding-left:18px;color:var(--muted);display:grid;gap:8px}
    .hero-orb{
      position:absolute;right:-10px;bottom:-28px;width:180px;height:180px;border-radius:50%;
      background:radial-gradient(circle at 30% 30%, rgba(255,255,255,0.35), rgba(56,189,248,0.16) 30%, transparent 60%);
      filter:blur(4px);pointer-events:none;opacity:0.7;
    }

    .grid-2{display:grid;grid-template-columns:1fr 1fr;gap:20px}
    .card{
      border-radius:var(--radius);padding:20px;
      border:1px solid var(--border);background:var(--panel);box-shadow:var(--shadow);transition:transform var(--transition),border-color var(--transition),box-shadow var(--transition);
    }
    .card:hover{transform:translateY(-4px);border-color:rgba(56,189,248,0.35);box-shadow:0 24px 56px rgba(0,0,0,0.35)}
    .tag{
      display:inline-flex;padding:7px 10px;border-radius:999px;font-size:0.74rem;letter-spacing:0.08em;
      background:rgba(56,189,248,0.12);border:1px solid rgba(56,189,248,0.2);color:#8edcff;text-transform:uppercase;margin-bottom:10px;
    }
    .card h3{font-size:1.06rem;margin-bottom:8px;color:#fff}
    .card p{color:var(--muted);margin-bottom:10px;min-height:56px}
    .meta{font-size:0.92rem;color:#9db0c8;margin-bottom:10px}
    .price{font-size:1.34rem;font-weight:800;margin-bottom:12px;color:#fff}
    .card .btn{width:100%}
    .empty{
      grid-column:1 / -1;padding:24px;border:1px dashed var(--border);text-align:center;border-radius:18px;color:var(--muted);background:rgba(255,255,255,0.03);
    }

    .course-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
    .search-row{
      display:flex;gap:10px;flex-wrap:wrap;margin-bottom:16px;
    }
    .search-row input{
      flex:1;min-width:240px;padding:12px 14px;border-radius:14px;background:rgba(7,12,24,0.95);border:1px solid var(--border);color:#fff;outline:none;
    }
    .filters{display:flex;flex-wrap:wrap;gap:10px;margin-bottom:18px}
    .filter-btn{
      padding:9px 13px;border-radius:999px;border:1px solid var(--border);background:rgba(255,255,255,0.05);color:var(--text);transition:all var(--transition);
    }
    .filter-btn.active{
      background:linear-gradient(90deg,var(--accent),var(--accent-2));border-color:transparent;color:#fff;box-shadow:0 10px 24px rgba(56,189,248,0.2);
    }

    .enroll-grid{
      display:grid;grid-template-columns:0.9fr 1.1fr;gap:20px;align-items:start;
    }
    .panel{
      border-radius:var(--radius);padding:24px;border:1px solid var(--border);background:var(--panel);box-shadow:var(--shadow);
    }
    .panel h3{font-size:1.2rem;margin-bottom:8px;color:#fff}
    .panel p{color:var(--muted)}
    .feature-list{margin-top:12px;display:grid;gap:8px}
    .feature-item{padding:10px 12px;border-radius:12px;background:rgba(255,255,255,0.05);border:1px solid var(--border);color:var(--muted)}
    .form-grid{display:grid;gap:12px}
    .form-group{display:grid;gap:6px}
    .form-label{font-size:0.9rem;color:#dce7f8}
    input,select,textarea{
      width:100%;padding:12px 14px;border-radius:14px;background:rgba(7,12,24,0.95);border:1px solid var(--border);color:#fff;outline:none;transition:border-color var(--transition),box-shadow var(--transition);
    }
    input:focus,select:focus,textarea:focus{
      border-color:var(--accent);box-shadow:0 0 0 3px rgba(56,189,248,0.16);
    }
    textarea{min-height:110px;resize:vertical}
    .status{min-height:24px;font-size:0.92rem;color:#8edcff;margin-top:4px}

    .points-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:16px}
    .point-item{padding:12px 14px;border-radius:14px;border:1px solid var(--border);background:rgba(255,255,255,0.05);color:var(--muted)}

    .contact-grid{display:grid;grid-template-columns:0.9fr 1.1fr;gap:20px;align-items:start}
    .contact-card .info{margin-top:16px;display:grid;gap:10px;color:var(--muted)}

    .chat-button{
      position:fixed;right:20px;bottom:20px;width:60px;height:60px;border-radius:50%;
      background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#fff;display:grid;place-items:center;font-size:24px;box-shadow:var(--shadow);z-index:1100;
    }
    .chat-panel{
      position:fixed;right:20px;bottom:90px;width:min(360px,calc(100vw - 24px));border-radius:24px;overflow:hidden;border:1px solid var(--border);background:rgba(6,10,24,0.94);box-shadow:var(--shadow);z-index:1090;display:none;
    }
    .chat-header{
      padding:12px 14px;background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#fff;display:flex;justify-content:space-between;align-items:center;font-weight:700;
    }
    .chat-body{
      padding:12px;height:320px;overflow:auto;display:flex;flex-direction:column;gap:10px;background:linear-gradient(180deg,rgba(7,12,24,0.97),rgba(7,12,24,0.9));scroll-behavior:smooth;
    }
    .message{display:flex;gap:8px;align-items:flex-end;max-width:100%}
    .message.user{justify-content:flex-end}
    .message.user .bubble{
      background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#fff;border-radius:16px 16px 6px 16px;
    }
    .message.bot .bubble{
      background:rgba(255,255,255,0.08);border:1px solid var(--border);color:var(--text);border-radius:16px 16px 16px 6px;
    }
    .bubble{
      padding:10px 12px;max-width:85%;font-size:0.95rem;line-height:1.5;box-shadow:0 8px 20px rgba(0,0,0,0.2);white-space:pre-wrap;
    }
    .avatar{
      width:34px;height:34px;border-radius:50%;display:grid;place-items:center;background:rgba(255,255,255,0.08);border:1px solid var(--border);flex-shrink:0;font-size:0.95rem;
    }
    .timestamp{
      font-size:0.72rem;color:#95a7bf;margin-top:4px;padding:0 2px;
    }
    .typing{
      display:inline-flex;align-items:center;gap:5px;padding:10px 12px;border-radius:14px;border:1px solid var(--border);background:rgba(255,255,255,0.08);width:fit-content;
    }
    .typing span{
      width:7px;height:7px;border-radius:50%;background:var(--accent);display:inline-block;animation:bounce 0.8s infinite ease-in-out;
    }
    .typing span:nth-child(2){animation-delay:0.15s}
    .typing span:nth-child(3){animation-delay:0.3s}
    @keyframes bounce{0%,80%,100%{transform:translateY(0);opacity:.7}40%{transform:translateY(-4px);opacity:1}}

    .quick-replies{display:flex;flex-wrap:wrap;gap:8px;padding:10px 12px;border-top:1px solid var(--border);background:rgba(255,255,255,0.03)}
    .quick-btn{
      border:1px solid var(--border);padding:8px 10px;border-radius:999px;background:rgba(255,255,255,0.06);color:var(--text);font-size:0.9rem;
    }
    .chat-input{display:flex;align-items:flex-end;gap:8px;padding:10px;border-top:1px solid var(--border);background:rgba(255,255,255,0.03)}
    .chat-input textarea{
      flex:1;min-height:46px;max-height:110px;resize:none;padding:10px 12px;border-radius:12px;background:rgba(7,12,24,0.95);border:1px solid var(--border);color:#fff;
    }
    .send-btn{
      padding:10px 12px;border-radius:12px;background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#fff;font-weight:700;
    }

    .whatsapp{
      position:fixed;left:20px;bottom:20px;padding:12px 16px;border-radius:999px;background:#25D366;color:#fff;font-weight:700;box-shadow:var(--shadow);z-index:1100;
    }

    footer{
      padding:30px 0 42px;border-top:1px solid var(--border);text-align:center;color:#9fb0c8;background:rgba(3,5,14,0.8);
    }
    .reveal{opacity:0;transform:translateY(16px);transition:opacity .7s ease,transform .7s ease}
    .reveal.is-visible{opacity:1;transform:translateY(0)}

    @media (max-width: 980px){
      .hero-grid,.enroll-grid,.contact-grid{grid-template-columns:1fr}
      .course-grid{grid-template-columns:1fr 1fr}
      .grid-2{grid-template-columns:1fr}
    }

    @media (max-width: 760px){
      .menu-btn{display:inline-flex;align-items:center;justify-content:center}
      .nav-links{
        display:none;position:absolute;top:60px;right:4%;left:4%;flex-direction:column;align-items:flex-start;
        background:rgba(6,8,22,0.97);border:1px solid var(--border);border-radius:16px;padding:14px;box-shadow:var(--shadow);
      }
      .nav-links.show{display:flex}
      .hero{padding-top:66px}
      .course-grid{grid-template-columns:1fr}
      .points-grid{grid-template-columns:1fr}
      .hero-stats{gap:10px}
      .hero-stat{min-width:100%}
      .chat-button,.whatsapp{bottom:14px}
      .chat-panel{bottom:74px}
    }
  </style>
</head>
<body>
  <div id="loader" class="loader" aria-live="polite">
    <div class="loader-box">
      <div class="loader-mark" aria-hidden="true">
        <svg viewBox="0 0 128 128"><path d="M64 20l16 36 38 4-29 24 9 38-34-20-34 20 9-38-29-24 38-4z"/></svg>
      </div>
      <h3>Welcome to Aetheria AI Academy</h3>
      <p>Preparing your magical learning journey...</p>
    </div>
  </div>

  <a class="skip-link" href="#main">Skip to content</a>

  <div class="aurora"></div>

  <header>
    <div class="container nav">
      <a class="brand" href="#home" aria-label="Aetheria AI Academy home">
        <span class="brand-mark" aria-hidden="true">
          <svg viewBox="0 0 128 128"><path d="M64 20l16 36 38 4-29 24 9 38-34-20-34 20 9-38-29-24 38-4z"/></svg>
        </span>
        <span class="brand-text">
          <span class="brand-title">AETHERIA</span>
          <span class="brand-sub">AI ACADEMY</span>
        </span>
      </a>

      <button class="menu-btn" id="menuBtn" aria-label="Open menu">☰</button>

      <nav class="nav-links" id="navLinks" aria-label="Primary navigation">
        <a href="#enroll">Enroll</a>
        <a href="#courses">Courses</a>
        <a href="#why">Why Us</a>
        <a href="#contact">Contact</a>
        <a href="#enroll" class="btn btn-primary">Enroll Now</a>
      </nav>
    </div>
  </header>

  <main id="main">
    <section class="hero" id="home">
      <div class="container hero-grid">
        <div class="reveal">
          <div class="eyebrow">✨ Premium learning, powered by magic</div>
          <h1>Master <span class="magic">AI</span>, Web, Data, and Creative Skills</h1>
          <p class="lead">
            Aetheria AI Academy blends practical training, expert guidance, and a premium learning experience into one unforgettable path for students and professionals.
          </p>
          <div class="hero-actions">
            <a href="#courses" class="btn btn-primary">Explore Courses</a>
            <a href="#enroll" class="btn btn-secondary">Start Enrollment</a>
          </div>
          <div class="hero-stats">
            <div class="hero-stat"><strong>30+</strong><span>Courses</span></div>
            <div class="hero-stat"><strong>100%</strong><span>Practical</span></div>
            <div class="hero-stat"><strong>24/7</strong><span>Support</span></div>
          </div>
        </div>

        <div class="hero-card reveal">
          <h3>Why learners love Aetheria</h3>
          <ul>
            <li>Beginner to advanced pathways</li>
            <li>Hands-on projects and guided practice</li>
            <li>High-impact, modern curriculum</li>
            <li>Flexible learning and mentor support</li>
            <li>Career-ready outcomes and certificates</li>
          </ul>
          <div class="hero-orb" aria-hidden="true"></div>
        </div>
      </div>
    </section>

    <section class="section" id="enroll">
      <div class="container">
        <div class="enroll-grid">
          <div class="panel reveal">
            <h3>Enroll in your next chapter</h3>
            <p>Tell us your goals and we’ll guide you to the perfect course, pace, and learning path.</p>
            <div class="feature-list">
              <div class="feature-item">🌟 Personalized course guidance</div>
              <div class="feature-item">🧠 Expert-led training</div>
              <div class="feature-item">📈 Career-focused learning outcomes</div>
              <div class="feature-item">⚡ Fast replies and support</div>
            </div>
          </div>

          <div class="panel reveal">
            <form class="form-grid" id="enrollForm">
              <div class="form-group">
                <label class="form-label" for="enrollName">Name</label>
                <input id="enrollName" name="name" type="text" placeholder="Your name" required />
              </div>
              <div class="form-group">
                <label class="form-label" for="enrollEmail">Email</label>
                <input id="enrollEmail" name="email" type="email" placeholder="you@example.com" required />
              </div>
              <div class="form-group">
                <label class="form-label" for="enrollPhone">Phone</label>
                <input id="enrollPhone" name="phone" type="text" placeholder="Phone number" />
              </div>
              <div class="form-group">
                <label class="form-label" for="enrollCourse">Course</label>
                <select id="enrollCourse" name="course">
                  <option value="Select a course">Select a course</option>
                  <option value="HTML & CSS Basics">HTML & CSS Basics</option>
                  <option value="JavaScript Essentials">JavaScript Essentials</option>
                  <option value="React Development">React Development</option>
                  <option value="Python for AI">Python for AI</option>
                  <option value="Machine Learning">Machine Learning</option>
                  <option value="Advanced AI & ML">Advanced AI & ML</option>
                  <option value="Data Science Bootcamp">Data Science Bootcamp</option>
                  <option value="AI Marketing">AI Marketing</option>
                  <option value="Prompt Engineering">Prompt Engineering</option>
                  <option value="Generative AI">Generative AI</option>
                </select>
              </div>
              <div class="form-group">
                <label class="form-label" for="enrollMessage">Goal</label>
                <textarea id="enrollMessage" name="message" placeholder="Tell us about your target and preferred pace..."></textarea>
              </div>
              <button class="btn btn-primary" type="submit">Send Enrollment Request</button>
              <div class="status" id="enrollStatus" aria-live="polite"></div>
            </form>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="courses">
      <div class="container">
        <div class="section-title reveal">
          <div>
            <h2>Featured Courses</h2>
            <p>Search, filter, and discover a path that fits your goals and pace.</p>
          </div>
        </div>

        <div class="search-row reveal">
          <input id="searchInput" type="text" placeholder="Search courses..." />
        </div>

        <div class="filters reveal">
          <button class="filter-btn active" data-category="all">All</button>
          <button class="filter-btn" data-category="web">Web</button>
          <button class="filter-btn" data-category="ai">AI</button>
          <button class="filter-btn" data-category="data">Data</button>
          <button class="filter-btn" data-category="business">Business</button>
          <button class="filter-btn" data-category="creative">Creative</button>
        </div>

        <div class="course-grid" id="courseGrid"></div>
      </div>
    </section>

    <section class="section" id="why">
      <div class="container">
        <div class="section-title reveal">
          <div>
            <h2>Why Choose Aetheria</h2>
            <p>We combine elegance, structure, and real-world outcomes so your learning feels both inspiring and practical.</p>
          </div>
        </div>

        <div class="points-grid reveal">
          <div class="point-item">1. Beginner-friendly teaching and clear guidance</div>
          <div class="point-item">2. Practical projects in every learning path</div>
          <div class="point-item">3. Expert support for doubts and growth</div>
          <div class="point-item">4. Flexible pacing for students and professionals</div>
          <div class="point-item">5. Modern tools, workflows, and industry relevance</div>
          <div class="point-item">6. Certificates and a premium learning experience</div>
          <div class="point-item">7. Structured courses from foundation to advanced</div>
          <div class="point-item">8. Friendly, human support at every step</div>
        </div>
      </div>
    </section>

    <section class="section" id="contact">
      <div class="container contact-grid">
        <div class="panel contact-card reveal">
          <h3>Let’s talk</h3>
          <p>Have questions, want a custom track, or need guidance? We’re happy to help.</p>
          <div class="info">
            <div>📧 Email: abida28125@gmail.com</div>
            <div>📱 WhatsApp: +91 9596191037</div>
            <div>🌐 Online classes available worldwide</div>
          </div>
        </div>

        <div class="panel reveal">
          <form class="form-grid" id="contactForm">
            <div class="form-group">
              <label class="form-label" for="contactName">Name</label>
              <input id="contactName" name="name" type="text" placeholder="Your name" required />
            </div>
            <div class="form-group">
              <label class="form-label" for="contactEmail">Email</label>
              <input id="contactEmail" name="email" type="email" placeholder="you@example.com" required />
            </div>
            <div class="form-group">
              <label class="form-label" for="contactPhone">Phone</label>
              <input id="contactPhone" name="phone" type="text" placeholder="Phone number" />
            </div>
            <div class="form-group">
              <label class="form-label" for="contactMessage">Message</label>
              <textarea id="contactMessage" name="message" placeholder="Write your query here..."></textarea>
            </div>
            <button class="btn btn-primary" type="submit">Send Message</button>
            <div class="status" id="contactStatus" aria-live="polite"></div>
          </form>
        </div>
      </div>
    </section>
  </main>

  <div class="chat-button" id="chatToggle" aria-label="Open assistant">🤖</div>

  <div class="chat-panel" id="chatPanel">
    <div class="chat-header">
      <span>✨ Aetheria Assistant</span>
      <span id="closeChat" style="cursor:pointer;">✖</span>
    </div>

    <div class="chat-body" id="chatBody"></div>

    <div class="quick-replies">
      <button class="quick-btn" data-text="Show me the courses">Courses</button>
      <button class="quick-btn" data-text="What is the price?">Prices</button>
      <button class="quick-btn" data-text="Enroll now">Enroll</button>
      <button class="quick-btn" data-text="I want Python">Python</button>
    </div>

    <div class="chat-input">
      <textarea id="chatInput" placeholder="Ask anything about courses and learning..."></textarea>
      <button class="send-btn" id="sendChat">➤</button>
    </div>
  </div>

  <a class="whatsapp" href="https://wa.me/9596191037" target="_blank" rel="noreferrer">WhatsApp Us</a>

  <footer>
    © 2026 Aetheria AI Academy. Crafted for modern learners.
  </footer>

  <script>
    const courses = [
      { title: "HTML & CSS Basics", category: "web", price: 5999, duration: "2 Weeks", desc: "Build modern, responsive web pages from scratch.", badge: "Beginner" },
      { title: "JavaScript Essentials", category: "web", price: 6999, duration: "3 Weeks", desc: "Master DOM, logic, events, and interactive web experiences.", badge: "Popular" },
      { title: "React Development", category: "web", price: 7999, duration: "4 Weeks", desc: "Create polished frontend interfaces with React.", badge: "Advanced" },
      { title: "Full Stack Web Course", category: "web", price: 8999, duration: "6 Weeks", desc: "Learn frontend, backend, and deployment in one path.", badge: "Pro" },
      { title: "UI/UX Design Foundations", category: "web", price: 7499, duration: "4 Weeks", desc: "Design clean experiences with wireframes, flows, and systems.", badge: "Design" },
      { title: "Python for AI", category: "ai", price: 9499, duration: "5 Weeks", desc: "Start your AI journey with practical Python basics.", badge: "Beginner" },
      { title: "Machine Learning", category: "ai", price: 9999, duration: "6 Weeks", desc: "Learn models, evaluation, feature engineering, and insight.", badge: "Popular" },
      { title: "Advanced AI & ML", category: "ai", price: 10999, duration: "8 Weeks", desc: "Build advanced pipelines, optimization, and deployment workflows.", badge: "Expert" },
      { title: "Generative AI", category: "ai", price: 10499, duration: "6 Weeks", desc: "Create content, prompts, and automation with modern AI tools.", badge: "Trending" },
      { title: "Prompt Engineering", category: "ai", price: 6499, duration: "3 Weeks", desc: "Master prompts for better results across AI tools.", badge: "Practical" },
      { title: "Data Science Bootcamp", category: "data", price: 9999, duration: "6 Weeks", desc: "Work with Python, analysis, dashboards, and storytelling.", badge: "Popular" },
      { title: "Power BI & Analytics", category: "data", price: 8999, duration: "5 Weeks", desc: "Turn raw data into useful insights and dashboards.", badge: "Practical" },
      { title: "SQL & Database Essentials", category: "data", price: 6999, duration: "3 Weeks", desc: "Learn querying, schema design, and data operations.", badge: "Core" },
      { title: "Cloud & DevOps Basics", category: "data", price: 10999, duration: "5 Weeks", desc: "Explore deployment, CI/CD, and basic cloud workflows.", badge: "Advanced" },
      { title: "AI Marketing", category: "business", price: 7499, duration: "4 Weeks", desc: "Use AI to grow campaigns, content, and customer engagement.", badge: "Business" },
      { title: "AI Business Tools", category: "business", price: 7999, duration: "4 Weeks", desc: "Automate operations and productivity with smart AI workflows.", badge: "Business" },
      { title: "Digital Growth Strategy", category: "business", price: 8299, duration: "4 Weeks", desc: "Plan modern digital growth using AI insights and analytics.", badge: "Growth" },
      { title: "AI Content Creation", category: "creative", price: 6999, duration: "3 Weeks", desc: "Create social media, blogs, and visuals using AI tools.", badge: "Creative" },
      { title: "Video Editing with AI", category: "creative", price: 7999, duration: "4 Weeks", desc: "Generate and edit short-form content with AI-powered workflows.", badge: "Creative" },
      { title: "No-Code Automation", category: "creative", price: 6899, duration: "3 Weeks", desc: "Build useful automations without traditional programming.", badge: "Automation" },
      { title: "Cybersecurity Basics", category: "data", price: 8499, duration: "4 Weeks", desc: "Learn digital safety, privacy, and practical protection methods.", badge: "Security" },
      { title: "AI Product Basics", category: "business", price: 8799, duration: "4 Weeks", desc: "Design smart digital products using AI-driven thinking.", badge: "Product" },
      { title: "Automation for Teams", category: "business", price: 7599, duration: "3 Weeks", desc: "Use AI and automation to streamline everyday team work.", badge: "Ops" },
      { title: "Ethical AI & Responsible Design", category: "ai", price: 7299, duration: "3 Weeks", desc: "Understand fairness, safety, and good practices in AI work.", badge: "Ethics" },
      { title: "Excel for Data Work", category: "data", price: 6499, duration: "3 Weeks", desc: "Get comfortable using Excel for analysis and reporting.", badge: "Practical" },
      { title: "Git & GitHub Essentials", category: "web", price: 6299, duration: "2 Weeks", desc: "Learn version control and modern collaborative workflows.", badge: "Workflow" },
      { title: "AI for Students", category: "ai", price: 5999, duration: "2 Weeks", desc: "Learn practical AI tools that improve study, writing, and productivity.", badge: "Student" },
      { title: "Chatbot Design", category: "creative", price: 7699, duration: "4 Weeks", desc: "Create conversation experiences for support, education, and business.", badge: "Bot" },
      { title: "Web3 & AI Basics", category: "web", price: 8499, duration: "4 Weeks", desc: "Explore the intersection of modern web trends and AI workflows.", badge: "Emerging" }
    ];

    const state = { category: "all", search: "", selectedCourse: null };
    const courseGrid = document.getElementById("courseGrid");
    const searchInput = document.getElementById("searchInput");
    const enrollStatus = document.getElementById("enrollStatus");
    const contactStatus = document.getElementById("contactStatus");
    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");
    const chatToggle = document.getElementById("chatToggle");
    const chatPanel = document.getElementById("chatPanel");
    const closeChat = document.getElementById("closeChat");
    const chatBody = document.getElementById("chatBody");
    const chatInput = document.getElementById("chatInput");
    const sendChat = document.getElementById("sendChat");
    const loader = document.getElementById("loader");

    function escapeHtml(str) {
      return String(str)
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#39;");
    }

    function renderCourses() {
      const filtered = courses.filter(course => {
        const matchCategory = state.category === "all" || course.category === state.category;
        const text = `${course.title} ${course.desc} ${course.duration}`.toLowerCase();
        const matchSearch = text.includes(state.search.toLowerCase());
        return matchCategory && matchSearch;
      });

      if (!filtered.length) {
        courseGrid.innerHTML = `<div class="empty">No course found. Try another filter or keyword.</div>`;
        return;
      }

      courseGrid.innerHTML = filtered.map(course => `
        <article class="card reveal">
          <span class="tag">${escapeHtml(course.badge)}</span>
          <h3>${escapeHtml(course.title)}</h3>
          <p>${escapeHtml(course.desc)}</p>
          <div class="meta">Duration: ${escapeHtml(course.duration)}</div>
          <div class="price">₹${course.price}</div>
          <button class="btn btn-primary enroll-btn" type="button" data-course="${escapeHtml(course.title)}">Enroll Now</button>
        </article>
      `).join("");
      observeReveals();
    }

    document.querySelectorAll(".filter-btn").forEach(btn => {
      btn.addEventListener("click", () => {
        document.querySelectorAll(".filter-btn").forEach(b => b.classList.remove("active"));
        btn.classList.add("active");
        state.category = btn.dataset.category;
        renderCourses();
      });
    });

    searchInput.addEventListener("input", e => {
      state.search = e.target.value.trim();
      renderCourses();
    });

    courseGrid.addEventListener("click", e => {
      const button = e.target.closest(".enroll-btn");
      if (!button) return;
      const title = button.dataset.course;
      openEnrollmentForm(title);
    });

    function openEnrollmentForm(courseTitle) {
      const section = document.getElementById("enroll");
      section.scrollIntoView({ behavior: "smooth", block: "start" });
      const select = document.getElementById("enrollCourse");
      if (courseTitle && Array.from(select.options).some(option => option.value === courseTitle)) {
        select.value = courseTitle;
      }
      document.getElementById("enrollName").focus();
      state.selectedCourse = courseTitle || null;
    }

    const FORM_PROVIDER = window.FORM_PROVIDER || "local";
    const EMAILJS_CONFIG = {
      publicKey: window.EMAILJS_PUBLIC_KEY || "",
      serviceId: window.EMAILJS_SERVICE_ID || "",
      templateId: window.EMAILJS_TEMPLATE_ID || ""
    };

    function fallbackSubmission(kind, payload) {
      const entry = { kind, ...payload, createdAt: new Date().toISOString() };
      try {
        const list = JSON.parse(localStorage.getItem("aetheriaFormSubmissions") || "[]");
        list.push(entry);
        localStorage.setItem("aetheriaFormSubmissions", JSON.stringify(list));
      } catch (error) {
        console.warn("Local storage unavailable", error);
      }
      return { ok: true, mode: "local-storage", entry };
    }

    async function submitFormData(kind, payload) {
      const hasEmailjsConfig =
        EMAILJS_CONFIG.publicKey &&
        !EMAILJS_CONFIG.publicKey.includes("YOUR") &&
        EMAILJS_CONFIG.serviceId &&
        !EMAILJS_CONFIG.serviceId.includes("YOUR") &&
        EMAILJS_CONFIG.templateId &&
        !EMAILJS_CONFIG.templateId.includes("YOUR");

      if (FORM_PROVIDER === "emailjs" && hasEmailjsConfig && window.emailjs) {
        try {
          if (typeof window.emailjs.init === "function") {
            window.emailjs.init(EMAILJS_CONFIG.publicKey);
          }
          const templateParams = {
            subject: kind === "enrollment" ? "Enrollment Request - Aetheria AI Academy" : "Contact Request - Aetheria AI Academy",
            name: payload.name,
            email: payload.email,
            phone: payload.phone || "N/A",
            course: payload.course || "N/A",
            message: payload.message || "N/A",
            type: kind
          };
          const result = await window.emailjs.send(EMAILJS_CONFIG.serviceId, EMAILJS_CONFIG.templateId, templateParams);
          if (result && result.status === 200) return result;
        } catch (error) {
          console.warn("EmailJS failed, using fallback", error);
        }
      }

      return fallbackSubmission(kind, payload);
    }

    async function handleFormSubmit(event, kind, statusElement) {
      event.preventDefault();
      const form = event.currentTarget;
      const formData = new FormData(form);
      const payload = Object.fromEntries(formData.entries());
      const name = payload.name?.toString().trim() || "";
      const email = payload.email?.toString().trim() || "";

      if (!name || !email) {
        statusElement.textContent = "Please enter your name and email.";
        return;
      }

      statusElement.textContent = "Sending your request...";
      try {
        await submitFormData(kind, payload);
        statusElement.textContent = "Thanks! Your request is received. We’ll be in touch soon.";
        form.reset();
      } catch (error) {
        console.error(error);
        statusElement.textContent = "Submission failed. Please contact us directly.";
      }
    }

    document.getElementById("enrollForm").addEventListener("submit", e => handleFormSubmit(e, "enrollment", enrollStatus));
    document.getElementById("contactForm").addEventListener("submit", e => handleFormSubmit(e, "contact", contactStatus));

    menuBtn.addEventListener("click", () => {
      navLinks.classList.toggle("show");
    });

    document.querySelectorAll(".nav-links a").forEach(link => {
      link.addEventListener("click", () => navLinks.classList.remove("show"));
    });

    function addTimestamp() {
      return new Date().toLocaleTimeString([], { hour: "numeric", minute: "2-digit" });
    }

    function addMessage(text, sender = "bot") {
      const wrapper = document.createElement("div");
      wrapper.className = `message ${sender}`;

      const avatar = document.createElement("div");
      avatar.className = "avatar";
      avatar.textContent = sender === "user" ? "🧑" : "✦";

      const bubbleWrap = document.createElement("div");
      bubbleWrap.style.maxWidth = "100%";

      const bubble = document.createElement("div");
      bubble.className = "bubble";
      bubble.innerHTML = text;

      const stamp = document.createElement("div");
      stamp.className = "timestamp";
      stamp.textContent = addTimestamp();

      bubbleWrap.appendChild(bubble);
      bubbleWrap.appendChild(stamp);

      if (sender === "bot") {
        wrapper.appendChild(avatar);
      }

      wrapper.appendChild(bubbleWrap);

      if (sender === "user") {
        wrapper.appendChild(avatar);
      }

      chatBody.appendChild(wrapper);
      chatBody.scrollTop = chatBody.scrollHeight;
    }

    function addTypingIndicator() {
      const wrap = document.createElement("div");
      wrap.className = "message bot";
      wrap.innerHTML = `
        <div class="avatar">✦</div>
        <div class="typing">
          <span></span><span></span><span></span>
        </div>
      `;
      chatBody.appendChild(wrap);
      chatBody.scrollTop = chatBody.scrollHeight;
      return wrap;
    }

    function removeTypingIndicator(el) {
      if (el && el.parentNode) el.parentNode.removeChild(el);
    }

    function normalizeText(text) {
      return text.toLowerCase().replace(/[^a-z0-9\s]/g, " ").replace(/\s+/g, " ").trim();
    }

    function correctText(text) {
      const raw = normalizeText(text);
      const replacements = {
        enrool: "enroll",
        enrol: "enroll",
        enroll: "enroll",
        pythin: "python",
        javscript: "javascript",
        js: "javascript",
        corse: "course",
        jion: "join",
        learnng: "learning",
        machien: "machine"
      };

      const words = raw.split(" ").map(word => replacements[word] || word);
      let corrected = words.join(" ").replace(/\s+/g, " ");
      corrected = corrected.charAt(0).toUpperCase() + corrected.slice(1);
      if (!/[?.!]$/.test(corrected)) corrected += ".";
      return corrected;
    }

    function detectIntent(text) {
      const corrected = correctText(text).toLowerCase();
      if (/\b(enroll|enrol|join|register|admission)\b/.test(corrected)) return "enroll";
      if (/\b(price|cost|fee|how much)\b/.test(corrected)) return "price";
      if (/\b(course|python|react|javascript|html|css|machine learning|data science|generative|prompt|marketing|content|cloud|devops)\b/.test(corrected)) return "course";
      return "general";
    }

    function findCourseByQuery(text) {
      const q = normalizeText(text);
      if (q.includes("python")) return courses.find(c => c.title.toLowerCase().includes("python")) || null;
      if (q.includes("react")) return courses.find(c => c.title.toLowerCase().includes("react")) || null;
      if (q.includes("javascript")) return courses.find(c => c.title.toLowerCase().includes("javascript")) || null;
      if (q.includes("html") || q.includes("css")) return courses.find(c => c.title.toLowerCase().includes("html")) || null;
      if (q.includes("machine learning")) return courses.find(c => c.title.toLowerCase().includes("machine learning")) || null;
      if (q.includes("data science")) return courses.find(c => c.title.toLowerCase().includes("data science")) || null;
      if (q.includes("generative")) return courses.find(c => c.title.toLowerCase().includes("generative")) || null;
      if (q.includes("prompt")) return courses.find(c => c.title.toLowerCase().includes("prompt")) || null;
      if (q.includes("marketing")) return courses.find(c => c.title.toLowerCase().includes("marketing")) || null;
      if (q.includes("cloud")) return courses.find(c => c.title.toLowerCase().includes("cloud")) || null;
      return null;
    }

    function getAIReply(rawText) {
      const corrected = correctText(rawText);
      const intent = detectIntent(rawText);
      const foundCourse = findCourseByQuery(rawText);

      if (foundCourse) {
        state.selectedCourse = foundCourse;
      }

      if (intent === "enroll") {
        openEnrollmentForm(state.selectedCourse ? state.selectedCourse.title : "");
        return "Absolutely — I’ve opened the enrollment section for you. Fill in your details and we’ll guide you to the best course.";
      }

      if (intent === "price") {
        if (state.selectedCourse) {
          return `${state.selectedCourse.title} costs ₹${state.selectedCourse.price}. It is a strong choice for practical learning.`;
        }
        return "Our courses start from ₹5999 and go up to ₹10999 depending on the course and level.";
      }

      if (intent === "course" && foundCourse) {
        return `${foundCourse.title} is an excellent choice. It is designed to help you build practical skills quickly. Would you like to enroll or see the price?`;
      }

      if (/hello|hi/.test(corrected.toLowerCase())) {
        return "Hello! I’m Aetheria Assistant. I can help with courses, pricing, enrollment, and study guidance.";
      }

      if (/courses|show/.test(corrected.toLowerCase())) {
        document.getElementById("courses").scrollIntoView({ behavior: "smooth", block: "start" });
        return "Absolutely — I’ve brought the course list into view for you.";
      }

      if (/contact|email/.test(corrected.toLowerCase())) {
        return "You can reach us at abida28125@gmail.com or WhatsApp us at +91 9596191037.";
      }

      if (/thanks|thank you/.test(corrected.toLowerCase())) {
        return "You’re welcome. I’m happy to help.";
      }

      return "I can help with course recommendations, pricing, enrollment, and learning guidance. Tell me what you want to learn.";
    }

    async function sendChatMessage() {
      const raw = chatInput.value.trim();
      if (!raw) return;

      addMessage(escapeHtml(raw).replace(/\\n/g, "<br>"), "user");
      chatInput.value = "";
      const typing = addTypingIndicator();

      await new Promise(resolve => setTimeout(resolve, 900));
      removeTypingIndicator(typing);

      const corrected = correctText(raw);
      let response = await getAIReply(raw);

      if (corrected.toLowerCase() !== raw.toLowerCase()) {
        response = `I understood your request as: "${corrected}"<br><br>${response}`;
      }

      addMessage(response, "bot");
    }

    chatToggle.addEventListener("click", () => {
      chatPanel.style.display = chatPanel.style.display === "block" ? "none" : "block";
      if (chatPanel.style.display === "block") chatInput.focus();
    });

    closeChat.addEventListener("click", () => {
      chatPanel.style.display = "none";
    });

    sendChat.addEventListener("click", sendChatMessage);

    chatInput.addEventListener("keydown", e => {
      if (e.key === "Enter" && !e.shiftKey) {
        e.preventDefault();
        sendChatMessage();
      }
    });

    document.querySelectorAll(".quick-btn").forEach(btn => {
      btn.addEventListener("click", () => {
        chatInput.value = btn.dataset.text;
        sendChatMessage();
      });
    });

    function observeReveals() {
      document.querySelectorAll(".reveal").forEach(el => {
        el.classList.remove("is-visible");
        const observer = new IntersectionObserver(entries => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              entry.target.classList.add("is-visible");
              observer.disconnect();
            }
          });
        }, { threshold: 0.12 });
        observer.observe(el);
      });
    }

    window.addEventListener("load", () => {
      renderCourses();
      observeReveals();
      setTimeout(() => {
        loader.classList.add("hidden");
      }, 850);
      addMessage("Hello! I’m Aetheria Assistant. I can help with courses, pricing, enrollment, and study guidance.", "bot");
    });
  </script>
</body>
</html>
