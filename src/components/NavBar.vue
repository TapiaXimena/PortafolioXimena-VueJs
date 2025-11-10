<template>
    <nav class="navbar">
        <div class="navbar-menu">
            <ul>
                <li v-for="nav in navegacion" :key="nav.nombre">
                    <a :href="nav.enlace" class="nav-item">{{nav.nombre}}</a> 
                </li>
            </ul>
        </div>
    </nav>
</template>

<script setup>
import { ref } from 'vue';
const navegacion= ref([
    {id:1, nombre:'Educación', enlace:'#educacion'},
    {id:2, nombre:'Experiencia', enlace:'#experiencia'},
    {id:3, nombre:'Proyectos', enlace:'#proyectos'},
    {id:4, nombre:'Habilidades', enlace:'#habilidades'},
    {id:5, nombre:'Intereses', enlace:'#intereses'}
]);
</script>

<style scoped>
.navbar {
    background-color: rgba(81, 27, 107, 0.726);
    color: #ecd5f3;
    padding: 0.5rem 1rem;
    align-items: center;
}

.navbar-menu {
    display: flex;
    justify-content: flex-end;
}

/* --- ESTA ES LA PARTE MÁS IMPORTANTE --- */
.navbar-menu ul {
    display: flex;         /* 1. Pone los <li> en línea horizontal */
    flex-wrap: wrap;       /* 2. Permite que bajen de línea si no caben */
    list-style: none;      /* 3. Quita los puntos de la lista */
    padding: 0;            /* 4. ¡Quita el padding que causaba el error! */
    margin: 0;             /* 5. Quita el margen por defecto */
}

/* Es mejor aplicar el margen al <li> para separar los botones */
.navbar-menu li {
    margin-right: 0.5rem; /* Ajusta esto para la separación que quieras */
}
.navbar-menu li:last-child {
    margin-right: 0; /* El último elemento no necesita margen */
}

/* Estilos para el enlace (tu clase .nav-item) */
.nav-item {
    display: block; /* Hace que el padding se aplique correctamente */
    color: #ecd5f3;
    border: 1px solid hsla(293, 73%, 40%, 0.39);
    border-radius: 5px;
    text-decoration: none;
    transition: 0.4s;
    padding: 5px 10px; /* Un poco más de espacio a los lados */
}

.nav-item:hover {
    background-color: hsla(290, 41%, 66%, 0.712);
}

/* El CSS global 'a' y '.nav-list' ya no son necesarios si usamos .nav-item */

@media (max-width: 768px) {
  .navbar-menu {
    display: flex;
    justify-content: flex-end;
    width: 100%;
  }
  
  /* Opcional: Centrar los items en móvil */
  .navbar-menu ul {
    justify-content: center;
  }
}
</style>