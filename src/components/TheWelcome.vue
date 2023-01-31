<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Japanese - English Study Web App (Software Development)</template>
    An app for English speakers to study Japanese<br>
    <span style="font-weight: 700">Frontend:</span> Vue.js, JavaScript, HTML, CSS, Vite<br>
    <span style="font-weight: 700">Backend:</span> Python, FastAPI<br>
    Link coming soon
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Space Game (Software Development)</template>
    An open-world 3D first-person game in space<br>
    <span style="font-weight: 700">Coding:</span> C#<br>
    <span style="font-weight: 700">Tools Used:</span> Unity, Blender<br>
    <a href="https://play.unity.com/mg/other/webgl-builds-238852" target="_blank">Check it out</a>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Movie Recommendations (Software Development)</template>
    Web app that uses machine learning (AI) to recommend movies similar to a movie input by the user<br>
    <span style="font-weight: 700">Frontend:</span> React, JavaScript, HTML, CSS<br>
    <span style="font-weight: 700">Backend:</span> Python, Flask<br>
    <span style="font-weight: 700">Other Tools Used:</span> scikit-learn, NLTK, NumPy, Pandas, WayScript<br>
    <a href="https://daringly-nifty-panda-domain.wayscript.cloud/" target="_blank">Go To Movie Recommendations</a>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Event Horizon (Business & Software Development)</template>
    Development of event hosting web / mobile apps and business strategy<br>
    <span style="font-weight: 700">Frontend:</span> Vue.js, JavaScript, HTML, CSS<br>
    <span style="font-weight: 700">Backend:</span> Python, Django REST, SQLite, PostgreSQL, Node.js<br>
    <span style="font-weight: 700">Other Tools Used:</span> AWS, Google Cloud<br>
    Link coming soon
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>XMS (Software Development)</template>
    Aerodynamics simulation software for propeller design and analysis including automatic propeller design and optimization, blade strength analysis, contra-rotating propeller systems, ducted propeller systems, and utilization in hovering, angled flight, ascent, descent, etc.<br>
    <span style="font-weight: 700">Coding:</span> Python<br>
    <span style="font-weight: 700">Methodologies Used:</span> Machine learning, data analysis, optimization, BEM, FEM<br>
    <span style="font-weight: 700">Other Tools Used:</span> X-Foil, Subprocess, Matplotlib, NumPy<br>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Original Music (Not Software)</template>
    Writing and creating original music - ongoing. Mainly guitar and singing, including some ukulele, piano, and electronic music production with Ableton LIVE<br>
    <a href="https://soundcloud.com/mikey-s-music" target="_blank">Mostly Completed Work ⇨ SoundCloud</a><br>
    <a href="https://www.youtube.com/playlist?list=PLvIq75Y7oDPsfqUzv-WdztMCJ67MGPtFl" target="_blank">Works In Progress ⇨ YouTube</a>
  </WelcomeItem>
</template>
