<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="color-scheme" content="dark">
<title>Tejas Sri S.M. | Software Engineering Aspirant</title>
<meta name="description" content="Third-year B.Tech IT student building in Java and Python. Projects, problem-solving and contact links.">
<style>
  :root{
    color-scheme: dark;
    --bg:#0b1220; --card:#121b2e; --text:#e6edf7; --muted:#93a1b8;
    --accent:#22d3ee; --border:#1f2c47;
  }
  *{box-sizing:border-box}
  body{margin:0;background:var(--bg);color:var(--text);font:16px/1.6 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
  a{color:var(--accent);text-decoration:none}
  a:hover{text-decoration:underline}
  .wrap{max-width:860px;margin:0 auto;padding:0 20px}
  header{padding:64px 0 32px}
  h1{font-size:clamp(2rem,6vw,3rem);margin:0 0 8px;line-height:1.15}
  .tag{color:var(--muted);font-size:1.1rem;margin:0 0 20px}
  .links{display:flex;flex-wrap:wrap;gap:10px}
  .btn{padding:8px 16px;border:1px solid var(--border);border-radius:999px;background:var(--card);color:var(--text);font-size:.95rem}
  .btn:hover{border-color:var(--accent);text-decoration:none}
  .btn.primary{background:var(--accent);color:#06222a;border-color:var(--accent);font-weight:600}
  section{padding:28px 0}
  h2{font-size:1.3rem;margin:0 0 16px}
  .grid{display:grid;gap:16px;grid-template-columns:repeat(auto-fit,minmax(250px,1fr))}
  .card{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:20px}
  .card h3{margin:0 0 6px;font-size:1.05rem}
  .card p{margin:0 0 10px;color:var(--muted);font-size:.95rem}
  .chips{display:flex;flex-wrap:wrap;gap:6px}
  .chip{font-size:.8rem;padding:2px 10px;border-radius:999px;border:1px solid var(--border);color:var(--muted)}
  .status{font-size:.75rem;color:var(--accent)}
  ul.steps{padding-left:20px;margin:0}
  ul.steps li{margin-bottom:8px}
  footer{padding:32px 0 56px;color:var(--muted);font-size:.9rem;border-top:1px solid var(--border);margin-top:24px}
</style>
</head>
<body>
<div class="wrap">

  <header>
    <h1>Tejas Sri S.M.</h1>
    <p class="tag">Third-year B.Tech IT student · aspiring software engineer · Java &amp; Python</p>
    <div class="links">
      <a class="btn primary" href="https://www.linkedin.com/in/tejas-sri-sm-0b909a444">LinkedIn</a>
      <a class="btn" href="https://github.com/tejassri-sm">GitHub</a>
      <a class="btn" href="https://leetcode.com/u/tejassri_sm/">LeetCode</a>
      <a class="btn" href="https://www.hackerrank.com/profile/tejassri456">HackerRank</a>
      <!-- TODO: <a class="btn" href="resume.pdf">Resume</a> -->
    </div>
  </header>

  <section>
    <h2>About</h2>
    <div class="card">
      <ul class="steps">
        <li><strong>Learn</strong> fundamentals properly: C, Java, Python, OOP, SQL basics.</li>
        <li><strong>Build</strong> small, working programs that solve everyday problems.</li>
        <li><strong>Practise</strong> data structures and algorithms in public on LeetCode and HackerRank.</li>
      </ul>
      <p style="margin:14px 0 0;color:var(--muted)">Currently learning Spring Boot and REST APIs. Looking for software engineering internships and entry-level roles.</p>
    </div>
  </section>

  <section>
    <h2>Projects</h2>
    <div class="grid" id="projects"></div>
  </section>

  <section>
    <h2>Skills</h2>
    <div class="chips" id="skills"></div>
  </section>

  <footer>
    <span id="year"></span> Tejas Sri S.M. · Hosted on GitHub Pages
  </footer>
</div>

<script>
  // Edit these arrays; nothing else needs to change.
  const projects = [
    {
      name: "Weather Forecasting System",
      desc: "Java application that turns weather data into a readable forecast. TODO: add one line on features.",
      tags: ["Java"],
      url: "https://github.com/tejassri-sm/WeatherForecastingSystem",
      status: ""
    },
    {
      name: "Currency Converter",
      desc: "C program for converting between currencies. TODO: add one line on features.",
      tags: ["C"],
      url: "https://github.com/tejassri-sm/CurrencyConverter",
      status: ""
    },
    {
      name: "Expense Splitter",
      desc: "Planned Java + SQL app for splitting shared costs and settling who owes whom.",
      tags: ["Java", "SQL"],
      url: "",
      status: "In progress"
    }
  ];
  const skills = ["Java", "Python", "C", "OOP", "Data Structures", "Algorithms", "SQL / MySQL", "HTML", "CSS", "Git & GitHub", "VS Code"];

  const grid = document.getElementById("projects");
  projects.forEach(p => {
    const card = document.createElement("div");
    card.className = "card";
    const title = p.url ? `<a href="${p.url}">${p.name}</a>` : p.name;
    card.innerHTML =
      `<h3>${title}</h3>` +
      (p.status ? `<div class="status">${p.status}</div>` : "") +
      `<p>${p.desc}</p>` +
      `<div class="chips">${p.tags.map(t => `<span class="chip">${t}</span>`).join("")}</div>`;
    grid.appendChild(card);
  });

  document.getElementById("skills").innerHTML =
    skills.map(s => `<span class="chip">${s}</span>`).join("");
  document.getElementById("year").textContent = "© " + new Date().getFullYear();
</script>
</body>
</html>
