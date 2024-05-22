<template>
  <div id="app">
    <transition name="menu-transition">
      <Menu v-if="showMenu" class="menu-bar" @close="showMenu = false" />
    </transition>
    <transition name="hidden-div-transition">
      <div v-if="showMenu" class="hidden-div" @click="showMenu = false"></div>
    </transition>
    <svg
      version="1.1"
      id="Layer_1"
      x="0px"
      y="0px"
      viewBox="0 0 400 400"
      style="enable-background: new 0 0 400 400"
      xml:space="preserve"
      class="logo"
      @click="scrollToTop"
    >
      <g>
        <path
          class="st0"
          d="M 233.00,0.21
           C 233.00,0.21 271.00,0.21 271.00,0.21
             298.00,0.04 334.24,10.04 359.00,20.72
             386.09,32.40 413.13,50.14 434.00,71.00
             434.00,71.00 447.83,85.00 447.83,85.00
             468.70,108.11 486.23,137.76 496.95,167.00
             504.46,187.49 511.97,219.25 512.00,241.00
             512.00,241.00 512.00,273.00 512.00,273.00
             511.81,288.89 506.82,312.58 502.42,328.00
             484.65,390.30 442.05,445.03 386.00,477.58
             356.13,494.92 324.24,505.83 290.00,510.28
             290.00,510.28 271.00,512.00 271.00,512.00
             271.00,512.00 239.00,512.00 239.00,512.00
             219.85,511.77 191.28,505.10 173.00,499.00
             149.08,491.02 126.51,479.23 106.00,464.57
             52.27,426.17 15.13,366.90 3.42,302.00
             -0.51,280.18 -0.25,260.99 0.00,239.00
             0.25,217.99 7.79,186.80 15.05,167.00
             40.79,96.81 96.19,41.76 166.00,15.42
             181.81,9.46 200.26,4.66 217.00,2.28
             217.00,2.28 233.00,0.21 233.00,0.21 Z
           M 239.00,22.14
           C 216.79,25.48 200.77,26.95 179.00,34.69
             114.46,57.66 63.96,105.22 38.45,169.00
             3.47,256.44 24.62,356.29 91.17,422.83
             114.29,445.95 143.48,463.90 174.00,475.42
             193.24,482.69 223.48,489.76 244.00,490.00
             244.00,490.00 266.00,490.00 266.00,490.00
             297.60,489.95 333.93,478.79 362.00,464.75
             389.28,451.11 405.66,437.59 427.00,416.00
             441.67,401.15 455.89,379.71 465.25,361.00
             512.21,267.08 491.09,152.79 413.00,82.17
             387.70,59.29 358.38,43.03 326.00,32.66
             302.22,25.04 279.89,22.00 255.00,22.14
             255.00,22.14 239.00,22.14 239.00,22.14 Z
           M 163.00,144.00
           C 163.00,144.00 260.00,144.00 260.00,144.00
             270.27,144.02 280.31,146.41 290.00,149.67
             333.09,164.17 361.93,206.86 362.00,252.00
             362.04,280.85 355.78,307.42 336.71,330.00
             318.14,351.98 289.29,367.95 260.00,368.00
             260.00,368.00 226.00,368.00 226.00,368.00
             226.00,368.00 163.00,368.00 163.00,368.00
             163.00,368.00 163.00,144.00 163.00,144.00 Z
           M 215.00,318.00
           C 215.00,318.00 240.00,318.00 240.00,318.00
             255.67,318.00 268.67,319.05 283.00,310.96
             319.44,290.38 322.18,228.28 288.00,204.21
             272.57,193.34 259.76,194.00 242.00,194.00
             242.00,194.00 215.00,194.00 215.00,194.00
             215.00,194.00 215.00,318.00 215.00,318.00 Z"
        />
      </g>
    </svg>
    <svg
      version="1.1"
      id="Layer_1"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      x="0px"
      y="0px"
      viewBox="0 0 24 24"
      style="enable-background: new 0 0 24 24"
      xml:space="preserve"
      class="menu"
      @click="showMenu = true"
    >
      <path class="st1" d="M0,0h24v24H0V0z" />
      <path
        class="st2"
        d="M3,18h18v-2H3V18z M3,13h18v-2H3V13z M3,6v2h18V6H3z"
      />
    </svg>
    <Home id="home" class="section" />
    <Me id="me" class="section" />
    <Work id="work" />
    <FindMe id="find-me" />
    <div class="ocean">
      <div class="wave"></div>
    </div>
  </div>
