<script setup>
import { ref } from 'vue';
// Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Mi interés principal, además de la programación, es la música. Actualmente llevo 4 años tocando el piano y tocando en restaurantes y en prestigiosas bodegas. La música es lo que más disfruto en la vida.',
    'Tengo un interés particular en los videojuegos desde pequeño, y siempre me interesó algún día poder crear un videojuego con mis compañeros de tecnicatura.',
    'Me encanta el desarrollo frontend porque me permite combinar creatividad y tecnología para crear interfaces atractivas y funcionales. Disfruto diseñar experiencias de usuario intuitivas y visualmente agradables.',
    'Me gusta mucho la programación porque su mundo abarca muchas cosas nuevas todos los días, y me gusta el hecho de crear algo con la programación.'
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLava />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    flex-direction: column; /* Para que los elementos se apilen verticalmente */
    align-items: center; /* Centra la lista horizontalmente */
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 2rem; /* Espaciado interior más amplio */
    background: hsl(29, 100%, 50%); /* Fondo transparente con color blanco */
    border-radius: 12px; /* Bordes redondeados */
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1); /* Sombra suave */
}

.contenedor-lista {
    list-style-type: none;
    padding: 0; /* Elimina el padding de la lista */
    margin: 0; /* Elimina el margen de la lista */
    color: #D9E0E8; /* Color de texto oscuro */
    font-size: 1.2rem; /* Tamaño de fuente más pequeño y elegante */
}

.item {
    margin-bottom: 1rem;
    padding: 1rem; /* Espaciado alrededor de cada ítem */
    background: rgba(106, 199, 227, 0.2); /* Fondo celeste semi-transparente */
    border: 1px solid #e1e1e1; /* Borde sutil alrededor de cada ítem */
    border-radius: 8px; /* Bordes redondeados para cada ítem */
    transition: none; /* Sin efecto de hover */
}
</style>
