<template>
  <v-row justify="center" align="center">
    <NavBar/>

  
 <!-- 
  <v-carousel
    cycle
    height="40rem"
    hide-delimiter-background
    show-arrows-on-hover
  >


      >
     
      <v-carousel-item
          v-for="(slide, i) in slides"
          :key="i"
    >
     
      <img
        :src="colors[i]"
        width="100%"
        class="imgTest"
      >
    </v-carousel-item>

      <div class="text-h2">
          {{ slide }} Slide
      </div>
    
  </v-carousel>-->

  <v-carousel
    cycle
    height="40rem"
    hide-delimiter-background
    show-arrows-on-hover
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
    <v-row
          class="fill-height"
          align="end"
          justify="center"
        >
      <img
        :src="colors[i]"
        width="100%"
      >
        
          <div class="text-h2 mb-15"
          >
            {{ slide }} Slide
          </div>
        </v-row>
    </v-carousel-item>
  </v-carousel>




  </v-row>
</template>

<style>

  .text-h2 {
    position: absolute;

    background: rgba(255, 255, 255, 0) !important;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1) !important;
        backdrop-filter: blur(3.4px) !important;
        border: none !important;
  }

</style>


<script>
import NavBar from '~/components/navBar.vue';
export default {
  name: "IndexPage",
  data() {
      return {
        
              colors: [
                'img/imgtest.jpg',
                'warning',
                'pink darken-2',
                'red lighten-1',
                'deep-purple accent-4',
              ],
              slides: [
                'Os touros Cardano perdem o fôlego após o hard fork Vasil: Queda de preço de 40% ADA.',
                'Second',
                'Third',
                'Fourth',
                'Fifth',
              ]
      }
  },
  components: { NavBar }
    
}
</script>
