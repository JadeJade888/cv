<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Jade Marquez | Full Stack & Mobile Computer Engineer</title>
  <!-- Google Fonts: Tipografía sans-serif geométrica y limpia que replica fielmente el diseño del CV -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700;1,9..40,400&family=Plus+Jakarta+Sans:wght@500;600;700;800&display=swap"
    rel="stylesheet" />

  <style>
    /* ==========================================================================
       1. VARIABLES DE DISEÑO Y PALETA DE COLORES FUERTES
       ========================================================================== */
    :root {
      --bg-page: #f0e4df;
      --bg-sheet: #ffffff;
      --sidebar-bg: #6b081b;
      --sidebar-overlay: rgba(84, 6, 21, 0.74);
      --purple-primary: #8c0b23;
      --purple-deep: #4d0311;
      --purple-soft: #d9a83b;
      --text-primary: #1a0d10;
      --text-secondary: #332024;
      --text-muted: #69494f;
      --border-light: #dfb88c;
      --shadow-sheet: 0 22px 55px rgba(84, 6, 21, 0.22);
    }

    /* ==========================================================================
       2. RESET Y ESTILOS BASE
       ========================================================================== */
    *,
    *::before,
    *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      font-size: 16px;
    }

    body {
      background-color: var(--bg-page);
      color: var(--text-primary);
      font-family: 'DM Sans', sans-serif;
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
      padding: 2rem 1rem 4rem;
    }

    a {
      color: inherit;
      text-decoration: none;
      transition: color 0.2s ease, opacity 0.2s ease;
    }

    a:hover {
      color: var(--purple-primary);
    }

    /* ==========================================================================
       3. BARRA DE NAVEGACIÓN FLOTANTE Y BOTÓN DE IMPRESIÓN
       ========================================================================== */
    .top-toolbar {
      max-width: 960px;
      margin: 0 auto 1.25rem;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 0.75rem;
      padding: 0.65rem 1.25rem;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(10px);
      border: 1px solid var(--border-light);
      border-radius: 999px;
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1.1rem;
      font-size: 0.875rem;
      font-weight: 600;
      color: var(--text-secondary);
    }

    .nav-links a:hover {
      color: var(--purple-primary);
    }

    .btn-print {
      display: inline-flex;
      align-items: center;
      gap: 0.45rem;
      background-color: var(--purple-primary);
      color: #ffffff;
      border: none;
      border-radius: 999px;
      padding: 0.5rem 1.1rem;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.85rem;
      font-weight: 600;
      cursor: pointer;
      transition: background-color 0.2s ease, transform 0.15s ease;
    }

    .btn-print:hover {
      background-color: var(--purple-deep);
      transform: translateY(-1px);
    }

    .toolbar-controls {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      flex-wrap: wrap;
    }

    .btn-control {
      display: inline-flex;
      align-items: center;
      gap: 0.35rem;
      background-color: var(--bg-sheet);
      color: var(--purple-deep);
      border: 1px solid var(--border-light);
      border-radius: 999px;
      padding: 0.45rem 0.9rem;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.82rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .btn-control:hover {
      border-color: var(--purple-primary);
      background-color: var(--purple-soft);
    }

    /* ==========================================================================
       4. CONTENEDOR PRINCIPAL TIPO DOCUMENTO
       ========================================================================== */
    .cv-sheet {
      max-width: 960px;
      margin: 0 auto;
      background-color: var(--bg-sheet);
      border-radius: 18px;
      box-shadow: var(--shadow-sheet);
      display: grid;
      grid-template-columns: 185px 1fr;
      overflow: hidden;
      position: relative;
      border: 1px solid var(--border-light);
    }

    /* ==========================================================================
       5. FRANJA LATERAL CON SUPERPOSICIÓN DE COLOR INTENSO
       ========================================================================== */
    .botanical-sidebar {
      background-color: var(--sidebar-bg);
      background-image: linear-gradient(180deg, var(--sidebar-overlay) 0%, rgba(20, 10, 30, 0.82) 100%);
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      position: relative;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      padding: 2rem 0.75rem;
      border-right: 3px solid var(--purple-soft);
      transition: all 0.35s ease;
    }

    [data-theme="crimson-gold"] .botanical-sidebar {
      background-image: linear-gradient(180deg, var(--sidebar-overlay) 0%, rgba(45, 3, 12, 0.85) 100%);
      border-right: 3px solid #d9a83b;
    }

    .sidebar-badge {
      writing-mode: vertical-rl;
      transform: rotate(180deg);
      font-family: 'Plus Jakarta Sans', sans-serif;
      font-size: 0.78rem;
      font-weight: 700;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: #ffffff;
      opacity: 0.92;
      margin: 1.5rem 0;
    }

    [data-theme="crimson-gold"] .sidebar-badge {
      color: #f7d683;
    }

    .sidebar-accent-line {
      width: 3px;
      height: 65px;
      border-radius: 999px;
      background-color: #ffffff;
      opacity: 0.75;
    }

    [data-theme="crimson-gold"] .sidebar-accent-line {
      background-color: #d9a83b;
    }

    /* ==========================================================================
       6. CONTENIDO PRINCIPAL DEL CURRÍCULUM
       ========================================================================== */
    .cv-content {
      padding: 3rem 3.25rem 3.5rem;
    }

    .cv-header {
      margin-bottom: 1.75rem;
    }

    .cv-name {
      font-family: 'Plus Jakarta Sans', sans-serif;
      font-size: 2.35rem;
      font-weight: 800;
      line-height: 1.15;
      color: var(--text-primary);
      letter-spacing: -0.02em;
      margin-bottom: 0.25rem;
    }

    .cv-role {
      font-family: 'Plus Jakarta Sans', sans-serif;
      font-size: 1.25rem;
      font-weight: 700;
      color: var(--text-primary);
      margin-bottom: 0.45rem;
    }

    .cv-contact-info {
      font-size: 0.94rem;
      color: var(--text-secondary);
      line-height: 1.5;
    }

    .cv-contact-line {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 0.4rem 0.85rem;
    }

    .cv-contact-line a {
      border-bottom: 1px solid transparent;
    }

    .cv-contact-line a:hover {
      border-bottom-color: var(--purple-primary);
    }

    .cv-section {
      margin-top: 1.85rem;
    }

    .section-title {
      font-family: 'Plus Jakarta Sans', sans-serif;
      font-size: 1.22rem;
      font-weight: 700;
      color: var(--text-primary);
      margin-bottom: 0.85rem;
      padding-bottom: 0.35rem;
      border-bottom: 2px solid var(--purple-soft);
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .section-title::after {
      content: "";
      display: inline-block;
      width: 28px;
      height: 4px;
      border-radius: 4px;
      background-color: var(--purple-primary);
    }

    .profile-text {
      font-size: 0.96rem;
      color: var(--text-secondary);
      text-align: left;
      line-height: 1.65;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 0.9rem 2.25rem;
      list-style: none;
    }

    .skill-item {
      position: relative;
      padding-left: 1.15rem;
      font-size: 0.94rem;
      color: var(--text-secondary);
      line-height: 1.55;
    }

    .skill-item::before {
      content: "•";
      position: absolute;
      left: 0;
      top: 0;
      color: var(--text-primary);
      font-weight: 700;
      font-size: 1.1rem;
      line-height: 1.4;
    }

    .skill-item strong {
      color: var(--text-primary);
      font-weight: 700;
    }

    .experience-item {
      margin-bottom: 1.65rem;
    }

    .experience-item:last-child {
      margin-bottom: 0;
    }

    .exp-header {
      margin-bottom: 0.45rem;
    }

    .exp-title {
      font-family: 'Plus Jakarta Sans', sans-serif;
      font-size: 1.03rem;
      font-weight: 700;
      color: var(--text-primary);
      line-height: 1.35;
    }

    .exp-date {
      display: block;
      font-size: 0.9rem;
      font-weight: 500;
      color: var(--text-muted);
      margin-top: 0.1rem;
    }

    .exp-subtitle {
      display: block;
      font-size: 0.93rem;
      font-weight: 600;
      color: var(--purple-deep);
      margin-top: 0.1rem;
    }

    .cv-bullets {
      list-style: none;
      margin-top: 0.45rem;
    }

    .cv-bullets li {
      position: relative;
      padding-left: 1.2rem;
      font-size: 0.94rem;
      color: var(--text-secondary);
      margin-bottom: 0.38rem;
      line-height: 1.58;
    }

    .cv-bullets li::before {
      content: "•";
      position: absolute;
      left: 0.1rem;
      top: 0;
      color: var(--text-primary);
      font-weight: 700;
    }

    .edu-degree {
      font-family: 'Plus Jakarta Sans', sans-serif;
      font-size: 1.03rem;
      font-weight: 700;
      color: var(--text-primary);
    }

    .edu-status {
      font-size: 0.9rem;
      font-weight: 600;
      color: var(--purple-primary);
      margin: 0.1rem 0;
    }

    .edu-institution {
      font-size: 0.95rem;
      font-weight: 500;
      color: var(--text-primary);
      margin-bottom: 0.45rem;
    }

    .cert-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.65rem;
    }

    .cert-item {
      background-color: #fbf7fd;
      border-left: 3.5px solid var(--purple-primary);
      padding: 0.65rem 1rem;
      border-radius: 0 10px 10px 0;
      font-size: 0.93rem;
      color: var(--text-secondary);
      transition: background-color 0.3s ease, border-color 0.3s ease;
    }

    [data-theme="crimson-gold"] .cert-item {
      background-color: #5A0F1E;
      border-left: 4px solid #b8861b;
    }

    .cert-item strong {
      color: var(--text-primary);
      font-weight: 700;
    }

    .cert-meta {
      display: inline-block;
      color: var(--text-muted);
      font-size: 0.88rem;
      margin-left: 0.25rem;
    }

    .cv-footer {
      margin-top: 2.5rem;
      padding-top: 1rem;
      border-top: 1px solid var(--border-light);
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.82rem;
      color: var(--text-muted);
    }

    /* ==========================================================================
       7. DISEÑO RESPONSIVO (Móvil y Tablet)
       ========================================================================== */
    @media (max-width: 820px) {
      .cv-sheet {
        grid-template-columns: 1fr;
      }

      .botanical-sidebar {
        flex-direction: row;
        padding: 0.85rem 1.5rem;
        height: 82px;
        border-right: none;
        border-bottom: 3px solid var(--purple-soft);
      }

      .sidebar-accent-line {
        display: none;
      }

      .sidebar-badge {
        writing-mode: horizontal-tb;
        transform: none;
        margin: 0;
        font-size: 0.72rem;
      }

      .cv-content {
        padding: 2rem 1.5rem 2.5rem;
      }

      .cv-name {
        font-size: 1.85rem;
      }

      .skills-grid {
        grid-template-columns: 1fr;
        gap: 0.75rem;
      }
    }

    @media (max-width: 480px) {
      body {
        padding: 0.75rem 0.5rem 2rem;
      }

      .top-toolbar {
        border-radius: 14px;
        justify-content: center;
      }

      .cv-name {
        font-size: 1.6rem;
      }

      .cv-role {
        font-size: 1.08rem;
      }
    }

    /* ==========================================================================
       8. ESTILOS DE IMPRESIÓN
       ========================================================================== */
    @media print {
      body {
        background: #ffffff;
        padding: 0;
      }

      .top-toolbar {
        display: none;
      }

      .cv-sheet {
        box-shadow: none;
        border: none;
        border-radius: 0;
        max-width: 100%;
      }

      .cv-content {
        padding: 1.5rem 2rem;
      }
    }
  </style>
</head>

<body>

  <nav class="top-toolbar" aria-label="Curriculum Navigation">
    <div class="nav-links">
      <a href="#profile" data-i18n="nav_profile">Profile</a>
      <a href="#skills" data-i18n="nav_skills">Technical Skills</a>
      <a href="#experience" data-i18n="nav_experience">Experience &amp; Projects</a>
      <a href="#education" data-i18n="nav_education">Education</a>
      <a href="#certifications" data-i18n="nav_certifications">Certifications</a>
    </div>
    <div class="toolbar-controls">
      <button type="button" class="btn-control" id="lang-toggle" aria-label="Switch Language">
        <span id="lang-label">ES / EN</span>
      </button>

      <button type="button" class="btn-print" onclick="window.print()">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2"
          stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
          <polyline points="6 9 6 2 18 2 18 9"></polyline>
          <path d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"></path>
          <rect x="6" y="14" width="12" height="8"></rect>
        </svg>
        <span data-i18n="btn_print">Print / Save PDF</span>
      </button>
    </div>
  </nav>

  <main class="cv-sheet">
    <aside class="botanical-sidebar" aria-hidden="true">
      <span class="sidebar-badge" data-i18n="sidebar_badge">Computer Engineering Portfolio</span>
      <div class="sidebar-accent-line"></div>
    </aside>

    <div class="cv-content">
      <header class="cv-header">
        <h1 class="cv-name">Jade Marquez</h1>
        <p class="cv-role" data-i18n="role">Full stack and mobile computer engineering</p>
        <div class="cv-contact-info">
          <div class="cv-contact-line">
            <span data-i18n="location">Guadalajara, Jalisco, Mexico.</span>
          </div>
          <div class="cv-contact-line">
            <a href="mailto:jademarquez2190@gmail.com">jademarquez2190@gmail.com</a>
          </div>
          <div class="cv-contact-line">
            <a href="mailto:jade.marquez7750@alumnos.udg.mx">jade.marquez7750@alumnos.udg.mx</a>
          </div>
        </div>
      </header>

      <section id="profile" class="cv-section">
        <h2 class="section-title" data-i18n="sec_profile">Professional Profile</h2>
        <p class="profile-text" data-i18n="profile_desc">
          A qualified computer engineer with a strong background in software architecture,
          intelligent systems, web and mobile application development, and real-time
          programming. I possess practical experience across the entire software development life
          cycle, including requirements gathering, front-end and back-end development,
          integration with RESTful APIs, implementation of geolocation services, and unit testing. I
          hold professional certifications in Information Technology, AWS Cloud, and databases; I
          am also experienced in working within Agile/SCRUM environments and possess strong
          communication skills.
        </p>
      </section>

      <section id="skills" class="cv-section">
        <h2 class="section-title" data-i18n="sec_skills">Technical Skills and Competencies</h2>
        <ul class="skills-grid">
          <li class="skill-item" data-i18n="skill_1">
            <strong>Frontend and Mobile:</strong> React, React Native, JavaScript, HTML5/CSS3, Expo, Android Studio
            (Java), Astro, Bootstrap.
          </li>
          <li class="skill-item" data-i18n="skill_2">
            <strong>Backend and Programming Languages:</strong> Python, Node.js, Java, C, C++, C#, Spring Boot, embedded
            and parallel programming, RESTful APIs.
          </li>
          <li class="skill-item" data-i18n="skill_3">
            <strong>AI and Data Science:</strong> Machine Learning (ML), Deep Learning (DL), Artificial Neural Networks,
            Metaheuristic Algorithms.
          </li>
          <li class="skill-item" data-i18n="skill_4">
            <strong>Cloud and Databases:</strong> AWS Cloud, Oracle DB, PostgreSQL, MySQL, Firebase, Docker
            (fundamentals).
          </li>
          <li class="skill-item" data-i18n="skill_5">
            <strong>Tools and Architecture:</strong> Git, GitHub, Blender, Linux, UML Diagrams, Software Architecture.
          </li>
          <li class="skill-item" data-i18n="skill_6">
            <strong>Methodologies and Languages:</strong> SCRUM/Agile, unit testing, English (intermediate B1/B2), and
            Spanish (native).
          </li>
        </ul>
      </section>

      <section id="experience" class="cv-section">
        <h2 class="section-title" data-i18n="sec_experience">Experience and Projects Under Development</h2>

        <article class="experience-item">
          <div class="exp-header">
            <h3 class="exp-title" data-i18n="exp1_title">Project Temis - Mobile App for Geolocation and Urban Risk
              Management</h3>
            <span class="exp-date" data-i18n="exp1_date">Oct 2025 - Jan 2026</span>
            <span class="exp-subtitle" data-i18n="exp1_sub">Lead Developer | Technological and Social Impact
              Project</span>
          </div>
          <ul class="cv-bullets">
            <li data-i18n="exp1_b1">Designed and developed a mobile platform for mapping, tracking, and monitoring urban
              infrastructure risks and public safety in Jalisco.</li>
            <li data-i18n="exp1_b2">Implemented mobile architecture and frontend using React Native, Expo, and Firebase
              for real-time database synchronization.</li>
            <li data-i18n="exp1_b3">Integrated interactive maps and precise geolocation services by consuming custom
              RESTful APIs.</li>
            <li data-i18n="exp1_b4">Drafted technical requirement specifications, UML architecture diagrams, and urban
              risk mitigation metrics.</li>
          </ul>
        </article>

        <article class="experience-item">
          <div class="exp-header">
            <h3 class="exp-title" data-i18n="exp2_title">VR Software Development and Neurological Research Assistant
            </h3>
            <span class="exp-date" data-i18n="exp2_date">Aug 2024 - Apr 2025</span>
            <span class="exp-subtitle" data-i18n="exp2_sub">University of Guadalajara (CUCEI)</span>
          </div>
          <ul class="cv-bullets">
            <li data-i18n="exp2_b1">Developed an interactive 3D/VR digital tool using C# and Unity to assess executive
              functions in older adults.</li>
            <li data-i18n="exp2_b2">Designed accessible user interfaces (UX/UI) and 3D models (using Blender) tailored
              for healthcare applications.</li>
            <li data-i18n="exp2_b3">Collaborated on the integration of backend modules for real-time data collection and
              secure analysis of neurological data.</li>
          </ul>
        </article>

        <article class="experience-item">
          <div class="exp-header">
            <h3 class="exp-title" data-i18n="exp3_title">Mobile Development and Technical Documentation Lead</h3>
            <span class="exp-date" data-i18n="exp3_date">Jan 2024 - May 2024</span>
            <span class="exp-subtitle" data-i18n="exp3_sub">CUCEI Mobile App Hackathon</span>
          </div>
          <ul class="cv-bullets">
            <li data-i18n="exp3_b1">Created a mobile platform focused on financial management and commercial risk
              prevention for Mexican SMEs.</li>
            <li data-i18n="exp3_b2">Developed key features using Android Studio and Java, including dynamic forms and
              inventory dashboards.</li>
            <li data-i18n="exp3_b3">Led technical documentation, UML domain modeling, and agile requirements validation
              with multidisciplinary teams.</li>
          </ul>
        </article>
      </section>

      <section id="education" class="cv-section">
        <h2 class="section-title" data-i18n="sec_education">Education</h2>
        <div class="education-block">
          <h3 class="edu-degree" data-i18n="edu_degree">Bachelor's degree in computer engineering</h3>
          <p class="edu-status" data-i18n="edu_status">Graduate</p>
          <p class="edu-institution" data-i18n="edu_inst">University of Guadalajara &middot; University Center for Exact
            Sciences and Engineering (CUCEI)</p>
          <ul class="cv-bullets">
            <li data-i18n="edu_b1"><strong>Systems Software:</strong> Parallel and real-time programming, embedded
              systems programming, advanced systems programming</li>
            <li data-i18n="edu_b2"><strong>Intelligent Systems:</strong> Machine learning, metaheuristic algorithms,
              artificial neural networks, and deep learning</li>
          </ul>
        </div>
      </section>

      <section id="certifications" class="cv-section">
        <h2 class="section-title" data-i18n="sec_certifications">Certifications</h2>
        <ul class="cert-list">
          <li class="cert-item">
            <strong>Learn, Connect, Transform Database with Oracle</strong>
            <span class="cert-meta" data-i18n="cert1_meta">/ Oracle &bull; 1-Nov-2025 — 31-Mar-2026</span>
          </li>
          <li class="cert-item">
            <strong>Introduction to Information Technology and AWS Cloud</strong>
            <span class="cert-meta" data-i18n="cert2_meta">/ AWS &bull; February 23, 2025</span>
          </li>
        </ul>
      </section>

      <footer class="cv-footer">
        <span>Jade Marquez &mdash; Curriculum Vitae</span>
      </footer>
    </div>
  </main>

  <script>
    const translations = {
      en: {
        nav_profile: "Profile",
        nav_skills: "Technical Skills",
        nav_experience: "Experience & Projects",
        nav_education: "Education",
        nav_certifications: "Certifications",
        btn_print: "Print / Save PDF",
        sidebar_badge: "Computer Engineering Portfolio",
        role: "Full stack and mobile computer engineering",
        location: "Guadalajara, Jalisco, Mexico.",
        footer_loc: "Guadalajara, Jalisco, Mexico",
        sec_profile: "Professional Profile",
        profile_desc: "A qualified computer engineer with a strong background in software architecture, intelligent systems, web and mobile application development, and real-time programming. I possess practical experience across the entire software development life cycle, including requirements gathering, front-end and back-end development, integration with RESTful APIs, implementation of geolocation services, and unit testing. I hold professional certifications in Information Technology, AWS Cloud, and databases; I am also experienced in working within Agile/SCRUM environments and possess strong communication skills.",
        sec_skills: "Technical Skills and Competencies",
        skill_1: "<strong>Frontend and Mobile:</strong> React, React Native, JavaScript, HTML5/CSS3, Expo, Android Studio (Java), Astro, Bootstrap.",
        skill_2: "<strong>Backend and Programming Languages:</strong> Python, Node.js, Java, C, C++, C#, Spring Boot, embedded and parallel programming, RESTful APIs.",
        skill_3: "<strong>AI and Data Science:</strong> Machine Learning (ML), Deep Learning (DL), Artificial Neural Networks, Metaheuristic Algorithms.",
        skill_4: "<strong>Cloud and Databases:</strong> AWS Cloud, Oracle DB, PostgreSQL, MySQL, Firebase, Docker (fundamentals).",
        skill_5: "<strong>Tools and Architecture:</strong> Git, GitHub, Blender, Linux, UML Diagrams, Software Architecture.",
        skill_6: "<strong>Methodologies and Languages:</strong> SCRUM/Agile, unit testing, English (intermediate B1/B2), and Spanish (native).",
        sec_experience: "Experience and Projects Under Development",
        exp1_title: "Project Temis - Mobile App for Geolocation and Urban Risk Management",
        exp1_date: "Oct 2025 - Jan 2026",
        exp1_sub: "Lead Developer | Technological and Social Impact Project",
        exp1_b1: "Designed and developed a mobile platform for mapping, tracking, and monitoring urban infrastructure risks and public safety in Jalisco.",
        exp1_b2: "Implemented mobile architecture and frontend using React Native, Expo, and Firebase for real-time database synchronization.",
        exp1_b3: "Integrated interactive maps and precise geolocation services by consuming custom RESTful APIs.",
        exp1_b4: "Drafted technical requirement specifications, UML architecture diagrams, and urban risk mitigation metrics.",
        exp2_title: "VR Software Development and Neurological Research Assistant",
        exp2_date: "Aug 2024 - Apr 2025",
        exp2_sub: "University of Guadalajara (CUCEI)",
        exp2_b1: "Developed an interactive 3D/VR digital tool using C# and Unity to assess executive functions in older adults.",
        exp2_b2: "Designed accessible user interfaces (UX/UI) and 3D models (using Blender) tailored for healthcare applications.",
        exp2_b3: "Collaborated on the integration of backend modules for real-time data collection and secure analysis of neurological data.",
        exp3_title: "Mobile Development and Technical Documentation Lead",
        exp3_date: "Jan 2024 - May 2024",
        exp3_sub: "CUCEI Mobile App Hackathon",
        exp3_b1: "Created a mobile platform focused on financial management and commercial risk prevention for Mexican SMEs.",
        exp3_b2: "Developed key features using Android Studio and Java, including dynamic forms and inventory dashboards.",
        exp3_b3: "Led technical documentation, UML domain modeling, and agile requirements validation with multidisciplinary teams.",
        sec_education: "Education",
        edu_degree: "Bachelor's degree in computer engineering",
        edu_status: "Graduate",
        edu_inst: "University of Guadalajara &middot; University Center for Exact Sciences and Engineering (CUCEI)",
        edu_b1: "<strong>Systems Software:</strong> Parallel and real-time programming, embedded systems programming, advanced systems programming",
        edu_b2: "<strong>Intelligent Systems:</strong> Machine learning, metaheuristic algorithms, artificial neural networks, and deep learning",
        sec_certifications: "Certifications",
        cert1_meta: "/ Oracle &bull; 1-Nov-2025 — 31-Mar-2026",
        cert2_meta: "/ AWS &bull; February 23, 2025"
      },
      es: {
        nav_profile: "Perfil",
        nav_skills: "Habilidades",
        nav_experience: "Experiencia y Proyectos",
        nav_education: "Educación",
        nav_certifications: "Certificaciones",
        btn_print: "Imprimir / Guardar PDF",
        sidebar_badge: "Portafolio Ingeniería en Computación",
        role: "Ingeniera en Computación Full Stack y Móvil",
        location: "Guadalajara, Jalisco, México.",
        footer_loc: "Guadalajara, Jalisco, México",
        sec_profile: "Perfil Profesional",
        profile_desc: "Ingeniera en computación titulada con sólida formación en arquitectura de software, sistemas inteligentes, desarrollo de aplicaciones web y móviles, y programación en tiempo real. Cuento con experiencia práctica en todo el ciclo de vida del desarrollo de software, incluyendo levantamiento de requerimientos, desarrollo front-end y back-end, integración de APIs RESTful, implementación de servicios de geolocalización y pruebas unitarias. Poseo certificaciones profesionales en Tecnologías de la Información, AWS Cloud y bases de datos; tengo experiencia trabajando en entornos Ágiles/SCRUM y fuertes habilidades de comunicación.",
        sec_skills: "Habilidades Técnicas y Competencias",
        skill_1: "<strong>Frontend y Móvil:</strong> React, React Native, JavaScript, HTML5/CSS3, Expo, Android Studio (Java), Astro, Bootstrap.",
        skill_2: "<strong>Backend y Lenguajes de Programación:</strong> Python, Node.js, Java, C, C++, C#, Spring Boot, programación embebida y paralela, APIs RESTful.",
        skill_3: "<strong>IA y Ciencia de Datos:</strong> Machine Learning (ML), Deep Learning (DL), Redes Neuronales Artificiales, Algoritmos Metaheurísticos.",
        skill_4: "<strong>Nube y Bases de Datos:</strong> AWS Cloud, Oracle DB, PostgreSQL, MySQL, Firebase, Docker (fundamentos).",
        skill_5: "<strong>Herramientas y Arquitectura:</strong> Git, GitHub, Blender, Linux, Diagramas UML, Arquitectura de Software.",
        skill_6: "<strong>Metodologías e Idiomas:</strong> SCRUM/Agile, pruebas unitarias, Inglés (intermedio B1/B2) y Español (nativo).",
        sec_experience: "Experiencia y Proyectos en Desarrollo",
        exp1_title: "Proyecto Temis - App Móvil de Geolocalización y Gestión de Riesgos Urbanos",
        exp1_date: "Oct 2025 - Ene 2026",
        exp1_sub: "Desarrolladora Líder | Proyecto de Impacto Tecnológico y Social",
        exp1_b1: "Diseñé y desarrollé una plataforma móvil para el mapeo, seguimiento y monitoreo de riesgos de infraestructura urbana y seguridad pública en Jalisco.",
        exp1_b2: "Implementé la arquitectura móvil y el frontend utilizando React Native, Expo y Firebase para la sincronización de bases de datos en tiempo real.",
        exp1_b3: "Integré mapas interactivos y servicios de geolocalización precisa consumiendo APIs RESTful personalizadas.",
        exp1_b4: "Redacté especificaciones de requerimientos técnicos, diagramas de arquitectura UML y métricas de mitigación de riesgos urbanos.",
        exp2_title: "Desarrollo de Software VR y Asistente de Investigación Neurológica",
        exp2_date: "Ago 2024 - Abr 2025",
        exp2_sub: "Universidad de Guadalajara (CUCEI)",
        exp2_b1: "Desarrollé una herramienta digital interactiva 3D/VR con C# y Unity para evaluar funciones ejecutivas en adultos mayores.",
        exp2_b2: "Diseñé interfaces de usuario accesibles (UX/UI) y modelos 3D (con Blender) adaptados a aplicaciones del sector salud.",
        exp2_b3: "Colaboré en la integración de módulos backend para la recolección en tiempo real y el análisis seguro de datos neurológicos.",
        exp3_title: "Líder de Desarrollo Móvil y Documentación Técnica",
        exp3_date: "Ene 2024 - May 2024",
        exp3_sub: "Hackathon de Aplicaciones Móviles CUCEI",
        exp3_b1: "Creé una plataforma móvil enfocada en la gestión financiera y prevención de riesgos comerciales para PyMEs mexicanas.",
        exp3_b2: "Desarrollé funcionalidades clave usando Android Studio y Java, incluyendo formularios dinámicos y paneles de inventario.",
        exp3_b3: "Lideré la documentación técnica, el modelado de dominio UML y la validación ágil de requerimientos con equipos multidisciplinarios.",
        sec_education: "Educación",
        edu_degree: "Ingeniería en Computación",
        edu_status: "Titulada",
        edu_inst: "Universidad de Guadalajara &middot; Centro Universitario de Ciencias Exactas e Ingenierías (CUCEI)",
        edu_b1: "<strong>Software de Sistemas:</strong> Programación paralela y en tiempo real, programación de sistemas embebidos, programación avanzada de sistemas",
        edu_b2: "<strong>Sistemas Inteligentes:</strong> Aprendizaje automático (Machine Learning), algoritmos metaheurísticos, redes neuronales artificiales y aprendizaje profundo",
        sec_certifications: "Certificaciones",
        cert1_meta: "/ Oracle &bull; 1-Nov-2025 — 31-Mar-2026",
        cert2_meta: "/ AWS &bull; 23 de Febrero de 2025"
      }
    };

    let currentLang = 'en';
    const langToggleBtn = document.getElementById('lang-toggle');
    const langLabel = document.getElementById('lang-label');

    function setLanguage(lang) {
      currentLang = lang;
      document.documentElement.lang = lang;
      langLabel.textContent = lang === 'en' ? 'Español' : 'English';

      document.querySelectorAll('[data-i18n]').forEach((el) => {
        const key = el.getAttribute('data-i18n');
        if (translations[lang] && translations[lang][key]) {
          el.innerHTML = translations[lang][key];
        }
      });
    }

    langToggleBtn.addEventListener('click', () => {
      setLanguage(currentLang === 'en' ? 'es' : 'en');
    });

    setLanguage('en');
  </script>
</body>

</html>
