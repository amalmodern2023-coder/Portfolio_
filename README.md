<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Amal Ahmad Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- React + Babel -->
  <script src="https://unpkg.com/react@18/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:Arial,sans-serif;}
    body{background:#ffe4ec;color:#000;scroll-behavior:smooth;}
    nav{position:fixed;top:0;width:100%;background:#ffb6c1;display:flex;justify-content:space-between;align-items:center;padding:15px 40px;z-index:1000;}
    nav h2{font-size:22px;}
    nav ul{display:flex;list-style:none;gap:20px;}
    nav ul li a{text-decoration:none;color:#000;font-size:15px;font-weight:bold;white-space:nowrap;}
    nav ul li a.active{border-bottom:2px solid #ff1493;}
    section{padding:100px 40px;min-height:100vh;}
    h1,h2{text-align:center;margin-bottom:20px;}
    #home{display:flex;flex-direction:column;justify-content:center;align-items:center;animation:fade 1.2s ease;}
    #home h1{font-size:32px;}
    #home p{margin-top:10px;font-size:18px;text-align:center;max-width:600px;}
    .btn{display:inline-block;margin-top:20px;padding:10px 18px;background:#ff69b4;color:#fff;text-decoration:none;border-radius:8px;transition:0.3s;}
    .btn:hover{background:#ff1493;}
    .projects-container{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:25px;margin-top:40px;}
    .project-card{padding:25px;border-radius:18px;text-align:center;transition:.4s ease;animation:fadeUp 1s ease;}
    .project-card:hover{transform:translateY(-10px) scale(1.03);box-shadow:0 15px 30px rgba(0,0,0,0.2);}
    .project-icon{font-size:40px;margin-bottom:12px;}
    .project-links{margin-top:15px;display:flex;justify-content:center;gap:18px;}
    .project-links a{font-size:22px;color:#000;transition:.3s ease;}
    .project-links a:hover{color:#ff1493;transform:scale(1.2);}
    /* Project Colors */
    .todo{background:#ffd6e8;}
    .password{background:#ffe9c6;}
    .coffee{background:#e6d4c3;}
    .food{background:#ffdede;}
    .music-player{background:#a0d2ff;}
    .skills-container{display:grid;grid-template-columns:repeat(auto-fit,minmax(100px,1fr));gap:20px;justify-items:center;margin-top:40px;}
    .skill{display:flex;flex-direction:column;align-items:center;font-size:16px;color:#000;transition:.3s;}
    .skill i{font-size:30px;margin-bottom:8px;color:#ff69b4;}
    .skill:hover{transform:scale(1.1);}
    .contact-box{text-align:center;margin-top:30px;animation:fadeUp 1s ease;}
    .contact-box a{display:inline-block;margin:10px;font-size:28px;color:#000;transition:0.3s;}
    .contact-box a:hover{color:#ff1493;transform:scale(1.2);}
    @keyframes fadeUp{from{opacity:0;transform:translateY(30px);}to{opacity:1;transform:translateY(0);}}
    @keyframes fade{from{opacity:0;}to{opacity:1;}}
    @media(max-width:600px){nav ul{gap:12px;} nav ul li a{font-size:13px;}}
  </style>
</head>
<body>
  <nav>
    <h2> Amal Ahmad </h2>
    <ul id="navbar">
      <li><a href="#home" class="nav-link active">Home</a></li>
      <li><a href="#projects" class="nav-link">Projects</a></li>
      <li><a href="#skills" class="nav-link">Skills</a></li>
      <li><a href="#contact" class="nav-link">Contact Me</a></li>
    </ul>
  </nav>

  <section id="home">
    <h1>Front-End Developer</h1>
    <p>2+ Years Experience Building Interactive Web Projects</p>
    <a href="https://1drv.ms/w/c/f3d5176858fdf593/IQBXlpuK1Z-qSaqu3pnj6IgcAVt4bP8Cl0p82Fmsliv6j48?e=lbp37Q" class="btn" target="_blank">Download CV</a>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <div id="root" class="projects-container"></div>
  </section>

  <section id="skills">
    <h2>Skills</h2>
    <div class="skills-container">
      <div class="skill"><i class="fa-brands fa-html5"></i>HTML</div>
      <div class="skill"><i class="fa-brands fa-css3-alt"></i>CSS</div>
      <div class="skill"><i class="fa-brands fa-js"></i>JavaScript</div>
      <div class="skill"><i class="fa-brands fa-bootstrap"></i>Bootstrap</div>
      <div class="skill"><i class="fa-brands fa-react"></i>React</div>
      <div class="skill"><i class="fa-brands fa-github"></i>GitHub</div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <div class="contact-box">
      <a href="mailto:amal@email.com"><i class="fa-solid fa-envelope"></i></a>
      <a href="https://github.com/amalmodern2023-coder" target="_blank"><i class="fa-brands fa-github"></i></a>
    </div>
  </section>

  <script type="text/babel">
    const projects = [
      {name:"To Do List App",desc:"Task management app using JavaScript",icon:"fa-solid fa-list-check",color:"todo",codepen:"https://codepen.io/Amalmodern2023-coder/pen/RNRMrqp",github:"https://github.com/amalmodern2023-coder/To-list-App-/commit/305acdaa764ccfd94a36b0e8da615e86ebf02ce2"},
      {name:"Password Strength",desc:"Real-time password validation",icon:"fa-solid fa-lock",color:"password",codepen:"https://codepen.io/Amal-Ahmad-the-scripter/pen/xbOWepN",github:"https://github.com/amalmodern2023-coder/Password-strength-/commit/55e2b54039ec9abc1546f622ea13f2f02d26621d"},
      {name:"Responsive Coffee",desc:"Bootstrap responsive website",icon:"fa-solid fa-mug-hot",color:"coffee",codepen:"https://codepen.io/Amalmodern2023-coder/pen/bNeVPOz",github:"https://github.com/amalmodern2023-coder"},
      {name:"Food Website",desc:"Modern food landing page",icon:"fa-solid fa-burger",color:"food",codepen:"https://codepen.io/Amal-Ahmad-the-scripter/pen/azZERKV",github:"https://github.com/amalmodern2023-coder"},
      {name:"Advanced Music Player",desc:"Interactive music player with playlist, visualizer & dark mode",icon:"fa-solid fa-music",color:"music-player",codepen:"https://codepen.io/Amalmodern2023-coder/pen/RNRYJBW",github:"https://github.com/amalmodern2023-coder"}
    ];

    const ProjectGrid = () => (
      <>
        {projects.map((proj,i)=>(
          <div key={i} className={`project-card ${proj.color}`}>
            <i className={`${proj.icon} project-icon`}></i>
            <h3>{proj.name}</h3>
            <p>{proj.desc}</p>
            <div className="project-links">
              <a href={proj.codepen} target="_blank"><i className="fa-brands fa-codepen"></i></a>
              <a href={proj.github} target="_blank"><i className="fa-brands fa-github"></i></a>
            </div>
          </div>
        ))}
      </>
    );

    ReactDOM.createRoot(document.getElementById("root")).render(<ProjectGrid />);

    // Navbar active link
    const sections = document.querySelectorAll("section");
    const navLinks = document.querySelectorAll(".nav-link");
    window.addEventListener("scroll",()=>{
      let current="";
      sections.forEach(sec=>{if(window.scrollY >= sec.offsetTop - 150) current=sec.id;});
      navLinks.forEach(a=>{a.classList.remove("active");if(a.getAttribute("href")==="#"+current)a.classList.add("active");});
    });
  </script>
</body>
</html>
