<template>
  <div class="main-page">
    <BrandHeader :currentSection="currentSection" :isHeaderMode="isHeaderMode" />

    <BrandtopBar :sections="sections" :currentSection="currentSection" @change-section="changeSection" />

    <main class="main-content" id="mainContent">
      <BrandSection v-for="section in sections" :key="section.id" :section="section"
        :isActive="currentSection === section.id" />
    </main>


    <ThemeIndicator :isVisible="isIndicatorVisible" :sectionName="currentSectionName" />

    <div class="section-transition"
      :class="{ active: isTransitioning, [`slide-${transitionDirection}`]: transitionDirection }"></div>
  </div>

  <NuxtPage to="/about" />



</template>




<style>
@import url("https://fonts.googleapis.com/css2?family=Lexend+Deca:wght@100..900&family=Lexend:wght@100..900&display=swap");

@font-face {
  font-family: "Transforma";
  src: url("~/fonts/TRANSFORMASANS_TRIAL-SEMIBOLD.woff") format("woff");
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: "TransformaScript";
  src: url("~/fonts/TRANSFORMASCRIPT_TRIAL-SEMIBOLD.woff") format("woff");
  font-weight: normal;
  font-style: normal;
}



* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {

  margin: 0 auto;
  text-align: center;
  width: 100vw;
}

body {
  font-family: "Lexend Deca", sans-serif;
  line-height: 1.6;
  color: #181818;
  background-color: #f8f9fa;
  overflow-x: hidden;
  margin: 0;
  padding: 0;
  transition: background-color 0.4s ease;
}

br {
  margin-top: 2rem;
}

h2 {
  font-size: 2.2rem;
  margin-bottom: 1.5rem;
  color: #54c1dc;
  font-family: "Transforma", Tahoma, Geneva, Verdana, sans-serif;
  transition: color 0.4s ease;
}

h3 {
  font-size: 1.6rem;
  margin: 2rem 0 1rem;
  color: #54c1dc;
  transition: color 0.4s ease;
}

h4 {
  font-weight: 700;
  font-family: "Lexend Deca";
  text-transform: uppercase;
  font-size: 1.05rem;
  color: #181818;
}

p {
  margin-bottom: 1rem;
  display: flex;
}

.script {
  font-family: "TransformaScript";
}

.main-page {
  display: flex;
  flex-direction: column;

  width: 100%;
  min-height: 100vh;
}

.main-content {
  padding: 2rem;
  width: 80%;
  max-width: 1200px;
  margin: 0 auto;
  padding-top: 10b rem;

  min-height: 100vh;


  display: flex;
  top: 25vh;
}

.section-transition {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.1);
  opacity: 0;
  pointer-events: none;
  z-index: 9999;
  transition: opacity 0.3s ease;
}

.section-transition.active {
  opacity: 1;
  animation: sectionTransition 0.5s ease-in-out;
}

.section-transition.slide-left {
  background: linear-gradient(to left, rgba(255, 255, 255, 0.2), transparent);
}

.section-transition.slide-right {
  background: linear-gradient(to right, rgba(255, 255, 255, 0.2), transparent);
}

@keyframes sectionTransition {
  0% {
    opacity: 0;
  }

  50% {
    opacity: 0.1;
  }

  100% {
    opacity: 0;
  }
}

/* Theme styles */
body.theme-Tipografía {
  background-color: #f8f9fa;
  color: #181818;
}

body.theme-Tipografía h2,
body.theme-Tipografía h3 {
  color: #54c1dc;
}

body.theme-Tipografía .header.header-mode {
  background: #181818;
}

body.theme-Tipografía .header.header-mode .header-title {
  color: #54c1dc;
}

body.theme-Tipografía .topBar {
  border-top: 3px solid #54c1dc;
}

body.theme-Tipografía .topBar .nav-item:hover,
body.theme-Tipografía .topBar .nav-item.active {
  color: #54c1dc;
}

body.theme-Tipografía .topBar .nav-item.active:after {
  background-color: #54c1dc;
}

body.theme-Tipografía .font-example {
  border-color: #54c1dc;
}

body.theme-Tipografía .font-example .font-heading {
  color: #54c1dc;
}

body.theme-Tipografía .icon-item {
  border-color: #54c1dc;
}

body.theme-Tipografía .icon-item .icon {
  color: #54c1dc;
}

body.theme-Tipografía .logo-variant .logo-img.primary-logo {
  background-color: #54c1dc;
}

body.theme-Tipografía .logo-variant .logo-img.reversed-logo {
  color: #54c1dc;
}

body.theme-Tipografía .image-example {
  border-color: #54c1dc;
}

body.theme-colors {
  background-color: #fff9f8;
  color: #181818;
}

body.theme-colors h2,
body.theme-colors h3 {
  color: #e94f1e;
}

body.theme-colors .header.header-mode {
  background: #181818;
}

body.theme-colors .header.header-mode .header-title {
  color: #e94f1e;
}

body.theme-colors .topBar {
  border-top: 3px solid #e94f1e;
}

body.theme-colors .topBar .nav-item:hover,
body.theme-colors .topBar .nav-item.active {
  color: #e94f1e;
}

body.theme-colors .topBar .nav-item.active:after {
  background-color: #e94f1e;
}

body.theme-colors .font-example {
  border-color: #e94f1e;
}

body.theme-colors .font-example .font-heading {
  color: #e94f1e;
}

