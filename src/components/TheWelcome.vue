<template>
  <div class="centered-container">
    <div class="welcome-container">
      <!-- WelcomeItem pertama -->
      <WelcomeItem class="welcome-item">
        <template #icon>
          <DocumentationIcon />
        </template>
        <template #heading>Data Diri</template>
        <p><strong>Nama:</strong> Ikmal Ardhiyaro</p>
        <p><strong>NPM:</strong> 223510503</p>
        <p><strong>Matkul:</strong> Praktikum PBK</p>
      </WelcomeItem>

      <!-- WelcomeItem kedua -->
      <WelcomeItem class="welcome-item">
        <template #icon>
          <ToolingIcon />
        </template>
        <template #heading>Keahlian</template>
        <ul>
          <li>Pengamat</li>
          <li>Berdikusi</li>
          <li>HTML</li>
          <li>CSS</li>
          <li>JS</li>
        </ul>
      </WelcomeItem>

      <!-- WelcomeItem ketiga -->
      <WelcomeItem class="welcome-item">
        <template #icon>
          <EcosystemIcon />
        </template>
        <template #heading>Tentang Saya</template>
        <p>
          Saya bersusia 21 tahun, memiliki pengalaman sebagai kepala sebuah perkantoran berbasis
          perekonomian daerah dan juga pernah menjadi wartawan di sebuah stasiun televisi.
        </p>
      </WelcomeItem>

      <!-- WelcomeItem empat -->
      <WelcomeItem class="welcome-item">
        <template #icon>
          <SupportIcon />
        </template>
        <template #heading>Kontak</template>
        <p><strong>No HP:</strong> 085179714126</p>
        <p><strong>Email:</strong> ikmalardhiyaro012@gmail.com</p>
      </WelcomeItem>
    </div>
  </div>
</template>

<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<style scoped>
.centered-container {
  display: flex;
  justify-content: center;
}

.welcome-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}

.welcome-item {
  display: flex;
  flex-direction: column;
  padding: 20px;
  border-radius: 10px;
  background-color: #ffffff;
  transition: transform 0.3s ease;
  font-family: 'Times New Roman', Times, serif;
}

.welcome-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.welcome-item p {
  margin: 10px 0;
}

.welcome-item ul {
  list-style-type: none;
  padding: 0;
  margin: 10px 0;
}

.welcome-item ul li {
  margin-bottom: 5px;
}

.welcome-item a {
  color: #3182ce;
  text-decoration: none;
}

.welcome-item a:hover {
  text-decoration: underline;
}

.welcome-item code {
  background-color: #edf2f7;
  padding: 2px 4px;
  border-radius: 4px;
}
</style>
