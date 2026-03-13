<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Amal Ahmad Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

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

    #home{
      display:flex; flex-direction:column; justify-content:center; align-items:center; min-height:100vh;
      color:#fff; text-align:center; animation:fade 1.2s ease;
      background: url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
      position:relative;
    }
    #home::before{
      content:""; position:absolute; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.4); z-index:0;
    }
    #home h1, #home p, #home .btn{position:relative; z-index:1;}
    #home h1{font-size:36px;}
    #home p{margin-top:10px;font-size:18px;max-width:600px;}
    .btn{display:inline-block;margin-top:20px;padding:10px 18px;background:#ff69b4;color:#fff;text-decoration:none;border-radius:8px;transition:0.3s;}
    .btn:hover{background:#ff1493;}

    .projects-container{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:25px;margin-top:40px;}
    .project-card{position:relative;border-radius:18px;overflow:hidden;cursor:pointer;transition: transform 0.3s, box-shadow 0.3s, opacity 0.5s;opacity:0;transform: translateX(50px);}
    .project-card.show{opacity:1; transform:translateX(0);}
    .project-card:hover{transform:scale(1.03); box-shadow:0 15px 30px rgba(0,0,0,0.25);}
    .project-img{width:100%; display:block; border-radius:15px; object-fit:cover; transition: transform 0.4s ease;}
    .project-card:hover .project-img{transform: scale(1.05);}
    .overlay{position:absolute; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.35); color:#fff; display:flex; flex-direction:column; justify-content:center; align-items:center; opacity:0; transition:0.3s ease; padding:15px;}
    .project-card:hover .overlay{opacity:1;}
    .overlay h4{margin-bottom:10px; font-size:18px;}
    .overlay p{font-size:14px; text-align:center; margin-bottom:12px;}
    .overlay a{color:#fff; margin:5px; font-size:20px; transition:0.3s;}
    .overlay a:hover{color:#ff1493; transform:scale(1.2);}

    .skills-container{display:grid;grid-template-columns:repeat(auto-fit,minmax(100px,1fr));gap:20px;justify-items:center;margin-top:40px;}
    .skill{display:flex;flex-direction:column;align-items:center;font-size:16px;color:#000;transition:.3s;}
    .skill i{font-size:30px;margin-bottom:8px;color:#ff69b4;transition: transform 0.4s ease;}
    .skill:hover{transform:scale(1.1) rotate(5deg);}

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
    <div class="projects-container" id="projects-container"></div>
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
      <a href="https://wa.me/201142546944" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
      <a href="https://linkedin.com/in/amal-ahmad-96a092355" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
    </div>
  </section>

  <script>
    const projects = [
      {name:"To Do List App",desc:"Task management app using JavaScript",img:"https://i.postimg.cc/L6n7VdrX/Screenshot-20260306-005353-Chrome.jpg",codepen:"https://codepen.io/Amalmodern2023-coder/pen/RNRMrqp",github:"https://github.com/amalmodern2023-coder/To-list-App-"},
      {name:"Responsive Coffee Website",desc:"Bootstrap responsive website",img:"https://i.ibb.co/ynSXYWXk/Screenshot-20260306-025651-Chrome.jpg",codepen:"https://codepen.io/Amalmodern2023-coder/pen/bNeVPOz",github:"https://github.com/amalmodern2023-coder"},
      {name:"Food Website",desc:"Modern food landing page",img:"https://i.postimg.cc/gkVMsYN5/Screenshot-20260306-005403-Chrome.jpg",codepen:"https://codepen.io/Amal-Ahmad-the-scripter/pen/azZERKV",github:"https://github.com/amalmodern2023-coder"},
      {name:"Music Player",desc:"Real-time password validation",img:"https://i.ibb.co/ycGNHxVr/Screenshot-20260306-024154-Chrome.jpg",codepen:"https://codepen.io/Amalmodern2023-coder/pen/RNRYJBW",github:"https://github.com/amalmodern2023-coder/Password-strength-/commit/55e2b54039ec9abc1546f622ea13f2f02d26621d"},
      {name:"Password Strength",desc:"Real-time password ",img:"https://i.ibb.co/6RkLDcPR/Screenshot-20260306-024148-Chrome.jpg",codepen:"https://codepen.io/Amal-Ahmad-the-scripter/pen/xbOWepN",github:"https://github.com/amalmodern2023-coder/Password-strength-/commit/55e2b54039ec9abc1546f622ea13f2d26621d"},
      {name:"E-Commerce Website",desc:"Online shop layout with interactive UI",img:"https://i.ibb.co/208Hwmjx/Screenshot-20260306-024115-Chrome.jpg",codepen:"https://codepen.io/Amalmodern2023-coder/pen/RNRXXLY",github:"https://github.com/amalmodern2023-coder/E-Commerce-/commit/3b00ab16312af8bc5943eddcb298fff74e382fda"}
    ];

    const container = document.getElementById('projects-container');

    projects.forEach(proj => {
      const card = document.createElement('div');
      card.className = 'project-card';

      const img = document.createElement('img');
      img.src = proj.img;
      img.alt = proj.name;
      img.className = 'project-img';
      card.appendChild(img);

      const overlay = document.createElement('div');
      overlay.className = 'overlay';

      const title = document.createElement('h4');
      title.textContent = proj.name;
      overlay.appendChild(title);

      const desc = document.createElement('p');
      desc.textContent = proj.desc;
      overlay.appendChild(desc);

      const codepenLink = document.createElement('a');
      codepenLink.href = proj.codepen;
      codepenLink.target = '_blank';
      codepenLink.innerHTML = '<i class="fa-brands fa-codepen"></i>';
      overlay.appendChild(codepenLink);

      const githubLink = document.createElement('a');
      githubLink.href = proj.github;
      githubLink.target = '_blank';
      githubLink.innerHTML = '<i class="fa-brands fa-github"></i>';
      overlay.appendChild(githubLink);

      card.appendChild(overlay);
      container.appendChild(card);
    });

    // Navbar active link
    const sections = document.querySelectorAll("section");
    const navLinks = document.querySelectorAll(".nav-link");
    window.addEventListener("scroll",()=>{
      let current="";
      sections.forEach(sec=>{if(window.scrollY >= sec.offsetTop - 150) current=sec.id;});
      navLinks.forEach(a=>{a.classList.remove("active");if(a.getAttribute("href")==="#"+current)a.classList.add("active");});
    });

    // Intersection Observer for cards animation
    const cards = document.querySelectorAll('.project-card');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('show');
        }
      });
    },{ threshold: 0.3 });
    cards.forEach(card => observer.observe(card));
  </script>

</body>
</html> 
