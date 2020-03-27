<template>
<!-- Carrusel principal -->
  <v-carousel 
    cycle
    hide-delimiter-background
    show-arrows-on-hover>

    <!-- Item carrusel principal -->
    <v-carousel-item
      v-for="(imagen, i) in imagens"
      :key="i">

      <!-- Estilo del carrusel principal -->
      <v-sheet
        :color="colors[i]"
        height="1500px"
        absolute>

        <!-- Row para centrar el texto en el carrusel -->
        <v-row class="fill-height"
          align="center"
          justify="center">

          <!-- Division de los display en el carrusel -->
          <div class="display-3">{{ imagen }} Imagens</div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<!-- Script component -->
<script> 

  export default {

    data () {
      return {
        colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        imagens: [
          'A',
          'B',
          'C',
          'D',
          'E',
        ],
      }
    },
  }
</script>

