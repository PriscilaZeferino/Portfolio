<script setup>
import Navbar from '../components/Navbar.vue'
</script>

<template>
  <header class="header">
    <Navbar />
  </header>
  <main>
    <div class="home" id="home">
      <div class="home-avatar">
        <img
          src="../assets/img/avatar.jpeg"
          alt="uma garota fofa, com cabelo preto liso pouco abaixo dos ombros, olhos castanhos, usando óculos com moldura roxa, vestindo roupas feminas e confortaveis centralizadas na moldura, programando em um computador desktop."
        />
      </div>
      <div class="home-section">
        <div class="home-text">
          <h1>Olá, eu sou a <span>Priscila Zeferino</span></h1>
          <h2>Desenvolvedora Web | Freelancer</h2>
        </div>
        <div class="home-button">
          <button>Download CV</button>
          <button>Entrar em contato</button>
        </div>
      </div>
    </div>
  </main>
</template>
<style scoped>
.header {
  background-color: var(--color-background);
  padding-inline: 46px;
  width: 100vw;

  opacity: 0.8;
}

.home {
  display: flex;
  justify-content: center;
  align-items: center;

  flex-direction: row;
  flex-wrap: wrap;
  font-family: 'Inter', sans-serif;

  margin: 20px;
}

.home-avatar img {
  border-radius: 50%;
  width: 150px;
  height: 150px;

  margin: 10px;
}

.home-text {
  margin-block: 15px;
  line-height: 1.4;
  font-size: 1rem;
}

.home-text h1 span {
  font-size: 2rem;
  font-weight: 600;
  color: var(--color-primary);
}

.home-button button {
  border: none;
  background-color: var(--color-primary);

  font-size: 1rem;
  font-weight: 600;
  color: var(--color-text-button);

  width: 100%;
  height: 40px;

  cursor: pointer;

  margin: 5px 0;
}

.home-button button:hover {
  background-color: var(--color-hover);
}

@media (min-width: 620px) {
  .home-avatar img {
    border-radius: 50%;
    width: 400px;
    height: 400px;

    margin: 30px;
  }
}

@media (min-width: 1024px) {
  .home-avatar img {
    border-radius: 50%;
    width: 400px;
    height: 400px;

    margin: 30px;
  }

  .home-button button {
    margin-inline: 0 20px;
    max-width: 200px;
  }
}
</style>
