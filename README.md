<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Tiriveedhi Sai Venkatesh | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <!-- Your styles remain unchanged -->
  <style>
    /* (All your CSS here, unchanged for brevity) */
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
    <!-- ... All your sections remain unchanged ... -->
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
  document.addEventListener('DOMContentLoaded', function() {
    // Tab navigation logic for top nav
    const navLinks = document.querySelectorAll('nav ul li a');
    const sections = document.querySelectorAll('.section');

    function showHideExperienceCounter(sectionId) {
      const expCounter = document.getElementById('exp-counter-inline');
      if (!expCounter) return;
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
        const targetSection = document.getElementById(target);
        if (targetSection) {
          targetSection.classList.add('active-section');
          showHideExperienceCounter(target);
        }
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
      const expValue = document.getElementById('exp-value-inline');
      if (expValue) expValue.textContent = text;
    }
    updateExperienceCounterInline();
    setInterval(updateExperienceCounterInline, 1000 * 60 * 60);

    // Toggle the green dot every 2 seconds
    setInterval(function() {
      const expDot = document.getElementById('exp-dot');
      if (expDot) expDot.classList.toggle('off');
    }, 2000);
  });
  </script>
</body>
</html>
