<script setup lang="ts">
import TwitterIcon from '../components/icons/IconTwitter.vue'
import DiscordIcon from '../components/icons/IconDiscord.vue'
import GithubIcon from '../components/icons/IconGithub.vue'
import JavascriptIcon from '../components/icons/IconJavascript.vue'
import TypescriptIcon from '../components/icons/IconTypescript.vue'
import NodeIcon from '../components/icons/IconNode.vue'
import VueIcon from '../components/icons/IconVue.vue'
</script>

<template>
  <main>
    <div id="nav">
      <div class="nav-wrap">
        <div class="nav-logo">
          <a href="https://x.com/SolitudeRain_" target="_blank">
            <TwitterIcon />
          </a>
        </div>
        <div class="nav-logo">
          <a href="https://discordapp.com/users/113686209955364867" target="_blank">
            <DiscordIcon />
          </a>
        </div>
        <div class="nav-logo">
          <a href="https://github.com/skoleosho97" target="_blank">
            <GithubIcon />
          </a>
        </div>
      </div>
      <div class="nav-wrap">
        <div class="nav-link">
          <a href="#about-me">About Me</a>
        </div>
        <div class="nav-link">
          <a href="#projects">Projects</a>
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
    </div>
  </main>
</template>

<style lang="css" scoped>
main {
  height: 100vh;
  display: flex;
  flex-direction: column;
  overflow: auto;
  background: #eeeeee;
  color: #0e0e0e;
}

#nav {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #d1d1d1;
  padding: 10px 300px;
}

.nav-wrap {
  height: 25px;
  width: 150px;
  display: flex;
  justify-content: space-between;
}

.nav-logo {
  width: 25px;
  height: 25px;
}

.nav-logo a {
  width: 100%;
  height: 100%;
}

.nav-logo a:hover {
  opacity: 0.75;
  transition: 0.4s;
}

.nav-link a {
  text-decoration: none;
  font-weight: 500;
  color: #0e0e0e;
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
  padding: 0 300px;
}

#about-me {
  display: flex;
  flex-direction: column;
  margin-bottom: 50px;
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
</style>
