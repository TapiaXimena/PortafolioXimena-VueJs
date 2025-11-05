<script setup>
import linkedin from '../assets/linkedin_icon.svg';
import instagram from '../assets/instagram_icon.svg';
import github from '../assets/github_icon.svg';

const title = 'Tapia Ximena';
const descripcion = 'Técnico Universitario en Programación - UTN';
const residencia = 'San Rafael, Mendoza, Argentina';
const presentacion = 'Hola, Bienvenido a mi portafolio personal. Soy estudiante de la Tecnicatura Universitaria en Programación.';
const redesSociales = [
  { id: 1, name: 'linkedin', src: linkedin, url: 'https://www.linkedin.com/in/ximena-tapia-1154a4302/' },
  { id: 2, name: 'Instagram', src: instagram, url: 'https://www.instagram.com/ximena.tapia.33/' },
  { id: 3, name: 'github', src: github, url: 'https://github.com/TapiaXimena' },
];
const telefono = '+54 9 2616045626';
</script>

<template>
  <section class="datos-personales">
    <div class="card">
      <h1>{{ title }}</h1>
      <h2>{{ descripcion }}</h2>
      <p>{{ presentacion }}</p>
      <ul class="container-lista">
        <li v-for="red in redesSociales" :key="red.id">
          <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
        </li>
      </ul>
      <a 
        :href="'https://wa.me/' + telefono.replace(/\D/g,'')" 
        target="_blank" 
        class="btn-whatsapp">
        WhatsApp: {{ telefono }}
      </a>
      <h4>{{ residencia }}</h4>
    </div>
  </section>
</template>

<style scoped>
h1 {
  font-size: 2.5rem;
  color: rgb(217, 205, 221);
}

p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.btn-whatsapp {
  display: inline-block;
  padding: 9px 20px;
  margin-top: 10px;
  background-color: #47176e; /* verde WhatsApp */
  color: white;
  font-weight: 600;
  border-radius: 8px;
  text-decoration: none;
  transition: 0.3s;
}

.btn-whatsapp:hover {
  background-color: #128C7E; /* verde más oscuro al pasar el mouse */
  box-shadow: 0 0 10px rgba(37, 211, 102, 0.5);
}

.card {
  background-color: rgba(81, 27, 107, 0.726);
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  text-align: center;
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
}

.icon-redsocial {
  align-items: center;
  background-color: aliceblue;
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
  background-color: rgb(28, 41, 52);
  box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
  font-size: 1.2rem;
  font-weight: 600;
}
</style>