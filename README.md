<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Tiriveedhi Sai Venkatesh | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      color: #fff;
      min-height: 100vh;
      background: #fff;
      position: relative;
      padding-bottom: 90px;
      overflow-x: hidden;
    }
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      z-index: -1;
      background:
        linear-gradient(rgba(255,255,255,0.4), rgba(255,255,255,0.4)),
        url('https://www.intelligentcio.com/apac/wp-content/uploads/sites/44/2024/07/AdobeStock_592969307-1.jpg') no-repeat center center fixed;
      background-size: cover;
      filter: brightness(1.08) contrast(1.05);
    }
    nav {
      background: rgba(0,115,177,0.85);
      position: sticky;
      top: 0;
      z-index: 10;
      box-shadow: 0 2px 8px rgba(0,0,0,0.3);
    }
    .nav-container {
      max-width: 900px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 16px;
      flex-wrap: wrap;
      position: relative;
    }
    .logo {
      color: #fff;
      font-size: 1.4em;
      font-weight: bold;
      padding: 16px 0;
      flex: 1 1 150px;
      letter-spacing: 1px;
    }
    nav ul {
      list-style: none;
      display: flex;
      margin: 0;
      padding: 0;
      flex-wrap: wrap;
      flex: 3 1 600px;
    }
    nav ul li {
      margin-left: 24px;
      margin-bottom: 8px;
    }
    nav ul li:first-child {
      margin-left: 0;
    }
    nav ul li a {
      color: #fff;
      text-decoration: none;
      padding: 16px 0;
      display: inline-block;
      transition: border-bottom 0.2s;
      border-bottom: 2px solid transparent;
      font-size: 1em;
      cursor: pointer;
      white-space: nowrap;
    }
    nav ul li a.active,
    nav ul li a:hover {
      border-bottom: 2px solid #1dbab4;
    }
    .container {
      max-width: 900px;
      margin: 40px auto;
      background: rgba(0,0,0,0.68);
      border-radius: 18px;
      box-shadow: 0 4px 24px rgba(0,0,0,0.3);
      padding: 32px;
      min-height: 400px;
      position: relative;
      z-index: 5;
      text-shadow: 0 0 6px rgba(0,0,0,0.85);
      transition: background 0.3s;
    }
    .exp-counter-inline {
      font-size: 1em;
      font-weight: 500;
      color: #222;
      background: rgba(234, 246, 251, 0.7);
      display: flex;
      align-items: center;
      gap: 7px;
      margin-bottom: 16px;
      padding: 6px 16px 6px 10px;
      border-radius: 6px;
      width: fit-content;
      box-shadow: 0 1px 6px rgba(21,97,173,0.08);
      border-left: 4px solid #1561ad;
      letter-spacing: 0.2px;
      user-select: none;
    }
    .exp-dot {
      display: inline-block;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: #23d160;
      margin-left: 3px;
      margin-right: 0;
      box-shadow: 0 0 5px #23d16077;
      vertical-align: middle;
      transition: background 0.2s;
    }
    .exp-dot.off {
      background: #bbb;
      box-shadow: 0 0 4px #bbb7;
    }
    @media (max-width: 600px) {
      .exp-counter-inline {
        font-size: 1em;
        margin: 10px auto 12px auto;
        width: 98%;
        justify-content: center;
        border-radius: 10px;
        border-left: none;
        border-top: 4px solid #1561ad;
        padding-left: 0;
        padding-top: 8px;
      }
      .nav-container {
        flex-direction: column;
        align-items: flex-start;
      }
    }
    .section {
      display: none;
      animation: fadeIn 0.5s;
    }
    .section.active-section {
      display: block;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    .home-header {
      text-align: center;
      margin-bottom: 30px;
    }
    .home-header h1 {
      margin: 0 0 8px 0;
      font-size: 2.2em;
      font-family: 'Georgia', serif;
      letter-spacing: 0.5px;
      color: #fff;
      text-shadow: 0 2px 12px rgba(0,0,0,0.35);
    }
    .home-header h2 {
      margin: 0 0 10px 0;
      font-size: 1.25em;
      font-weight: 400;
      color: #cce6fa;
      letter-spacing: 0.5px;
    }
    .home-header p {
      margin: 0 auto 24px auto;
      font-size: 1.1em;
      color: #e0e0e0;
      max-width: 600px;
      text-align: justify;
      text-shadow: 0 2px 10px rgba(0,0,0,0.35);
    }
    .skills-photo-grid {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 40px;
      margin-bottom: 28px;
      flex-wrap: wrap;
    }
    .skills-list {
      display: flex;
      flex-direction: column;
      gap: 18px;
      font-size: 1.07em;
      font-weight: 500;
      min-width: 160px;
    }
    .skills-left {
      align-items: flex-end;
      text-align: right;
    }
    .skills-right {
      align-items: flex-start;
      text-align: left;
    }
    .skills-list div {
      background: #eaf6fb;
      color: #1561ad;
      border: 1px solid #1561ad;
      padding: 7px 18px;
      border-radius: 18px;
      margin: 0 0 0 0;
      box-shadow: 0 2px 8px rgba(21,97,173,0.04);
      display: inline-block;
      font-weight: 600;
      letter-spacing: 0.5px;
      transition: background 0.2s, color 0.2s;
    }
    .skills-list div:hover {
      background: #1561ad;
      color: #fff;
    }
    .skills-list-main {
      list-style: disc inside;
      margin: 0 0 18px 0;
      padding-left: 16px;
      color: #eaf6fb;
      font-size: 1.07em;
    }
    .skills-list-main li {
      margin-bottom: 7px;
      color: #eaf6fb;
      letter-spacing: 0.2px;
    }
    .skills-list-main li b {
      color: #1561ad;
    }
    .home-photo-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .home-photo-square {
      width: 260px;
      height: 260px;
      border-radius: 16px;
      object-fit: cover;
      border: 6px solid #fff;
      box-shadow: 0 4px 24px rgba(0,0,0,0.28);
      background: #222;
      display: block;
    }
    .section-title {
      color: #7ec8e3;
      font-size: 1.1em;
      margin-bottom: 12px;
      text-transform: uppercase;
      letter-spacing: 1px;
      font-weight: 700;
      text-shadow: 0 0 4px rgba(0,0,0,0.7);
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 16px;
      background: rgba(255,255,255,0.12);
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 2px 8px rgba(0,0,0,0.35);
      color: #fff;
      text-shadow: none;
    }
    th, td {
      padding: 12px 10px;
      text-align: left;
      vertical-align: top;
    }
    th {
      background: #1561ad;
      color: #fff;
      font-weight: 600;
      font-size: 1em;
    }
    tr:nth-child(even) td {
      background: rgba(21,97,173,0.09);
    }
    tr:hover td {
      background: rgba(21,97,173,0.16);
    }
    .achieve-list {
      color: #eee;
      font-size: 1.07em;
      margin-bottom: 12px;
    }
    .contact-form input, .contact-form textarea {
      width: 100%;
      max-width: 400px;
      padding: 8px;
      margin-top: 4px;
      border: 1px solid #555;
      border-radius: 6px;
      font-size: 1em;
      background: rgba(255,255,255,0.15);
      color: #eee;
    }
    .contact-form input::placeholder,
    .contact-form textarea::placeholder {
      color: #ccc;
    }
    .contact-form button {
      background: #0073b1;
      color: #fff;
      border: none;
      padding: 10px 24px;
      border-radius: 6px;
      font-size: 1em;
      cursor: pointer;
      margin-top: 12px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.3);
      transition: background-color 0.3s ease;
    }
    .contact-form button:hover {
      background: #005983;
    }
    .footer {
      position: fixed;
      left: 0;
      bottom: 0;
      width: 100%;
      background: rgba(0,115,177,0.95);
      color: #fff;
      text-align: center;
      padding: 12px 0 8px 0;
      font-size: 1em;
      z-index: 200;
      letter-spacing: 0.5px;
      box-shadow: 0 -2px 8px rgba(0,0,0,0.3);
    }
    .footer a {
      color: #fff;
      text-decoration: underline;
      margin: 0 10px;
    }
    @media (max-width: 900px) {
      .skills-photo-grid { flex-direction: column; gap: 18px; }
      .skills-list { min-width: 0; align-items: center; text-align: center; }
    }
    @media (max-width: 600px) {
      .container { padding: 12px; }
      nav ul { flex-direction: column; }
      nav ul li { margin: 0 0 8px 0; }
      .skills-list { flex-direction: row; gap: 10px; }
      table, th, td { font-size: 0.95em; }
      .footer { font-size: 0.95em; }
      .home-header h1 { font-size: 1.3em; }
      .home-photo-square { width: 140px; height: 140px; }
    }
  </style>
