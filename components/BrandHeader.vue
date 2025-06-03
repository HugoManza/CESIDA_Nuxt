<template>
  <header class="header" :class="{ 'landing-mode': !isHeaderMode, 'header-mode': isHeaderMode }">
    <div class="landing-content">
      <div class="landing-text">
        <div class="landing-logo">CESIDA</div>
        <h1>Br<span class="script">a</span>nd Ma<span class="script">n</span>ua<span class="script">l</span></h1>
        <p>Alejandra Veloso <br>Hugo Manzano <br>Ana Díaz</p>
      </div>
      <div class="landing-image">
        <div class="image-container">
          <img src="../assets/img/Pictogramas2.png" alt="CESIDA Brand Illustration" class="hero-image">
        </div>
      </div>
    </div>
    <div class="header-content">
      <div class="header-logo"><img src="../assets/img/logos/CESIDA_White.svg" alt=""></div>
      <div class="header-title">Manual de Marca</div>
    </div>
  </header>
</template>

<script setup>
defineProps({
  currentSection: {
    type: String,
    required: true
  },
  isHeaderMode: {
    type: Boolean,
    default: true,
  }
})
</script>

<style scoped>
.header {
  width: 100%;
  background-color: #181818;
  color: #fff;
  transition: height 0.6s cubic-bezier(0.22, 1, 0.36, 1), padding 0.6s cubic-bezier(0.22, 1, 0.36, 1);
  overflow: hidden;
  position: relative;
  z-index: 100;
  will-change: height;
}

.header.landing-mode {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}

.header.landing-mode .landing-content {
  opacity: 1;
  transform: translateY(0);
  transition: opacity 0.6s cubic-bezier(0.22, 1, 0.36, 1), transform 0.6s cubic-bezier(0.22, 1, 0.36, 1);
  max-width: 80%;
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.header.landing-mode .landing-content .landing-text {
  flex: 1;
  text-align: left;
  padding-right: 2rem;
}

.header.landing-mode .landing-content .landing-image {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header.landing-mode .landing-content .landing-image .image-container {
  width: 100%;
  max-width: 600px;
}

.header.landing-mode .landing-content .landing-image .image-container .hero-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  padding: 5rem;
}

.header.landing-mode .header-content {
  opacity: 0;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transform: translateY(-100%);
  justify-content: space-between;
}

.header.header-mode {
  height: 5rem;
  position: fixed;
  display: flex;
  justify-content: space-between;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.header.header-mode .landing-content {
  opacity: 0;
  transform: translateY(-100%);
  position: absolute;
  display: none;
}

.header.header-mode .header-content {
  opacity: 1;
  transform: translateY(0);
  transition: opacity 0.6s cubic-bezier(0.22, 1, 0.36, 1), transform 0.6s cubic-bezier(0.22, 1, 0.36, 1);
  display: flex;
  align-items: center;
  height: 100%;
  padding: 0 4rem;
  width: 100%;
  justify-content: space-between;
}

.header .landing-logo {
  font-size: 4rem;
  font-weight: 700;
  letter-spacing: 2px;
  margin-bottom: 1rem;
  

  
}



.header h1 {
  font-family: "Transforma", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 2.5rem;
  margin-bottom: 2rem;
  color: #fff;
}

.header p {
  font-size: 1.2rem;
  margin-bottom: 3rem;
  max-width: 600px;
  font-family: "Lexend Deca", sans-serif;
}

.header .header-logo {
  max-width: 100px;
  width: 20%;
  align-items: center;
  display: flex;
 
}

.header .header-logo img {
  width: 100%;
  height: 3.5rem;
  object-fit: contain;
}

.header .header-title {
  font-size: 1.4rem;
  font-weight: 500;
  transition: color 0.4s ease;
}

@media (max-width: 992px) {
  .header.landing-mode .landing-content {
    flex-direction: column;
    display: flex;
    flex-direction: column;
  }
  .header.landing-mode .landing-content .landing-text {
    text-align: center;
    padding-right: 0;
    margin-bottom: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .header.landing-mode .landing-content .landing-image .image-container {
    display: none;
  }
}

@media (max-width: 768px) {

  .header.header-mode .header-content {
  justify-content: space-between;
}

  .header.landing-mode .landing-content .landing-text .landing-logo {
    font-size: 3rem;
  }
  .header.landing-mode .landing-content .landing-text h1 {
    font-size: 2rem;
  }
  .header.landing-mode .landing-content .landing-text p {
    font-size: 1rem;
  }
  .header.landing-mode .landing-content .landing-image .image-container {
    max-width: 300px;
  }
  .header.header-mode .header-logo {
    font-size: 1.5rem;
  }
  .header.header-mode .header-title {
    font-size: 1.2rem;
  }
}
</style>