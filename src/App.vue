<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import EducacionComponente from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponente from './components/ProyectosComponente.vue';
import HabilidadesComponente from './components/HabilidadesComponente.vue';
import InteresesComponente from './components/InteresesComponente.vue';
</script>

<template>
    <header id="top">
        <!--Barra de Navegacion-->
        <NavBar />
        <!--Componente Datos Personales-->
        <DatosPersonales />
    </header>
    <main>
        <!--el estilo css de section se encuentra en base.css-->
        <section id="educacion">
            <h2>Educación - Cursos</h2>
            <!--Componente Educación-->
            <EducacionComponente />
        </section>
        <section id="experiencia">
            <h2>Experiencia</h2>
            <!--Componente Experiencia-->
            <ExperienciaComponente />
        </section>
        <section id="proyectos">
            <h2>Proyectos</h2>
            <!--Componente Proyectos-->
            <ProyectosComponente />
        </section>
        <section id="habilidades">
            <!--Componente Habilidades-->
            <h2>Habilidades</h2>
            <HabilidadesComponente />
        </section>
        <section id="intereses">
            <!--Componente Intereses-->
            <h2>Intereses</h2>
            <InteresesComponente />
        </section>
    </main>
    <footer>
        <a href="#top">Inicio</a>
        <p>© 2025 Tapia Ximena - Portafolio web - UTN FRSR</p>
    </footer>
</template>

<style>
/* Hacemos que todo el html y body ocupe 100% de ancho y alto */
html, body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
  overflow-x: hidden; /* evita scroll horizontal por el gradiente */
}

/* Fondo animado para toda la app */
body {
  background: linear-gradient(-45deg, #2E0854, #614081, #9517e9, #5A0D80);
  background-size: 600% 600%; /* gradiente más grande para animación */
  animation: gradientBG 10s ease infinite; /* animación suave y continua */
}

/* #app ocupa toda la altura disponible */
#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  color: rgb(229, 184, 255);
}

/* Animación que desplaza el gradiente para que cambien los colores */
@keyframes gradientBG {
  0% { background-position: 0% 50%; }
  25% { background-position: 50% 100%; }
  50% { background-position: 100% 50%; }
  75% { background-position: 50% 0%; }
  100% { background-position: 0% 50%; }
}

/* Footer y títulos visibles */
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  font-size: 1.3rem;
}
h2 {
  color: rgb(200, 180, 220); /* contraste con morado */
}
</style>

