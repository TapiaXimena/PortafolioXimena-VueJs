<script setup>
import icono1 from '../assets/academico.svg';
import icono2 from '../assets/practica_git.svg';
import icono3 from '../assets/configuracion.svg';
import icono4 from '../assets/desarrollo_web.svg'

import { ref } from 'vue';
const titulo = 'Desarrolladora en Formación – Tecnicatura Universitaria en Programación (UTN San Rafael)';
const fecha = 'Marzo 2024 – Actualidad';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Durante mi formación, he trabajado en distintos proyectos académicos y personales que me permitieron aplicar los conocimientos adquiridos en programación, desarrollo web y resolución de problemas. He desarrollado sitios y aplicaciones sencillas utilizando HTML, CSS y JavaScript, aplicando principios de diseño responsivo y estructuras lógicas básicas. También trabajé con PSeInt y Python para crear pequeños programas que refuerzan mi comprensión de los algoritmos, funciones y estructuras de control.' },
    { id: 2, src: icono2, parrafo: 'En mis prácticas, aprendí a utilizar Git y GitHub para el control de versiones y trabajo colaborativo, además de herramientas como Visual Studio Code, Canva y Figma para mejorar el diseño y la presentación de mis proyectos.' },
    { id: 3, src: icono3, parrafo: 'Actualmente, me encuentro desarrollando mi portafolio personal, un proyecto que refleja mi evolución como programadora, incluyendo mis proyectos, habilidades y aprendizajes.' },
    { id: 4, src: icono4, parrafo: 'Mi enfoque principal es seguir aprendiendo, fortalecer mis conocimientos en desarrollo web y adquirir experiencia en el trabajo en equipo dentro de proyectos de software reales.' },
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>

            <!-- <li class="item"><img class="imagen-svg" src="../assets/academico.svg" width="45rem" alt="">
                <p>Durante mi formación, he trabajado en distintos proyectos académicos y personales que me permitieron aplicar los conocimientos adquiridos en programación, desarrollo web y resolución de problemas. He desarrollado sitios y aplicaciones sencillas utilizando HTML, CSS y JavaScript, aplicando principios de diseño responsivo y estructuras lógicas básicas. También trabajé con PSeInt y Python para crear pequeños programas que refuerzan mi comprensión de los algoritmos, funciones y estructuras de control.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="../assets/practica_git.svg" width="45rem" alt="">
                <p>En mis prácticas, aprendí a utilizar Git y GitHub para el control de versiones y trabajo colaborativo, además de herramientas como Visual Studio Code, Canva y Figma para mejorar el diseño y la presentación de mis proyectos.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="../assets/configuracion.svg" width="45rem" alt="">
                <p>Actualmente, me encuentro desarrollando mi portafolio personal, un proyecto que refleja mi evolución como programadora, incluyendo mis proyectos, habilidades y aprendizajes.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="../assets/desarrollo_web.svg" width="45rem" alt="">
                <p>Mi enfoque principal es seguir aprendiendo, fortalecer mis conocimientos en desarrollo web y adquirir experiencia en el trabajo en equipo dentro de proyectos de software reales.</p>
            </li> -->
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgba(81, 27, 107, 0.726);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: rgba(165, 163, 240, 0.986);
}

.fecha {
    font-size: 1rem;
    color: rgb(208, 135, 222);
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
    color: rgb(250, 236, 253);
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>