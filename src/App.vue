<script setup>
import Logo from './components/icons/Logo.vue'
</script>

<template>
  <header>
    <nav>
      <ul>
        <li class="logo"><Logo /></li>
        <li><a href="#">Inicio</a></li>
        <li><a href="#">Sobre mim</a></li>
        <li><a href="#">Habilidades</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Serviços</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <div class="">
      <HelloWorld msg="You did it!" />
    </div>
    <TheWelcome />
  </main>
</template>

<style scoped>
@media (min-width: 1024px) {
 
  nav ul {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    font-size: 1rem;
  }

  nav ul li {
    list-style: none;
    margin: auto 1rem;
  }
}
</style>
