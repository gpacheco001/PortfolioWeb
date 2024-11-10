<script setup>
import {ref} from 'vue';
// const titulo = 'Desarrollador Full Stack';
// const fecha = 'Enero 2022 a Noviembre 2024';
const experiencias = ref([
    {id:1, src:'/src/assets/mountain.svg', parrafo:'Caminatas en la montaña'},
    {id:2, src:'/src/assets/tools.svg', parrafo:'Reparaciones y herramientas'},
    {id:3, src:'/src/assets/bike.svg', parrafo:'Ciclismo de montaña'},
    //{id:4, src:'/src/assets/colaborar.svg', parrafo:'Colaboré con diseñadores'},
    //{id:5, src:'/src/assets/automatizar.svg', parrafo:'Automaticé procesos'},
]);
</script>

<template>
    <div class="card">
        <!-- <h3 class="titulo">{{titulo.toLocaleUpperCase()}}</h3> -->
        <!-- <p class="fecha">{{fecha}}</p> -->
        <ul class="listado">
            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
                <img class="imagen-svg" :src="experiencia.src" width="45rem" alt="experiencia.parrafo">
                <p>{{ experiencia.parrafo }}</p>
            </li>

            <!-- <li class="item"><img class="imagen-svg" src="/src/assets/liderar.svg" width="45rem" alt="">
                <p>Lidere un equipo de 5 desarrolladores</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/diseñar.svg" width="45rem" alt="">
                <p>Diseñe apicaciones</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/implementar.svg" width="45rem" alt="">
                <p>Implemente soluciones</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/colaborar.svg" width="45rem" alt="">
                <p>Colaboré con diseñadores</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/automatizar.svg" width="45rem" alt="">
                <p>Automatice procesos</p>
            </li> -->
        </ul>

    </div>
</template>

<style scoped>
.card{
  display: flex;
  flex-direction: column;
  padding: 2rem;
  background-color: rgb(159, 177, 192);
  border-radius: 15px;  
}
.titulo{
  text-align: center;
  font-size: 1.8rem;
  color: rgb(39, 35, 33);
}
.fecha{
  font-size: 1.25rem;  
  color: rgb(73, 72, 70);
  margin-bottom: 1rem;
}
.listado{
  font-size: 1.2rem;
  display: flex;
  flex-direction: column;
  color: rgb(81, 94, 94);
}
.item{
  align-items: center;
  display: flex;
  padding: 1rem;
  gap: 1.5rem;
}
</style>