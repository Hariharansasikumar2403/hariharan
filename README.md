<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hariharan S — Futuristic Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b0c10;
      --accent:#00ffea;
      --text:#00ffea;
      --muted:#0f3c3c;
      --card-bg:rgba(0,255,234,0.05);
      --shadow:0 10px 40px rgba(0,255,234,.25);
      --radius:12px;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    body{font-family:'Orbitron', sans-serif;background:#0b0c10;color:var(--text);overflow-x:hidden;}
    body::before{content:'';position:fixed;top:0;left:0;width:100%;height:100%;
      background: radial-gradient(circle at 50% 50%, rgba(0,255,234,0.05), transparent 70%),
                  repeating-linear-gradient(0deg, rgba(0,255,234,0.05) 0px, rgba(0,255,234,0.05) 1px, transparent 1px, transparent 4px),
                  repeating-linear-gradient(90deg, rgba(0,255,234,0.05) 0px, rgba(0,255,234,0.05) 1px, transparent 1px, transparent 4px);
      z-index:-1;animation:pulse 6s infinite alternate;}
    @keyframes pulse{0%{opacity:0.05;}50%{opacity:0.12;}100%{opacity:0.05;}}
    .container{max-width:1000px;margin:40px auto;padding:20px}
    header{display:flex;justify-content:space-between;align-items:center;margin-bottom:30px;flex-wrap:wrap}
    header h1{font-size:40px;letter-spacing:2px;color:var(--accent)}
    nav a{margin:0 10px;color:var(--accent);cursor:pointer;text-decoration:none;font-weight:600;}
    nav a.active{color:#fff;border-bottom:2px solid var(--accent);}
    .card{background:var(--card-bg);padding:20px;border-radius:var(--radius);margin-bottom:20px;box-shadow:var(--shadow);border:1px solid rgba(0,255,234,0.2);display:none;}
    .section-title{font-size:28px;color:var(--accent);margin-bottom:15px}
    .list li{margin-bottom:8px}
    .kv{display:grid;grid-template-columns:150px 1fr;margin-bottom:10px}
    .kv .k{color:var(--muted)}
    .home-photo{width:200px;height:200px;border-radius:50%;object-fit:cover;margin-bottom:20px;}
    .certificate-gallery{display:flex;flex-direction:column;align-items:center;gap:20px;}
    .certificate-gallery img{width:90%;max-width:800px;border-radius:12px;box-shadow:0 0 25px rgba(0,255,234,.3);}
    @media(max-width:768px){.kv{grid-template-columns:1fr} header{flex-direction:column;align-items:flex-start}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Hariharan S</h1>
      <nav>
        <a class="active" onclick="showSection('home', event)">Home</a>
        <a onclick="showSection('about', event)">About</a>
        <a onclick="showSection('education', event)">Education</a>
        <a onclick="showSection('skills', event)">Skills</a>
        <a onclick="showSection('projects', event)">Projects</a>
        <a onclick="showSection('contact', event)">Contact</a>
        <a onclick="showSection('certificates', event)">Certificates</a>
      </nav>
    </header>

    <!-- Home -->
    <div id="home" class="card" style="display:block;text-align:center;">
      <img src="hariharan.jpg" alt="Hariharan S" class="home-photo">
      <div class="section-title">Welcome to My Portfolio</div>
      <p>Hello! I am Hariharan S, a passionate BCA student exploring futuristic web and app development.</p>
    </div>

    <!-- About -->
    <div id="about" class="card">
      <div class="section-title">About Me</div>
      <p>Hello! I am a BCA student who loves designing and developing modern web and app interfaces with a futuristic touch.</p>
      <div class="kv"><div class="k">Age</div><div>19</div></div>
      <div class="kv"><div class="k">DOB</div><div>18/09/2006</div></div>
      <div class="kv"><div class="k">Gender</div><div>Male</div></div>
    </div>

    <!-- Education -->
    <div id="education" class="card">
      <div class="section-title">Education</div>
      <div class="kv"><div class="k">College</div><div>Prince Shri Venkateswara Arts & Science College, Gowrivakkam</div></div>
      <div class="kv"><div class="k">Program</div><div>BCA (Bachelor of Computer Applications)</div></div>
    </div>

    <!-- Skills -->
    <div id="skills" class="card">
      <div class="section-title">Skills</div>
      <ul class="list">
        <li><strong>Basic coding knowledge</strong> — HTML, CSS, JavaScript</li>
        <li><strong>Leadership</strong> — guiding teams and managing tasks</li>
        <li><strong>Problem-solving</strong> — debugging and optimization</li>
        <li><strong>Design sense</strong> — futuristic UI & clean layouts</li>
      </ul>
    </div>

    <!-- Projects -->
    <div id="projects" class="card">
      <div class="section-title">Projects</div>
      <ul class="list">
        <li>Portfolio Website — tech-futuristic interface</li>
        <li>UI Card Components — interactive & reusable designs</li>
        <li>JavaScript Mini-Projects — DOM animations & interactivity</li>
      </ul>
    </div>

    <!-- Contact -->
    <div id="contact" class="card">
      <div class="section-title">Contact</div>
      <div class="kv"><div class="k">Phone</div><div><a href="tel:+919962762403">+91 99627 62403</a></div></div>
      <div class="kv"><div class="k">Email</div><div><a href="mailto:13227bca2024@princescience.in">13227bca2024@princescience.in</a></div></div>
      <div class="kv"><div class="k">Instagram</div><div><a href="https://instagram.com/h2_haran" target="_blank">@h2_haran</a></div></div>
      <div class="kv"><div class="k">Location</div><div>Chennai, India</div></div>
    </div>

    <!-- Certificates -->
    <div id="certificates" class="card">
      <div class="section-title">Certificates</div>
      <div class="certificate-gallery">
        <img src="certificate1.jpg" alt="Front End Web Development Certificate">
        <img src="certificate2.jpg" alt="Web Development Fundamentals Certificate">
      </div>
    </div>

    <footer style="text-align:center;color:var(--muted);margin-top:40px;">
      © Hariharan S • Futuristic Tech Portfolio
    </footer>
  </div>

  <script>
    function showSection(id, event){
      const sections = ['home','about','education','skills','projects','contact','certificates'];
      sections.forEach(sec => document.getElementById(sec).style.display = (sec === id) ? 'block' : 'none');
      document.querySelectorAll('nav a').forEach(a => a.classList.remove('active'));
      if(event) event.target.classList.add('active');
    }
  </script>
</body>
</html>
