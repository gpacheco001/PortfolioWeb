<script setup>
import {ref} from 'vue';
var misproyectos = ref([]);
misproyectos.value =([
{
    id:1,
    src:'/src/assets/proyectoCSharp.jpg',
    titulo:'Video juego',
    descripcion: "Creé un video juego en Visual Studio con C#",
    // proyectoLink: "https://www.google.com.ar",
    githubLink: "https://github.com/gpacheco001/Video-Juego-C-"
},
{
    id:2,
    src:'/src/assets/blazor.jpg',
    titulo:'Calculadora web',
    descripcion: "Creé una calculadora con .Net y Blazor",
    //proyectoLink: "https://www.google.com.ar",
    githubLink: "https://github.com/gpacheco001/Calculadora-Web/tree/master"
},
])

</script>

<template>
    <div class="galeria" >
        <li class="proyecto" v-for="proyecto in misproyectos" :key="proyecto.id">
            <img :src="proyecto.src" :alt="proyecto.titulo">
            <div class="proyecto-info">
                <h3>{{ proyecto.titulo }}</h3>
                <p>{{proyecto.descripcion}}</p>
                <div class="proyecto-links">
                    <a :href="proyecto.proyectoLink" class="btn-ver-mas" target="_blank"
                    rel="noopeener noreferrer">Ver Proyecto</a>
                    <a :href="proyecto.githubLink" class="github-link" target="_blank"
                    rel="noopeener noreferrer">Ver codigo en github</a>
                </div>
            </div>
        </li>        
    </div>
</template>

<style>
/* .galeria{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    background-image: url('/src/assets/fondo-proyectos.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
} */

.galeria{
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    padding: 20px;
    justify-content: center;
    background: linear-gradient(-45deg, #021526, #03346E, #6EACDA, #E2E2B6);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
}

@keyframes gradient{
    0%{
        background-position: 0% 50%;
    }

    50%{
        background-position: 100% 50%;
    }

    100%{
        background-position: 0% 50%;
    }
}

.proyecto{
    display: flex;
    flex-direction: column;
    border: 2px;
    border-radius: 8px;
    overflow: hidden;
    background-color: #f9f9f9;
    max-width: 222px;
    flex: 1 1 300px;
}

.proyecto img{
    width: 100%;
    height: auto;
    display: block;
}

.proyecto-info{
    padding: 15px;
    text-align: center;    
}

.proyecto-info h3{
    margin: 10px 0;
    font-size: 1.3em;
    color: #666;
}

.proyecto-info p{
    margin: 10px 0;
    font-size: 1em;
    color: #666
}

.proyecto-links{
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 10px;
}

.proyecto-links .btn-ver-mas{
    background-color: #007bff;
    color: #fff;
    padding: 10px 15px;
    border-radius: 5px;
    text-decoration: none;
    transition: background-color 0.3s;    
}

.proyecto-links .btn-ver-mas:hover{
    background-color: #0056b3;    
}

.proyecto-links .github-link{
    color: #333;
    text-decoration: none;
    font-size: 0.9em;
}

.proyecto-links .github-link:hover{
    text-decoration: underline;    
}
</style>