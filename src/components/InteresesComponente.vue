<script setup>
import { ref } from 'vue';
import FondoLineas from './FondoCirculo.vue';
//Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Desarrollo Web y Programación: Me interesa seguir aprendiendo sobre el desarrollo de páginas y aplicaciones web. Disfruto experimentar con HTML, CSS y JavaScript, y mejorar mis proyectos personales.',
    'Aprendizaje y Nuevas Tecnologías: Tengo curiosidad por las nuevas herramientas y tendencias tecnológicas, como la inteligencia artificial, el diseño responsivo y las aplicaciones móviles.',
    'Diseño y Creatividad: Me gusta combinar la programación con el diseño visual. Uso herramientas como Canva y Figma para crear interfaces atractivas y presentaciones organizadas.',
    'Actividades al Aire Libre: En mi tiempo libre disfruto caminar, salir en bicicleta y pasar tiempo al aire libre, lo que me ayuda a mantener un buen equilibrio entre el estudio y la vida personal.',
    'Fotografía y Contenidos Visuales: Me gusta la fotografía y la edición de imágenes, actividades que me inspiran a mantener una mirada creativa y detallista en mis proyectos.',
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLineas />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
    <!-- <div class="intereses-contenedor">
        <ul class="contenedor-lista">
            <li class="item">
                Desarrollo Web y Programación:
                Me interesa seguir aprendiendo sobre el desarrollo de páginas y aplicaciones web. Disfruto experimentar con HTML, CSS y JavaScript, y mejorar mis proyectos personales.
            </li>
            <li class="item">
                Aprendizaje y Nuevas Tecnologías:
                Tengo curiosidad por las nuevas herramientas y tendencias tecnológicas, como la inteligencia artificial, el diseño responsivo y las aplicaciones móviles.
            </li>
            <li class="item">
                Diseño y Creatividad:
                Me gusta combinar la programación con el diseño visual. Uso herramientas como Canva y Figma para crear interfaces atractivas y presentaciones organizadas.
            </li>
            <li class="item">
                Actividades al Aire Libre:
                En mi tiempo libre disfruto caminar, salir en bicicleta y pasar tiempo al aire libre, lo que me ayuda a mantener un buen equilibrio entre el estudio y la vida personal.
            </li>
            <li class="item">
               Fotografía y Contenidos Visuales:
                Me gusta la fotografía y la edición de imágenes, actividades que me inspiran a mantener una mirada creativa y detallista en mis proyectos.
            </li>
        </ul>
    </div> -->
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>