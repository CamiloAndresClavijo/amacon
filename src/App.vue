<template>
  <v-app>
    <!-- Bar principal -->
    <v-app-bar
      absolute
      color="#43a047"
      dark
      shrink-on-scroll
      prominent
      src="https://picsum.photos/1920/1080?random"
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-5"
      scroll-threshold="500">
      
      <!-- Template degrado del fondo de la bar principal -->
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(55,236,186,.7), rgba(25,32,72,.7)"
        ></v-img>
      </template>

       <!-- Boton de menu -->
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <!-- Nombre del menu -->
      <v-toolbar-title>Amacon</v-toolbar-title>
    </v-app-bar>
    
    <!-- Estilo Bar -->
    <v-sheet
      id="scrolling-techniques-5"
      class="overflow-y-auto"
      max-height="600">
    </v-sheet>

   <!-- Component carrusel -->
   <Carrusel/>
  
  <!-- Footer -->
  <v-footer app>
   <!-- Component Footer -->
   <Footer/>
  </v-footer> 
 </v-app>

</template>

<!-- Script component -->
<script>

// Importacion de los componentes utilizados
import Carrusel  from './components/Carrusel'
import Footer  from './components/Footer'

export default {
  name: 'App',
  
  // Llamado de los componentes
  components: {
    Carrusel,
    Footer,
    
  },

  data: () => ({
    //
  }),
};
</script>