</head>
<body>
  <nav>
    <div class="nav-container">
      <span class="logo"></span>
      <ul>
        <li><a href="#" class="active" data-section="profile">Home</a></li>
        <li><a href="#" data-section="experience">Experience</a></li>
        <li><a href="#" data-section="education">Education</a></li>
        <li><a href="#" data-section="certifications">Certifications</a></li>
        <li><a href="#" data-section="skills">Skills</a></li>
        <li><a href="#" data-section="achievements">Achievements</a></li>
        <li><a href="#" data-section="projects">Projects</a></li>
        <li><a href="#" data-section="contact">Contact</a></li>
      </ul>
    </div>
  </nav>
  <div class="container">
    <div class="exp-counter-inline" id="exp-counter-inline">
      <span>Professional Experience:</span>
      <span id="exp-value-inline">Calculating...</span>
      <span class="exp-dot" id="exp-dot"></span>
    </div>

    <!-- Home Landing Section -->
    <div class="section active-section" id="profile">
      <div class="home-header">
        <h1>Tiriveedhi Sai Venkatesh</h1>
        <h2>Sr. Analyst in Capgemini | Boomi Integration Developer</h2>
        <p>
          As a skilled Boomi integration specialist, I connect business applications and technologies to ensure secure, scalable, and efficient data flow across all environments. By leveraging the Boomi platform for end-to-end integration, I help organizations streamline processes, automate workflows, and maintain smooth information exchange throughout their digital landscape.
        </p>
      </div>
      <div class="skills-photo-grid">
        <div class="skills-list skills-left">
          <div>Boomi Integration</div>
          <div>Boomi API Management</div>
          <div>Boomi Event Streams</div>
          <div>NetSuite/Salesforce</div>
        </div>
        <div class="home-photo-container">
          <img src="https://drive.google.com/thumbnail?id=1zi6ER1EPlc2cj37huNiGDRLUgYVXU3B5&sz=w1000" alt="Profile Photo" class="home-photo-square" />
        </div>
        <div class="skills-list skills-right">
          <div>HTML/CSS</div>
          <div>SQL/PLSQL</div>
          <div>XML/JSON</div>
        </div>
      </div>
    </div>

    <!-- Experience Section (REVERSE CHRONOLOGICAL ORDER) -->
    <div class="section" id="experience">
      <div class="section-title">Experience</div>
      <table>
        <thead>
          <tr>
            <th>Role</th>
            <th>Company</th>
            <th>Duration</th>
            <th>Key Responsibilities</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Senior Analyst</td>
            <td>Capgemini</td>
            <td>Jun 2024 – Present</td>
            <td>
              <ul>
                <li>Leading Boomi integration projects for enterprise clients.</li>
                <li>Developing and maintaining scalable integration solutions.</li>
                <li>Giving innovative ideas with solutions and overseeing project delivery.</li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>Analyst</td>
            <td>Capgemini</td>
            <td>Jun 2023 – May 2024</td>
            <td>
              <ul>
                <li>Sync the Accounts & products details between Salesforce and Database.</li>
                <li>Integration of a PLM system with NetSuite.</li>
                <li>Sync of Transactions Details between NetSuite and Client’s shipment scanning device.</li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>Software Analyst</td>
            <td>Capgemini</td>
            <td>Dec 2022 – May 2023</td>
            <td>
              <ul>
                <li>Worked on NetSuite techno functional roles and Boomi.</li>
                <li>Learning Boomi & NetSuite.</li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>
    </div>

    <!-- Education Section -->
    <div class="section" id="education">
      <div class="section-title">Education</div>
      <table>
        <thead>
          <tr>
            <th>Qualification</th>
            <th>Institution</th>
            <th>Year</th>
            <th>Details</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>B.Tech in Electronics and Communication Engineering</td>
            <td>Ramachandra College of Engineering, Eluru</td>
            <td>2018 – 2022</td>
            <td>Graduated with First Class 76%</td>
          </tr>
          <tr>
            <td>Intermediate (MPC)</td>
            <td>Vidya Vikas Junior College</td>
            <td>2016 – 2018</td>
            <td>Completed with distinction 90%</td>
          </tr>
          <tr>
            <td>SSC</td>
            <td>St. Mary’s English Medium High School, Kamavarapukota</td>
            <td>2016</td>
            <td>Completed SSC Board 90%</td>
          </tr>
        </tbody>
      </table>
    </div>

    <!-- Certifications Section -->
    <div class="section" id="certifications">
      <div class="section-title">Certifications</div>
      <table>
        <thead>
          <tr>
            <th>Certification Name</th>
            <th>Issuing Organization</th>
            <th>Year/Version</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>Boomi Associate Master Data Hub Certification</td><td>Boomi</td><td>-</td><td>Completed</td></tr>
          <tr><td>Boomi Professional API Design Certification</td><td>Boomi</td><td>-</td><td>Completed</td></tr>
          <tr><td>Boomi Associate Integration Certification</td><td>Boomi</td><td>-</td><td>Completed</td></tr>
          <tr><td>Boomi Professional Integration Certification</td><td>Boomi</td><td>-</td><td>Completed</td></tr>
          <tr><td>Boomi Associate Event Streams Certification</td><td>Boomi</td><td>-</td><td>Completed</td></tr>
          <tr><td>Celigo Fundamentals Level 1</td><td>Celigo</td><td>-</td><td>Completed</td></tr>
          <tr><td>Celigo Fundamentals Level 2</td><td>Celigo</td><td>-</td><td>Completed</td></tr>
          <tr><td>Automation Pro 1 Certification</td><td>Workato</td><td>-</td><td>Completed</td></tr>
          <tr><td>Automation Pro 2 Certification</td><td>Workato</td><td>-</td><td>Completed</td></tr>
          <tr><td>Oracle Cloud Infrastructure 2024 Generative AI Certified Professional</td><td>Oracle</td><td>2024</td><td>Completed</td></tr>
          <tr><td>Oracle Cloud Infrastructure Certification</td><td>Oracle</td><td>-</td><td>Completed</td></tr>
          <tr><td>Oracle Cloud Data Management 2023 Certified Foundations Associate</td><td>Oracle</td><td>2023</td><td>Completed</td></tr>
          <tr><td>SQL Certification</td><td>-</td><td>-</td><td>Completed</td></tr>
          <tr><td>Agile Software Certification</td><td>-</td><td>-</td><td>Completed</td></tr>
        </tbody>
      </table>
    </div>

    <!-- Skills Section -->
    <div class="section" id="skills">
      <div class="section-title">Professional Skills</div>
      <ul class="skills-list-main">
        <li>Proficient in Boomi Integration development, including process design and deployment.</li>
        <li>Hands-on expertise in Boomi Master Data Hub (MDH) for centralized data management.</li>
        <li>Skilled in implementing Boomi Event Streams for real-time data integration.</li>
        <li>Experienced in designing and managing APIs using Boomi API Management.</li>
        <li>Strong knowledge of SQL and PL/SQL for database querying and programming.</li>
        <li>Proficient in front-end technologies: HTML and CSS.</li>
        <li>Adept at working with data formats such as JSON and XML.</li>
        <li>Solid understanding of relational databases and data modeling.</li>
        <li>Practical experience integrating with enterprise applications including:
          <ul>
            <li>NetSuite</li>
            <li>Snowflake</li>
            <li>Salesforce</li>
            <li>Anaplan</li>
            <li>OneTrust</li>
          </ul>
        </li>
        <li>Experience connecting to client applications via HTTP endpoints and APIs.</li>
      </ul>
    </div>

    <!-- Achievements Section -->
    <div class="section" id="achievements">
      <div class="section-title">Achievements</div>
      <ul class="achieve-list">
        <li>Got good rating in Capgemini (2024)</li>
      </ul>
    </div>

    <!-- Projects Section -->
    <div class="section" id="projects">
      <div class="section-title">Projects</div>
      <div class="project">
        <div class="proj-title"><b>Enterprise Integration Platform</b></div>
        <div class="proj-desc">
          <p>Designed and implemented an enterprise integration platform using Boomi, connecting multiple business systems for seamless data flow.</p>
        </div>
      </div>
    </div>

    <!-- Contact Section -->
    <div class="section" id="contact">
      <div class="section-title">Contact</div>
      <p>You can reach me at:</p>
      <ul>
        <li>Email: <a href="mailto:saivenkateshtiriveedhi@gmail.com">saivenkateshtiriveedhi@gmail.com</a></li>
        <li>LinkedIn: <a href="https://www.linkedin.com/in/tiriveedhi-sai-venkatesh-31b5a71ab" target="_blank">linkedin.com/in/tiriveedhi-sai-venkatesh-31b5a71ab</a></li>
        <li>Phone: +91-XXXXXXXXXX</li>
      </ul>
      <form class="contact-form" onsubmit="alert('Thank you for your message!'); return false;">
        <label>Name:<br />
          <input type="text" name="name" required />
        </label><br /><br />
        <label>Email:<br />
          <input type="email" name="email" required />
        </label><br /><br />
        <label>Message:<br />
          <textarea name="message" rows="5" required></textarea>
        </label><br /><br />
        <button type="submit">Send</button>
      </form>
    </div>
  </div>

  <div class="footer">
    <span>
      <b>Contact:</b>
      <a href="mailto:saivenkateshtiriveedhi@gmail.com">saivenkateshtiriveedhi@gmail.com</a> |
      <a href="https://www.linkedin.com/in/tiriveedhi-sai-venkatesh-31b5a71ab" target="_blank">LinkedIn</a> |
      <span>+91-XXXXXXXXXX</span>
    </span>
  </div>

  <script>
    // Tab navigation logic for top nav
    const navLinks = document.querySelectorAll('nav ul li a');
    const sections = document.querySelectorAll('.section');

    function showHideExperienceCounter(sectionId) {
      const expCounter = document.getElementById('exp-counter-inline');
      if (sectionId === 'profile' || sectionId === 'experience') {
        expCounter.style.display = 'flex';
      } else {
        expCounter.style.display = 'none';
      }
    }

    // Initial check (on page load)
    showHideExperienceCounter('profile');

    navLinks.forEach(link => {
      link.addEventListener('click', e => {
        e.preventDefault();
        navLinks.forEach(l => l.classList.remove('active'));
        link.classList.add('active');
        sections.forEach(s => s.classList.remove('active-section'));
        const target = link.getAttribute('data-section');
        document.getElementById(target).classList.add('active-section');
        showHideExperienceCounter(target);
      });
    });

    // Professional Experience Counter (inline, green dot toggles every 2 seconds)
    function updateExperienceCounterInline() {
      const joinDate = new Date(2022, 11, 1); // Dec 1, 2022
      const now = new Date();
      let months = (now.getFullYear() - joinDate.getFullYear()) * 12 + (now.getMonth() - joinDate.getMonth());
      if (now.getDate() < joinDate.getDate()) months--;
      months = Math.max(0, months);
      const years = Math.floor(months / 12);
      const remMonths = months % 12;
      let text = '';
      if (years > 0) text += years + (years === 1 ? ' year' : ' years');
      if (remMonths > 0 || years === 0) {
        if (years > 0) text += ' ';
        text += remMonths + (remMonths === 1 ? ' month' : ' months');
      }
      document.getElementById('exp-value-inline').textContent = text;
    }
    updateExperienceCounterInline();
    setInterval(updateExperienceCounterInline, 1000 * 60 * 60);

    // Toggle the green dot every 2 seconds
    setInterval(function() {
      document.getElementById('exp-dot').classList.toggle('off');
    }, 2000);
  </script>
</body>
</html>