</template>

<script>
import Home from "./views/Home";
import Menu from "./components/Menu";
import Me from "./views/Me";
import Work from "./views/Work";
import FindMe from "./views/FindMe";

export default {
  name: 'App',
  components: {
    Home, Menu, Me, FindMe, Work
  },
  data() {
    return {
      showMenu: false,
      previewImageUrl: "",
      previewImageTitle: "",
    };
  },
  methods: {
    scrollToTop() {
      document.getElementById("app").scrollIntoView({ behavior: "smooth" });
    },
  },
  metaInfo: {
    title: "Duarte - Portfolio",
    meta: [
      {
        name: "theme-color",
        content: "#59ff9c",
      },
      {
        name: "description",
        content: "Portfolio website of Duarte Vital",
      },
    ],
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&family=Source+Sans+Pro:wght@400;600;700&display=swap");
* {
  box-sizing: border-box;
  font-family: "Roboto", sans-serif;
}
:root {
  --primary-color: #59ff9c;
  --blue-accent-color: #11299d;
}
::selection {
  color: black;
  background-color: var(--primary-color);
}
body {
  margin: 0;
  padding: 0;
  background-color: #1c1c1c;
  color: white;
  position: relative;
  overflow-x: hidden;
  scroll-behavior: smooth;
}
.logo,
.menu {
  z-index: 1;
  margin: 2em;
  width: 30px;
  cursor: pointer;
  position: fixed;
}
.logo {
  top: 0;
  left: 0;
}
.image-preview {
  max-height: 95%;
  max-width: 95%;
  border-radius: 40px;
}
.image-preview-container {
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.8);
  backdrop-filter: blur(4px);
  z-index: 100;
}
.image-preview-transititon-enter-active,
.image-preview-transiiton-leave-active {
  transition: all 0.3s ease;
}
.image-preview-transititon-enter,
.image-preview-transititon-leave-to {
  opacity: 0;
}
.menu {
  top: 0;
  right: 0;
}
.nav {
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding: 2em;
  position: fixed;
}
.menu-bar {
  z-index: 10;
  position: fixed;
  right: 0;
  top: 0;
  height: 100vh;
}
.hidden-div {
  backdrop-filter: blur(3px);
  z-index: 5;
  position: fixed;
  width: 100%;
  left: 0;
  top: 0;
  height: 100vh;
}
.menu-transition-enter-active,
.menu-transition-leave-active {
  transition: all 0.3s ease-out;
}
.menu-transition-enter,
.menu-transition-leave-to {
  transform: translateX(80vw);
}
h1 {
  font-size: 72px;
}
.hidden-div-transition-active,
.hidden-div-transition-leave-active {
  transition: all 0.3s ease;
}
.hidden-div-transition-enter,
.hidden-div-transition-leave-to {
  opacity: 0;
}

.section {
  height: 100vh;
  width: 100%;
}

.ocean {
  height: 100px;
  width: 100%;
  position: absolute;
  left: 0;
}

.wave {
  background: url("./assets/pattern/wave.svg") repeat-x;
  position: absolute;
  bottom: 0;
  width: 6400px;
  height: 198px;
  opacity: 0.5;
  animation: wave 30s cubic-bezier(0.36, 0.45, 0.63, 0.53) infinite;
  transform: translate3d(0, 0, 0);
}

@keyframes wave {
  0% {
    margin-left: 0;
  }
  100% {
    margin-left: -1600px;
  }
}

.st0 {
  fill: #ffffff;
  transition: 0.4s ease-in;
}

.logo:hover .st0 {
  fill: var(--primary-color);
}
.st1 {
  fill: none;
}
.st2 {
  transition: 0.4s ease-in;
  fill: #ffffff;
}

.menu:hover .st2 {
  fill: var(--primary-color);
}

@media (max-width: 700px) {
  .section {
    height: 100%;
  }
  .ocean,
  .wave {
    display: none;
  }
}
</style>