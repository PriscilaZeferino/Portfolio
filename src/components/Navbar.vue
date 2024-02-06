<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Logo from '../components/icons/Logo.vue'
import BurgerMenu from './icons/BurgerMenu.vue';

const showMenu = ref(true)

function openMenu() {
  showMenu.value = !showMenu.value
}

const handleResize = () => {
  windowWidth.value = window.innerWidth
  windowHeight.value = window.innerHeight

  if (windowWidth < 768) {
    showMenu.value = false
  } else {
    showMenu.value = true
  }
}

onMounted(() => {
  window.addEventListener('resize', handleResize)
})

onUnmounted(() => {
  window.removeEventListener('resize', handleResize)
})
</script>
<template>
  <nav class="nav">
    <div class="navbar-mobile">
      <Logo />
      <button  class="hamburger-button" :class="{ isActive: showMenu }" @click="openMenu">
        <BurgerMenu :isActive="!showMenu"/>
      </button>
    </div>
    <div class="navbar-list" :class="{ showMenu: showMenu }">
      <ul class="nav-items">
        <li><a href="#">Inicio</a></li>
        <li><a href="#">Sobre mim</a></li>
        <li><a href="#">Habilidades</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Serviços</a></li>
      </ul>
    </div>
    <div class="toggleTheme">

    </div>
  </nav>
</template>
<style scoped>
.hamburger-button{
  display: block;
  border: none;
  background: none;
  cursor: pointer;
}

.nav-items {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
}

.navbar-mobile {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar-list ul {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
}

.nav-items a {
  font-size: 18px;
  color: var(--color-text);
}



.showMenu {
  display: none;
}

@media (min-width: 768px) {
  .hamburger-button {
    display: none;
  }

  .nav {
    max-width: 1280px;
    height: 70px;
    margin-inline: auto;

    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .nav-items {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: row;

    display: flex;
    gap: 32px;
    list-style: none;
  }

  .nav-items a {
    font-size: 18px;
    color: var(--color-text);
    padding-block: 6px;
  }

  .showMenu {
    display: block;
  }
}
</style>
