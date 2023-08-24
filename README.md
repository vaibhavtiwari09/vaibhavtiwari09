<h2 align="left">Greetings! I'm Vaibhav Tiwari, a Java enthusiast and Frontend Developer.<br>-- I'm committed to honing my skills and making a mark in the tech world.<br>-- I'm skilled in Java, JavaScript, HTML, CSS, and MySQL, with a knack for UI/UX design using Adobe XD and Figma.</h2>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=vaibhavtiwari09&hide_title=false&hide_rank=true&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=true&custom_title=Stats" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=vaibhavtiwari09&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=6&theme=dracula&hide_border=true" height="150" alt="languages graph"  />
</div>

###

<img align="right" height="150" src="https://img.freepik.com/free-photo/view-3d-male-teacher_23-2150710024.jpg?t=st=1692912087~exp=1692915687~hmac=3adf23dad362dd15b12ef8bd989800d753a566e5f3acc67d713e49ebb40d2dbc&w=740"  />

###

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="29" alt="javascript logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="29" alt="react logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="29" alt="html5 logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="29" alt="css3 logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/behance/behance-original.svg" height="29" alt="behance logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" height="29" alt="figma logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="29" alt="java logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" height="29" alt="linkedin logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="29" alt="mysql logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/xd/xd-plain.svg" height="29" alt="xd logo"  />
  <img width="23" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="29" alt="vscode logo"  />
</div>

###

<div align="center">
  <a href="https://www.linkedin.com/in/vaibhav-tiwari-b81391209/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=flat" height="35" alt="linkedin logo"  />
  </a>
  <a href="https://www.behance.net/vaibhavtiwari12" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Behance&logo=behance&label=&color=1769ff&logoColor=white&labelColor=&style=flat" height="35" alt="behance logo"  />
  </a>
  <a href="https://t.me/Vaibhav0902" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Telegram&logo=telegram&label=&color=2CA5E0&logoColor=white&labelColor=&style=flat" height="35" alt="telegram logo"  />
  </a>
  <a href="mailto:vaibhavtiwarisatna2004@gmail.com" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=flat" height="35" alt="gmail logo"  />
  </a>
</div>

###

<img src="https://raw.githubusercontent.com/vaibhavtiwari09/vaibhavtiwari09/output/snake.svg" alt="Snake animation" />
name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v2
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v2.6.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
###