body.theme-colors .icon-item {
  border-color: #e94f1e;
}

body.theme-colors .icon-item .icon {
  color: #e94f1e;
}


body.theme-colors .image-example {
  border-color: #e94f1e;
}

body.theme-icons {
  background-color: #f8fff9;
  color: #181818;
}

body.theme-icons h2,
body.theme-icons h3 {
  color: #2eaa53;
}

body.theme-icons .header.header-mode {
  background: #181818;
}

body.theme-icons .header.header-mode .header-title {
  color: #2eaa53;
}

body.theme-icons .topBar {
  border-top: 3px solid #2eaa53;
}

body.theme-icons .topBar .nav-item:hover,
body.theme-icons .topBar .nav-item.active {
  color: #2eaa53;
}

body.theme-icons .topBar .nav-item.active:after {
  background-color: #2eaa53;
}

body.theme-icons .font-example {
  border-color: #2eaa53;
}

body.theme-icons .font-example .font-heading {
  color: #2eaa53;
}

body.theme-icons .icon-item {
  border-color: #2eaa53;
}

body.theme-icons .icon-item .icon {
  color: #2eaa53;
}


body.theme-icons .image-example {
  border-color: #2eaa53;
}

body.theme-logos {
  background-color: #fffdf8;
  color: #181818;
}

body.theme-logos h2,
body.theme-logos h3 {
  color: #fdc609;
}

body.theme-logos .header.header-mode {
  background: #181818;
}

body.theme-logos .header.header-mode .header-title {
  color: #fdc609;
}

body.theme-logos .topBar {
  border-top: 3px solid #fdc609;
}

body.theme-logos .topBar .nav-item:hover,
body.theme-logos .topBar .nav-item.active {
  color: #fdc609;
}



body.theme-logos .topBar .nav-item.active:after {
  background-color: #fdc609;
}

body.theme-logos .font-example {
  border-color: #fdc609;
}

body.theme-logos .font-example .font-heading {
  color: #fdc609;
}

body.theme-logos .icon-item {
  border-color: #fdc609;
}

body.theme-logos .icon-item .icon {
  color: #fdc609;
}



body.theme-logos .image-example {
  border-color: #fdc609;
}

body.theme-images {
  background-color: #fff8fc;
  color: #181818;
}

body.theme-images h2,
body.theme-images h3 {
  color: #f087b5;
}

body.theme-images .header.header-mode {
  background: #181818;
}

body.theme-images .header.header-mode .header-title {
  color: #f087b5;
}

body.theme-images .topBar {
  border-top: 3px solid #f087b5;
}

body.theme-images .topBar .nav-item:hover,
body.theme-images .topBar .nav-item.active {
  color: #f087b5;
}

body.theme-images .topBar .nav-item.active:after {
  background-color: #f087b5;
}

body.theme-images .font-example {
  border-color: #f087b5;
}

body.theme-images .font-example .font-heading {
  color: #f087b5;
}

body.theme-images .icon-item {
  border-color: #f087b5;
}

body.theme-images .icon-item .icon {
  color: #f087b5;
}

body.theme-images .image-example {
  border-color: #f087b5;
}



@media (max-width: 768px) {
  .main-content {
    padding: .5rem;
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
  }
}
</style>

<script setup lang="ts">
import { ref, computed, onMounted } from 'vue'
import BrandHeader from './components/BrandHeader.vue'
import BrandtopBar from './components/BrandTopbar.vue'
import BrandSection from './components/BrandSection.vue'
import ThemeIndicator from './components/ThemeIndicator.vue'

const sections = [
  { id: 'logos', title: 'Logos', content: 'logos' },
  { id: 'Tipografía', title: 'Tipografía', content: 'typo' },
  { id: 'colors', title: 'Colores', content: 'colors' },
  { id: 'icons', title: 'Iconos', content: 'icons' },
  { id: 'images', title: 'Imagen', content: 'images' },
]

const currentSection = ref('logos')
const isHeaderMode = ref(false)
const isIndicatorVisible = ref(false)
const isTransitioning = ref(false)
const transitionDirection = ref<string | null>(null)
const exitDirection = ref<string | null>(null)

const currentSectionName = computed(() => {
  const section = sections.find(s => s.id === currentSection.value)
  return section ? section.title : ''
})

const changeSection = (sectionId: string) => {
  const currentIndex = sections.findIndex(s => s.id === currentSection.value)
  const newIndex = sections.findIndex(s => s.id === sectionId)
  if (newIndex === -1) return

  const direction = newIndex > currentIndex ? 'right' : 'left'
  transitionDirection.value = direction
  exitDirection.value = direction === 'right' ? 'left' : 'right'

  showTransitionEffect()
  setTimeout(() => {
    currentSection.value = sectionId
    document.body.className = `theme-${sectionId}`
    showThemeIndicator()
  }, 100)
}

const showThemeIndicator = () => {
  isIndicatorVisible.value = true
  setTimeout(() => {
    isIndicatorVisible.value = false
  }, 2000)
}

const showTransitionEffect = () => {
  isTransitioning.value = true
  setTimeout(() => {
    isTransitioning.value = false
  }, 500)
}

const handleScroll = () => {
  isHeaderMode.value = window.scrollY > 0.1
}

onMounted(() => {
  document.body.classList.add(`theme-${currentSection.value}`)
  window.addEventListener('scroll', handleScroll)

  return () => {
    window.removeEventListener('scroll', handleScroll)
  }
})
</script>