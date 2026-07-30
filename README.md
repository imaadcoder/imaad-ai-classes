<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Imaad AI Classes</title>
  <style>
    :root {
      --bg: #050816;
      --panel: #101728;
      --panel-2: #172132;
      --text: #f8fafc;
      --muted: #cbd5e1;
      --accent: #38bdf8;
      --accent-2: #2563eb;
      --border: #243447;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }

    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      color: var(--text);
      background:
        radial-gradient(circle at top left, rgba(56,189,248,0.22), transparent 28%),
        radial-gradient(circle at bottom right, rgba(37,99,235,0.20), transparent 32%),
        linear-gradient(135deg, #050816 0%, #07111f 45%, #111c35 100%);
    }

    a { text-decoration: none; color: inherit; }

    .container {
      width: min(1180px, 92%);
      margin: 0 auto;
    }

    header {
      position: sticky;
      top: 0;
      background: rgba(5, 8, 22, 0.95);
      border-bottom: 1px solid var(--border);
      z-index: 1000;
      backdrop-filter: blur(8px);
    }

    .nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 16px 0;
    }

    .logo {
      font-size: 1.35rem;
      font-weight: 800;
      color: var(--accent);
    }

    .logo span {
      display: block;
      font-size: 0.7rem;
      letter-spacing: .25em;
      color: #fff;
      margin-top: 3px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 16px;
      color: var(--muted);
    }

    .nav-links a:hover { color: #fff; }

    .btn {
      display: inline-block;
      border: none;
      cursor: pointer;
      transition: transform .2s ease;
    }

    .btn:hover { transform: translateY(-2px); }

    .btn-primary {
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      color: white;
      padding: 12px 16px;
      border-radius: 999px;
      font-weight: 700;
    }

    .hero {
      padding: 90px 0 70px;
      background:
        linear-gradient(120deg, rgba(3,8,20,0.86), rgba(15,23,42,0.72)),
        url("https://images.unsplash.com/photo-1677442136019-21780ecad995?auto=format&fit=crop&w=1600&q=80");
      background-size: cover;
      background-position: center;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 30px;
      align-items: center;
    }

    .hero h1 {
      font-size: clamp(2.15rem, 4vw, 3.3rem);
      margin-bottom: 12px;
      line-height: 1.2;
    }

    .hero .lead {
      color: var(--muted);
      font-size: 1.05rem;
      margin-bottom: 18px;
      max-width: 700px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 20px;
    }

    .stats {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      color: var(--muted);
    }

    .stat {
      background: rgba(255,255,255,0.08);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 10px 12px;
      min-width: 130px;
    }

    .stat strong {
      display: block;
      color: #fff;
      font-size: 1.02rem;
    }

    .hero-card, .panel {
      background: rgba(17,24,39,0.95);
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 24px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.32);
    }

    .hero-card h3, .panel h2 {
      color: var(--accent);
      margin-bottom: 10px;
    }

    .hero-card ul, .panel ul {
      padding-left: 18px;
      color: var(--muted);
    }

    section {
      padding: 70px 0;
    }

    .section-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      margin-bottom: 18px;
      flex-wrap: wrap;
    }

    .section-head h2 {
      font-size: 1.7rem;
    }

    .section-head .sub {
      color: var(--muted);
    }

    .enroll-card {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 20px;
      background: rgba(17,24,39,0.95);
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 24px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.32);
    }

    .contact-form {
      display: grid;
      gap: 12px;
    }

    .contact-form input,
    .contact-form select,
    .contact-form textarea {
      width: 100%;
      padding: 12px 14px;
      border-radius: 10px;
      border: 1px solid var(--border);
      background: #0b1223;
      color: #fff;
      outline: none;
    }

    .contact-form textarea {
      min-height: 110px;
      resize: vertical;
    }

    .contact-form .btn {
      padding: 12px 14px;
      border-radius: 10px;
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      color: white;
      font-weight: 700;
    }

    .status {
      min-height: 24px;
      color: var(--accent);
      margin-top: 4px;
    }

    .search-box {
      display: flex;
      gap: 10px;
      margin-bottom: 16px;
      flex-wrap: wrap;
    }

    .search-box input {
      flex: 1;
      min-width: 220px;
      padding: 12px 14px;
      border: 1px solid var(--border);
      border-radius: 10px;
      background: #111827;
      color: #fff;
      outline: none;
    }

    .filters {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 16px;
    }

    .filter-btn {
      padding: 9px 13px;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: #111827;
      color: #fff;
      cursor: pointer;
    }

    .filter-btn.active {
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      color: white;
      border-color: transparent;
    }

    .course-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .card {
      background: #111827;
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
      transition: transform .2s ease, border-color .2s ease;
    }

    .card:hover {
      transform: translateY(-4px);
      border-color: var(--accent);
    }

    .tag {
      display: inline-block;
      margin-bottom: 8px;
      padding: 6px 10px;
      border-radius: 999px;
      font-size: .8rem;
      background: rgba(56,189,248,0.12);
      color: var(--accent);
    }

    .card h3 {
      margin-bottom: 8px;
      font-size: 1.06rem;
    }

    .card p {
      color: var(--muted);
      margin-bottom: 10px;
      min-height: 46px;
    }

    .meta {
      color: #9fb3c8;
      font-size: .95rem;
      margin-bottom: 10px;
    }

    .price {
      font-size: 1.4rem;
      font-weight: 800;
      margin-bottom: 12px;
      color: #fff;
    }

    .card .btn {
      width: 100%;
      padding: 10px 12px;
      border-radius: 10px;
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      color: white;
      font-weight: 700;
    }

    .empty {
      grid-column: 1 / -1;
      padding: 24px;
      text-align: center;
      border: 1px dashed var(--border);
      border-radius: 16px;
      color: var(--muted);
      background: rgba(255,255,255,0.03);
    }

    .points-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
      margin-top: 16px;
    }

    .point-item {
      background: #111827;
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 12px 14px;
      color: #dbeafe;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 24px;
      align-items: start;
    }

    .contact-box {
      background: rgba(17,24,39,0.95);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 24px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    }

    .chat-button {
      position: fixed;
      right: 20px;
      bottom: 20px;
      width: 58px;
      height: 58px;
      border-radius: 50%;
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 28px;
      cursor: pointer;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
      z-index: 950;
    }

    .chat-box {
      display: none;
      position: fixed;
      right: 20px;
      bottom: 90px;
      width: 330px;
      background: #111827;
      border: 1px solid var(--border);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
      z-index: 949;
    }

    .chat-header {
      padding: 12px 14px;
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-weight: 700;
    }

    .chat-body {
      padding: 12px;
      height: 260px;
      overflow: auto;
      background: #0b1223;
      color: var(--muted);
    }

    .chat-body p { margin-bottom: 8px; }

    .chat-input {
      display: flex;
      border-top: 1px solid var(--border);
    }

    .chat-input input {
      flex: 1;
      border: none;
      outline: none;
      padding: 12px;
      background: #111827;
      color: #fff;
    }

    .chat-input button {
      border: none;
      padding: 12px 14px;
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      color: white;
      cursor: pointer;
      font-weight: 700;
    }

    .whatsapp {
      position: fixed;
      left: 20px;
      bottom: 20px;
      background: #25D366;
      color: white;
      padding: 12px 16px;
      border-radius: 999px;
      font-weight: 700;
      z-index: 950;
    }

    footer {
      padding: 28px 0 40px;
      text-align: center;
      color: #94a3b8;
      border-top: 1px solid var(--border);
      background: #020617;
    }

    @media (max-width: 980px) {
      .hero-grid,
      .enroll-card,
      .contact-grid { grid-template-columns: 1fr; }
      .course-grid { grid-template-columns: 1fr 1fr; }
    }

    @media (max-width: 700px) {
      .nav-links {
        display: none;
        position: absolute;
        top: 66px;
        right: 4%;
        left: 4%;
        flex-direction: column;
        align-items: flex-start;
        padding: 14px;
        border: 1px solid var(--border);
        border-radius: 12px;
        background: rgba(5,8,22,0.98);
      }

      .nav-links.show { display: flex; }

      .course-grid { grid-template-columns: 1fr; }
      .points-grid { grid-template-columns: 1fr; }
      .hero { padding-top: 60px; }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a href="#home" class="logo">🚀 IMAAD AI<span>CLASSES</span></a>
      <div class="nav-links" id="navLinks">
        <a href="#enroll">Enroll</a>
        <a href="#courses">Courses</a>
        <a href="#why">Why Us</a>
        <a href="#contact">Contact</a>
        <a href="#enroll" class="btn btn-primary">Enroll Now</a>
      </div>
    </div>
  </header>

  <section class="hero" id="home">
    <div class="container hero-grid">
      <div>
        <h1>Learn AI, Web, Data & Business Skills</h1>
        <p class="lead">
          Join practical training with expert guidance. Our course prices start from <strong>₹5999</strong> and go up to <strong>₹10999</strong>.
        </p>
        <div class="hero-actions">
          <a href="#courses" class="btn btn-primary">View Courses</a>
          <a href="#enroll" class="btn btn-primary">Enroll Now</a>
        </div>
        <div class="stats">
          <div class="stat"><strong>20+</strong> Courses</div>
          <div class="stat"><strong>100%</strong> Practical</div>
          <div class="stat"><strong>24/7</strong> Support</div>
        </div>
      </div>

      <div class="hero-card">
        <h3>Why Choose Imaad AI Classes?</h3>
        <ul>
          <li>Beginner to advanced learning paths</li>
          <li>Real projects and assignments</li>
          <li>Live support and guidance</li>
          <li>Flexible batch timing</li>
          <li>Certificate on completion</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="enroll">
    <div class="container">
      <div class="enroll-card">
        <div>
          <h2>Enroll Now</h2>
          <p>Fill this form and we will contact you shortly with the best course for your goal.</p>
        </div>

        <form class="contact-form" id="enrollForm">
          <input type="text" id="enrollName" placeholder="Your Name" required />
          <input type="email" id="enrollEmail" placeholder="Your Email" required />
          <input type="text" id="enrollPhone" placeholder="Your Phone" />
          <select id="enrollCourse">
            <option value="Select a course">Select a course</option>
            <option value="HTML & CSS Basics">HTML & CSS Basics</option>
            <option value="JavaScript Essentials">JavaScript Essentials</option>
            <option value="React Development">React Development</option>
            <option value="Python for AI">Python for AI</option>
            <option value="Machine Learning">Machine Learning</option>
            <option value="Advanced AI & ML">Advanced AI & ML</option>
            <option value="Data Science Bootcamp">Data Science Bootcamp</option>
            <option value="AI Marketing">AI Marketing</option>
          </select>
          <textarea id="enrollMessage" placeholder="Tell us about your goal..."></textarea>
          <button class="btn" type="submit">Send Enrollment Request</button>
          <div class="status" id="enrollStatus"></div>
        </form>
      </div>
    </div>
  </section>

  <section id="courses">
    <div class="container">
      <div class="section-head">
        <h2>Popular Courses</h2>
        <div class="sub">Search, filter, and enroll in the best course for you</div>
      </div>

      <div class="search-box">
        <input id="searchInput" type="text" placeholder="Search courses..." />
      </div>

      <div class="filters">
        <button class="filter-btn active" data-category="all">All</button>
        <button class="filter-btn" data-category="web">Web</button>
        <button class="filter-btn" data-category="ai">AI</button>
        <button class="filter-btn" data-category="data">Data</button>
        <button class="filter-btn" data-category="business">Business</button>
      </div>

      <div class="course-grid" id="courseGrid"></div>
    </div>
  </section>

  <section id="why">
    <div class="container">
      <div class="section-head">
        <h2>Why Choose Us?</h2>
        <div class="sub">20 reasons students trust Imaad AI Classes</div>
      </div>

      <div class="points-grid">
        <div class="point-item">1. Beginner-friendly learning environment</div>
        <div class="point-item">2. Simple and clear explanations</div>
        <div class="point-item">3. Practical projects in every course</div>
        <div class="point-item">4. Real-world examples and case studies</div>
        <div class="point-item">5. Flexible learning schedule</div>
        <div class="point-item">6. Support for doubts and questions</div>
        <div class="point-item">7. Career-focused training</div>
        <div class="point-item">8. Updated course content</div>
        <div class="point-item">9. Affordable pricing from ₹5999</div>
        <div class="point-item">10. Advanced tracks up to ₹10999</div>
        <div class="point-item">11. Hands-on assignments</div>
        <div class="point-item">12. Learn from basics to advanced level</div>
        <div class="point-item">13. Easy-to-follow lessons</div>
        <div class="point-item">14. Industry-friendly tools and methods</div>
        <div class="point-item">15. Certification on completion</div>
        <div class="point-item">16. Good for students and professionals</div>
        <div class="point-item">17. Personalized guidance</div>
        <div class="point-item">18. Build skills for future jobs</div>
        <div class="point-item">19. Fast and friendly support</div>
        <div class="point-item">20. Trusted by learners who want real results</div>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="container contact-grid">
      <div class="contact-box">
        <h2>Contact Us</h2>
        <p style="color: var(--muted); margin-top: 8px;">Want to know more? Fill the form and we will contact you soon.</p>
        <div style="margin-top: 16px; color: var(--muted);">
          <div>📧 Email: abida28125@gmail.com</div>
          <div>📱 WhatsApp: +91 9596191037</div>
          <div>📍 Online classes available</div>
        </div>
      </div>

      <div class="contact-box">
        <form class="contact-form" id="contactForm">
          <input type="text" id="contactName" placeholder="Your Name" required />
          <input type="email" id="contactEmail" placeholder="Your Email" required />
          <input type="text" id="contactPhone" placeholder="Your Phone" />
          <textarea id="contactMessage" placeholder="Write your query here..."></textarea>
          <button class="btn" type="submit">Send Message</button>
          <div class="status" id="contactStatus"></div>
        </form>
      </div>
    </div>
  </section>

  <div class="chat-button" id="chatToggle">🤖</div>

  <div class="chat-box" id="chatBox">
    <div class="chat-header">
      <span>Imaad AI Tutor</span>
      <span id="closeChat" style="cursor:pointer;">✖</span>
    </div>
    <div class="chat-body" id="chatBody">
      <p><b>AI Tutor:</b> Hello! Ask me about courses, pricing, or enrollment.</p>
    </div>
    <div class="chat-input">
      <input id="chatInput" type="text" placeholder="Ask something..." />
      <button id="sendChat">Send</button>
    </div>
  </div>

  <a class="whatsapp" href="https://wa.me/9596191037">WhatsApp Us</a>

  <footer>© 2026 Imaad AI Classes. All rights reserved.</footer>

  <script>
    const courses = [
      { title: "HTML & CSS Basics", category: "web", price: 5999, duration: "2 Weeks", desc: "Build clean and responsive websites from scratch.", badge: "Beginner" },
      { title: "JavaScript Essentials", category: "web", price: 6999, duration: "3 Weeks", desc: "Learn DOM, logic, and interactive web pages.", badge: "Popular" },
      { title: "React Development", category: "web", price: 7999, duration: "4 Weeks", desc: "Create modern UI applications with React.", badge: "Advanced" },
      { title: "Full Stack Web Course", category: "web", price: 8999, duration: "6 Weeks", desc: "Frontend + backend + deployment in one program.", badge: "Pro" },
      { title: "Python for AI", category: "ai", price: 9499, duration: "5 Weeks", desc: "Get started with Python for machine learning and AI.", badge: "Beginner" },
      { title: "Machine Learning", category: "ai", price: 9999, duration: "6 Weeks", desc: "Learn models, training, and evaluation.", badge: "Popular" },
      { title: "Advanced AI & ML", category: "ai", price: 10999, duration: "8 Weeks", desc: "Build advanced AI models and deployment workflows.", badge: "Expert" },
      { title: "Generative AI", category: "ai", price: 10499, duration: "6 Weeks", desc: "Create content, prompts, and automations using AI tools.", badge: "Trending" },
      { title: "Data Science Bootcamp", category: "data", price: 9999, duration: "6 Weeks", desc: "Work with Python, analytics, and dashboards.", badge: "Popular" },
      { title: "Power BI & Analytics", category: "data", price: 8999, duration: "5 Weeks", desc: "Turn raw data into business insights.", badge: "Practical" },
      { title: "Cloud & DevOps Basics", category: "data", price: 10999, duration: "5 Weeks", desc: "Learn deployment, CI/CD, and cloud basics.", badge: "Advanced" },
      { title: "AI Marketing", category: "business", price: 7499, duration: "4 Weeks", desc: "Use AI tools for campaigns and digital growth.", badge: "Business" },
      { title: "AI Business Tools", category: "business", price: 7999, duration: "4 Weeks", desc: "Automate office work with smart AI business workflows.", badge: "Business" },
      { title: "Prompt Engineering", category: "business", price: 6499, duration: "3 Weeks", desc: "Master prompts for better results from AI tools.", badge: "Practical" },
      { title: "AI Content Creation", category: "business", price: 6999, duration: "3 Weeks", desc: "Create media content using AI tools quickly.", badge: "Creative" }
    ];

    const state = { category: "all", search: "" };
    const courseGrid = document.getElementById("courseGrid");
    const searchInput = document.getElementById("searchInput");
    const enrollStatus = document.getElementById("enrollStatus");
    const contactStatus = document.getElementById("contactStatus");

    function renderCourses() {
      const filtered = courses.filter(course => {
        const matchCategory = state.category === "all" || course.category === state.category;
        const text = `${course.title} ${course.desc} ${course.duration}`.toLowerCase();
        const matchSearch = text.includes(state.search.toLowerCase());
        return matchCategory && matchSearch;
      });

      if (!filtered.length) {
        courseGrid.innerHTML = `<div class="empty">No course found. Try another keyword or filter.</div>`;
        return;
      }

      courseGrid.innerHTML = filtered.map(course => `
        <div class="card">
          <span class="tag">${course.badge}</span>
          <h3>${course.title}</h3>
          <p>${course.desc}</p>
          <div class="meta">Duration: ${course.duration}</div>
          <div class="price">₹${course.price}</div>
          <button class="btn enroll-btn">Enroll Now</button>
        </div>
      `).join("");
    }

    document.querySelectorAll(".filter-btn").forEach(btn => {
      btn.addEventListener("click", () => {
        document.querySelectorAll(".filter-btn").forEach(b => b.classList.remove("active"));
        btn.classList.add("active");
        state.category = btn.dataset.category;
        renderCourses();
      });
    });

    searchInput.addEventListener("input", (e) => {
      state.search = e.target.value.trim();
      renderCourses();
    });

    courseGrid.addEventListener("click", (e) => {
      if (e.target.classList.contains("enroll-btn")) {
        const card = e.target.closest(".card");
        const title = card.querySelector("h3").textContent;
        const price = card.querySelector(".price").textContent;
        enrollStatus.textContent = `You selected ${title} for ${price}.`;
      }
    });

    document.getElementById("enrollForm").addEventListener("submit", (e) => {
      e.preventDefault();
      const name = document.getElementById("enrollName").value.trim();
      const email = document.getElementById("enrollEmail").value.trim();
      if (!name || !email) {
        enrollStatus.textContent = "Please enter your name and email.";
        return;
      }

      const course = document.getElementById("enrollCourse").value;
      const message = document.getElementById("enrollMessage").value.trim();
      const body = encodeURIComponent(
        `Name: ${name}\nEmail: ${email}\nPhone: ${document.getElementById("enrollPhone").value.trim()}\nCourse: ${course}\nMessage: ${message}`
      );
      window.location.href = `mailto:abida28125@gmail.com?subject=${encodeURIComponent("Enrollment Request - Imaad AI Classes")}&body=${body}`;
      enrollStatus.textContent = "Opening your email app...";
      e.target.reset();
    });

    document.getElementById("contactForm").addEventListener("submit", (e) => {
      e.preventDefault();
      const name = document.getElementById("contactName").value.trim();
      const email = document.getElementById("contactEmail").value.trim();
      if (!name || !email) {
        contactStatus.textContent = "Please enter your name and email.";
        return;
      }

      const message = document.getElementById("contactMessage").value.trim();
      const body = encodeURIComponent(
        `Name: ${name}\nEmail: ${email}\nPhone: ${document.getElementById("contactPhone").value.trim()}\nMessage: ${message}`
      );
      window.location.href = `mailto:abida28125@gmail.com?subject=${encodeURIComponent("Contact Request - Imaad AI Classes")}&body=${body}`;
      contactStatus.textContent = "Opening your email app...";
      e.target.reset();
    });

    document.getElementById("navLinks").classList.remove("show"); // no-op just keeps script clean

    const chatToggle = document.getElementById("chatToggle");
    const chatBox = document.getElementById("chatBox");
    const closeChat = document.getElementById("closeChat");
    const sendChat = document.getElementById("sendChat");
    const chatInput = document.getElementById("chatInput");
    const chatBody = document.getElementById("chatBody");

    function addMessage(sender, text) {
      const p = document.createElement("p");
      p.innerHTML = `<b>${sender}:</b> ${text}`;
      chatBody.appendChild(p);
      chatBody.scrollTop = chatBody.scrollHeight;
    }

    function replyToChat(message) {
      const msg = message.toLowerCase();

      if (msg.includes("hello") || msg.includes("hi")) {
        return "Hello! I’m Imaad AI Tutor. I can help with courses, pricing, and enrollment.";
      }
      if (msg.includes("price") || msg.includes("cost")) {
        return "Our courses start from ₹5999 and go up to ₹10999 depending on the course.";
      }
      if (msg.includes("course")) {
        return "We offer web, AI, data, and business courses. You can choose from HTML, JavaScript, React, Python for AI, Machine Learning, Data Science, and more.";
      }
      if (msg.includes("enroll") || msg.includes("join")) {
        return "You can enroll by using the Enroll Now form on this page.";
      }
      if (msg.includes("contact") || msg.includes("email")) {
        return "You can contact us at abida28125@gmail.com or WhatsApp +91 9596191037.";
      }
      if (msg.includes("whatsapp")) {
        return "You can contact us on WhatsApp: +91 9596191037.";
      }
      if (msg.includes("ai")) {
        return "We teach AI, Machine Learning, Generative AI, Prompt Engineering, and more.";
      }
      return "Thanks for your message! I can help with courses, pricing, enrollment, or contact details.";
    }

    chatToggle.addEventListener("click", () => {
      chatBox.style.display = chatBox.style.display === "block" ? "none" : "block";
    });

    closeChat.addEventListener("click", () => {
      chatBox.style.display = "none";
    });

    function sendMessage() {
      const msg = chatInput.value.trim();
      if (!msg) return;

      addMessage("You", msg);
      addMessage("Imaad AI", replyToChat(msg));
      chatInput.value = "";
    }

    sendChat.addEventListener("click", sendMessage);

    chatInput.addEventListener("keydown", (e) => {
      if (e.key === "Enter") {
        sendMessage();
      }
    });

    renderCourses();
  </script>
</body>
</html>
