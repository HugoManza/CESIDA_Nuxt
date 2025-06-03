<template>
  <nav class="topBar" :class="{ 'expanded': isExpanded }">
    <div class="topBar-header">
      <div class="nav-toggle" @click="toggletopBar">
        <span class="toggle-icon">☰</span>
      </div>
      <ul class="nav-list">
        <li v-for="section in sections" :key="section.id" class="nav-item"
          :class="{ 'active': currentSection === section.id }" :data-section="section.id"
          @click="selectSection(section.id)">
          {{ section.title }}
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const props = defineProps({
  sections: {
    type: Array,
    required: true
  },
  currentSection: {
    type: String,
    required: true
  }
})

const emit = defineEmits(['change-section'])

const isExpanded = ref(false)

const toggletopBar = () => {
  isExpanded.value = !isExpanded.value
}

const selectSection = (sectionId) => {
  emit('change-section', sectionId)

  if (process.client && window.innerWidth <= 768) {
    isExpanded.value = false
  }
}

const handleClickOutside = (event) => {
  if (
    window.innerWidth <= 768 &&
    isExpanded.value &&
    !event.target.closest('.topBar') &&
    !event.target.closest('.nav-toggle')
  ) {
    isExpanded.value = false
  }
}

const handleResize = () => {
  if (window.innerWidth > 768) {
    isExpanded.value = false
  }
}

onMounted(() => {
  if (process.client) {
    document.addEventListener('click', handleClickOutside)
    window.addEventListener('resize', handleResize)
  }
})

onUnmounted(() => {
  if (process.client) {
    document.removeEventListener('click', handleClickOutside)
    window.removeEventListener('resize', handleResize)
  }
})
</script>

<style scoped>
.topBar {
  background-color: #fff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 80px;
  z-index: 90;
  width: 100%;
  height: 60px;
  transition: height 0.4s ease, background-color 0.4s ease, border-top 0.4s ease;
  overflow: hidden;
}

.topBar.expanded {
  height: auto;
}

.topBar .topBar-header {
  display: flex;
  position: relative;
}

.topBar .topBar-header .nav-toggle {
  display: none;
  position: absolute;
  top: 0;
  right: 1rem;
  height: 60px;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  z-index: 10;
  padding: 0 1rem;
}

.topBar .topBar-header .nav-toggle .toggle-icon {
  font-size: 1.5rem;
  transition: transform 0.4s ease;
  display: block;
  color: #181818;
}

.topBar .topBar-header .nav-list {
  display: flex;
  list-style: none;
  width: 100%;
  padding: 0 1rem;
  flex-wrap: wrap;
}

.topBar .topBar-header .nav-list .nav-item {
  padding: 0 1.5rem;
  height: 60px;
  display: flex;
  align-items: center;
  cursor: pointer;
  transition: background-color 0.2s, color 0.2s;
  color: #181818;
  position: relative;
}

.topBar .topBar-header .nav-list .nav-item:hover,
.topBar .topBar-header .nav-list .nav-item.active {
  color: #54c1dc;
}

.topBar .topBar-header .nav-list .nav-item.active:after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 1.5rem;
  right: 1.5rem;
  height: 5px;
  background-color: #54c1dc;
}

@media (max-width: 768px) {
  .topBar .topBar-header .nav-toggle {
    display: flex;
  }

  .topBar .topBar-header .nav-list {
    flex-direction: column;
    padding-top: 60px;
  }

  .topBar .topBar-header .nav-list .nav-item {
    width: 100%;
    padding: 1rem 1.5rem;
    height: auto;
  }

  .topBar .topBar-header .nav-list .nav-item.active:after {
    left: 0;
    right: 0;
    bottom: auto;
    top: 0;
    width: 3px;
    height: 100%;
  }
}
</style>
