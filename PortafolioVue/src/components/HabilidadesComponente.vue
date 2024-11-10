<script setup>
import {ref} from 'vue';

const habilidades = ref([
    {
        id: 1, nombre: 'Lenguajes de Programación', habilidades: [
            {id:1, nombre: 'C#', nivel: 'Avanzado', icono: '/src/components/icons/csharp.svg'},
            {id:2, nombre: 'Java', nivel: 'Avanzado', icono: '/src/components/icons/java.svg'},
            {id:3, nombre: 'JavaScript', nivel: 'Avanzado', icono: '/src/components/icons/javascript.svg'},
            {id:4, nombre: 'Python', nivel: 'Avanzado', icono: '/src/components/icons/python.svg'}
        ]
    },
    {
        id: 2, nombre: 'Framework y librerías', habilidades: [
            {id:1, nombre: 'Angular', nivel: 'Avanzado', icono: '/src/components/icons/angular.svg'},
            {id:2, nombre: 'Vue', nivel: 'Avanzado', icono: '/src/components/icons/vue.svg'}
    ]      
    },
    {
        id: 3, nombre: 'Herramientas y Software', habilidades: [
            {id:1, nombre: 'Git', nivel: 'Avanzado', icono: '/src/components/icons/git.svg'},
            {id:2, nombre: 'GitHub', nivel: 'Avanzado', icono: '/src/components/icons/github.svg'},
            {id:3, nombre: 'Visual Studio', nivel: 'Avanzado', icono: '/src/components/icons/visualstudio.svg'},
            {id:4, nombre: 'Visual Studio Code', nivel: 'Avanzado', icono: '/src/components/icons/visualstudiocode.svg'}
        ]
    },
    {
        id: 4, nombre: 'Base de Datos', habilidades: [
            {id:1, nombre: 'MySQL', nivel: 'Avanzado', icono: '/src/components/icons/mysql.svg'},
            {id:2, nombre: 'SQL Server', nivel: 'Avanzado', icono: '/src/components/icons/sqlserver.svg'}
    ]      
    },
    {
        id: 5, nombre: 'Idiomas', habilidades: [
            {id:1, nombre: 'Castellano', nivel: 'Avanzado', icono: '/src/components/icons/castellano.svg'},
            {id:2, nombre: 'Inglés', nivel: 'Avanzado', icono: '/src/components/icons/ingles.svg'}
    ]      
    }
]);
</script>

<template>

    <div class="skills-contenedor">        
        <div v-for="habilidad in habilidades" :key="habilidad.id" class="skills-categoria">
            <h3>{{ habilidad.nombre }}</h3>
            <ul class="skills">
                <li v-for="habilidad in habilidad.habilidades" :key="habilidad.id" class="skill">
                    <img :src="habilidad.icono" :alt="habilidad.nombre">
                    <!-- <span>{{ habilidad.nombre }} :{{habilidad.nivel}}</span> -->
                </li>
            </ul>
        </div>        
    </div>
</template>

<style scoped>
.skills-contenedor{
    padding: 2rem;
}

.skill-categoria{
    margin-bottom: 20px;
}

.skill-categoria h3{
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5em;
    color: aliceblue;
    font-size: 1.5em;
    font-weight: bold;
}

.skills{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill{
    display: flex;
    justify-content: center;
    gap: 10px;
    background-color: rgba(241, 245, 243, 0.856);
    padding: 0.3rem;
    border-radius: 0.8px;
    box-shadow: 0px 4px 12px rgba(2, 151, 151, 0.963);
    flex: 1 1 200px;
    max-width: 250px;  
}

.skill:hover{
    background-color: rgba(2, 151, 151, 0.963);
}

.skill img{
    width: 35px;
    height: 35px;
}

/* .skill span{
    font-size: 1em;
    color: #333;
} */

.skill:hover{
    font-size: 1.3em;
    transition: 2s ease;
}

@media (max-width: 768px){
    .skill-categoria h3{
        justify-content: center;
    }

    .skill{
        justify-content: center
    }
}
</style>