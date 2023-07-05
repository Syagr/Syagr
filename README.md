### Hi there, I'm Pasha 👋

### 💻 &nbsp;About Me

🤓 I love programming and creating new things 
🕶 A full-time programmer at heart 
🙌 A young student from Kiev with a big dream 


### ⌨️  &nbsp;Tech Stack

![Visual Studio Code](https://img.shields.io/badge/-Visual%20Studio%20Code-05122A?style=flat&logo=visual-studio-code&logoColor=007ACC)&nbsp;
![HTML](https://img.shields.io/badge/-HTML-05122A?style=flat&logo=HTML5)&nbsp;
![CSS](https://img.shields.io/badge/-CSS-05122A?style=flat&logo=CSS3&logoColor=1572B6)&nbsp;
![JavaScript](https://img.shields.io/badge/-JavaScript-05122A?style=flat&logo=javascript)&nbsp;
![Git](https://img.shields.io/badge/-Git-05122A?style=flat&logo=git)&nbsp;
![GitHub](https://img.shields.io/badge/-GitHub-05122A?style=flat&logo=github)&nbsp;
![Python](https://img.shields.io/badge/-Python-05122A?style=flat&logo=python)&nbsp;
![PHP](https://img.shields.io/badge/-PHP-05122A?style=flat&logo=php)&nbsp;

### ☑️ &nbsp;GitHub Analytics

<center>
  <a href="https://github.com/Syagr">
    <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Syagr&show_icons=true&theme=dark&show_icons=true&include_all_commits=true&count_private=true"/>
    <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Syagr&theme=dark&layout=compact&langs_count=8&hide=php"/>
  </a>
</center>

![Metrics](# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: Syagr
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Europe/Kiev)
