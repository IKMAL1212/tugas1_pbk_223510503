<template>
  <div>
    <header>
      <div class="wrapper">
        <nav class="navbar">
          <RouterLink to="/" class="navbar-item">Home</RouterLink>
          <RouterLink to="/about" class="navbar-item">About</RouterLink>
        </nav>
        <img alt="Vue logo" class="logo" src="@/assets/11.jpg" width="200" height="200" />
      </div>
      <HelloWorld msg="HALO!" />
    </header>
    <RouterView />
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<style scoped>
header {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.wrapper {
  display: flex;
  align-items: center;
}

.logo {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: filter 0.3s, transform 0.3s;
}

.logo:hover {
  filter: brightness(90%);
}

.navbar {
  margin-right: auto;
}

.navbar-item {
  margin-right: 20px;
  font-size: 24px;
  text-decoration: none;
  color: #333;
  transition: color 0.3s, text-shadow 0.3s;
}

.navbar-item:hover {
  color: #198754;
  text-shadow: 0 0 10px rgba(25, 135, 84, 0.5);
}

.router-view {
  padding: 20px;
}

.logo {
  animation: scaleAnimation 1s infinite alternate;
}

@keyframes scaleAnimation {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(1.05);
  }
}

/* Media Query for Laptop screens */
@media (min-width: 1024px) {
  header {
    flex-direction: row;
    justify-content: center;
  }
}
</style>
