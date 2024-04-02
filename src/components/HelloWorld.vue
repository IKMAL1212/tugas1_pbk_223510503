<template>
  <div class="greetings">
    <h1 class="title">{{ msg }}</h1>
    <H2>SAYA</H2>
    <h3 class="name"> Ikmal Ardhiyaro</h3>
  </div>
</template>

<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.greetings {
  text-align: center;
  padding: 20px;
  border-radius: 10px;
  background-color: #ffffff;
  transition:
    background-color 0.3s,
    transform 0.3s,
    box-shadow 0.3s;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.greetings:hover {
  background-color: #f5f5f5;
  transform: translateY(-5px);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

.title {
  font-weight: bold;
  font-size: 2.6rem;
  color: #198754;
  margin: 0;
}

.name {
  font-size: 1.2rem;
  color: #6c757d;
  margin-top: 5px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.greetings a {
  color: #0d6efd;
  text-decoration: none;
}

.greetings a:hover {
  text-decoration: underline;
}
</style>
