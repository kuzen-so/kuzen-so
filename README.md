### Hi there 👋

<span > <img src="https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" /> <img src="https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3" /> <img src="https://img.shields.io/badge/-JavaScript-oringe?style=flat-square&logo=javascript" /> </span>


<div align="center"> <img src="https://github-readme-streak-stats.herokuapp.com/?user=sun0225SUN" /> </div>

name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v2.3.4

      - name: Generate Snake
        uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          gif_out_path: ./assets/github-contribution-grid-snake.gif
          svg_out_path: ./assets/github-contribution-grid-snake.svg

      - name: Push to GitHub
        uses: EndBug/add-and-commit@v7.2.1
        with:
          branch: main
          message: 'Generate Contribution Snake'      

<!--
**chumen-Lu/chumen-Lu** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
