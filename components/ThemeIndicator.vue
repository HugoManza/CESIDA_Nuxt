<template>
  <div class="theme-indicator" :class="{ 'visible': isVisible }">
    Section: {{ sectionName }}
  </div>
</template>

<script setup>
defineProps({
  isVisible: {
    type: Boolean,
    default: false
  },
  sectionName: {
    type: String,
    default: ''
  }
})
</script>

<style scoped>
.theme-indicator {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: rgba(0, 0, 0, 0.7);
  color: #fff;
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 14px;
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.3s ease, transform 0.3s ease;
  z-index: 1000;
}

.theme-indicator.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>