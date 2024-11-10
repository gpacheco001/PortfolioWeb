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
        <NavBar/>
        <DatosPersonales/>
  </header>
  <main>
      <section id="educacion"><h2>Educación - Cursos</h2>
      <EducacionComponente />
      </section>

      <section id="experiencia"><h2>Experiencia</h2>
      <ExperienciaComponente />
      </section>
      
      <section id="proyectos"><h2>Proyectos</h2>
        <ProyectosComponente />
      </section>

      <section id="habilidades"><h2>Habilidades</h2></section>
      <HabilidadesComponente />
      <section id="intereses"><h2>Intereses</h2></section>
      <InteresesComponente />
  </main>

  <footer class="footer">
    <a href="#top" class="inicio">Inicio</a>
    <p>© 2024 Guillermo Pacheco - Portafolio web</p>
  </footer>
</template>

<style scoped>

.inicio{
  color: black;
}
.inicio:hover {
  text-decoration: underline; /* Subrayado cuando el mouse pasa sobre el enlace */
}

.footer{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding: .5rem;
  font-size: 1rem;
  position: relative;
  bottom: 0;
  left: 0;
  background-color: white;
  margin-top: 2rem;
} 

</style>