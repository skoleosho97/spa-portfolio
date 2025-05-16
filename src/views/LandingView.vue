<script setup lang="ts">
import TwitterIcon from '../components/icons/IconTwitter.vue'
import DiscordIcon from '../components/icons/IconDiscord.vue'
import GithubIcon from '../components/icons/IconGithub.vue'
import JavascriptIcon from '../components/icons/IconJavascript.vue'
import TypescriptIcon from '../components/icons/IconTypescript.vue'
import NodeIcon from '../components/icons/IconNode.vue'
import VueIcon from '../components/icons/IconVue.vue'
import SunIcon from '@/components/icons/IconSun.vue'
import MoonIcon from '@/components/icons/IconMoon.vue'
import { ref } from 'vue'

const dark = ref(true)

const darkToggle = () => {
  const element = document.querySelector('main')
  element?.classList.toggle('dark')

  dark.value = !dark.value
}
</script>

<template>
  <main>
    <div id="nav">
      <div class="nav-logos-wrap">
        <a class="nav-logo" href="https://x.com/SolitudeRain_" target="_blank">
          <TwitterIcon />
        </a>
        <a class="nav-logo" href="https://discordapp.com/users/113686209955364867" target="_blank">
          <DiscordIcon />
        </a>
        <a class="nav-logo" href="https://github.com/skoleosho97" target="_blank">
          <GithubIcon />
        </a>
      </div>
      <div class="nav-links-wrap">
        <div class="nav-link">
          <a href="#about-me">About Me</a>
        </div>
        <div class="nav-link">
          <a href="#projects">Projects</a>
        </div>
        <div class="nav-link">
          <button @click="darkToggle">
            <MoonIcon v-if="dark" />
            <SunIcon v-else />
          </button>
        </div>
      </div>
    </div>
    <div id="welcome">
      <div id="code-box">
        <div class="line">
          <p class="line-col">1</p>
          <p><span>public class</span> Introduction</p>
        </div>
        <div class="line">
          <p class="line-col">2</p>
          <p>&#123;</p>
        </div>
        <div class="line">
          <p class="line-col">3</p>
          <p>&emsp;<span>public</span> string fullName = <span>"Samson Koleosho"</span></p>
        </div>
        <div class="line">
          <p class="line-col">4</p>
          <p>&emsp;// Also goes by Sammy or Sam, or "seaz_n" (season).</p>
        </div>
        <div class="line">
          <p class="line-col">5</p>
          <p>&emsp;<span>public</span> int age = 27</p>
        </div>
        <div class="line">
          <p class="line-col">6</p>
          <p>&emsp;<span>public</span> string occupation = <span>"Software Engineer"</span></p>
        </div>
        <div class="line">
          <p class="line-col">7</p>
          <p>&#125;</p>
        </div>
      </div>
    </div>
    <div id="about-me">
      <h1>&#47;&#47; About Me</h1>
      <div class="container">
        <div class="info">
          <p>
            Hello! My name is Sam, and I am a developer with a preference of making websites and
            small applications. When I am not staring at Visual Studio Code I spend my free time
            watching or participating in sports or playing fighting games. Feel free to contact me
            anytime!
          </p>
        </div>
        <div class="icons">
          <div class="icon">
            <JavascriptIcon />
          </div>
          <div class="icon">
            <TypescriptIcon />
          </div>
          <div class="icon">
            <NodeIcon />
          </div>
          <div class="icon">
            <VueIcon />
          </div>
        </div>
      </div>
    </div>
    <div id="projects">
      <h1>&#47;&#47; Portfolio</h1>
      <div class="projects-wrap">
        <div class="project">
          <div class="tools">
            <div class="tool">Vue</div>
            <div class="tool">TypeScript</div>
            <div class="tool">HTML</div>
            <div class="tool">CSS</div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="css" scoped>
main {
  height: 100vh;
  background: #eeeeee;
  color: #0e0e0e;
  display: flex;
  flex-direction: column;
  overflow: auto;
  transition:
    background 0.4s ease,
    color 0.4s ease;
}

main a {
  color: #0e0e0e;
}

main svg {
  fill: #dd6e00;
  stroke: #dd6e00;
}

button {
  background: none;
  border: none;
  cursor: pointer;
}

svg {
  height: 25px;
}

#nav {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #d1d1d1;
  padding: 10px 300px;
}

.nav-logos-wrap,
.nav-links-wrap {
  height: 25px;
  display: flex;
  justify-content: space-between;
}

.nav-logos-wrap {
  width: 150px;
}

.nav-links-wrap {
  width: 200px;
}

.nav-logo svg:hover {
  opacity: 0.75;
  transition: 0.4s;
}

.nav-link a {
  text-decoration: none;
  font-weight: 500;
}

.container {
  display: flex;
}

#welcome {
  position: relative;
  height: 100%;
  display: flex;
  flex-direction: column;
  flex-shrink: 0;
  padding: 0 300px;
}

#code-box {
  width: 750px;
  font-size: 24px;
  font-weight: 500;
  margin: auto auto;
}

.line {
  display: flex;
  align-items: center;
}

.line span,
h1 {
  color: #dd6e00;
}

.line-col {
  padding: 0 30px;
}

#about-me,
#projects {
  display: flex;
  flex-direction: column;
  margin-bottom: 50px;
  padding: 0 300px;
}

.container {
  height: 200px;
  display: flex;
  align-items: center;
}

.info {
  width: 550px;
}

.icons {
  width: 100%;
  display: flex;
  justify-content: space-evenly;
}

.icon {
  width: 40px;
  height: 40px;
}

.icon svg {
  filter: grayscale(0.9);
}

.icon svg:hover {
  filter: grayscale(0);
  transition: 0.6s;
}

.project {
  width: 200px;
  background: #e6e6e6;
  padding: 5px;
}

.project .tools {
  display: flex;
}

.project .tools .tool {
  background: red;
  font-size: 12px;
  font-weight: 500;
}

.dark {
  background: #0e0e0e;
  color: #eeeeee;
}

.dark a {
  color: #eeeeee;
}

.dark svg {
  fill: #dd6e00;
  stroke: #dd6e00;
}
</style>
