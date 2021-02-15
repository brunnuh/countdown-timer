<template>
  <div id="app">

    <InfoComponent />
    <PatternComponent />
  </div>
</template>

<script>
import PatternComponent from '@/components/Pattern-Hills.vue'
import InfoComponent from '@/components/Info.vue'

export default {
  name: 'App',
  components: {
    PatternComponent,
    InfoComponent
  }
}
</script>

<style>
#app {
  display: grid;
  grid-template-rows: 613px auto;

  grid-template-areas: 'INF' 'MNT';
  background-image: linear-gradient( #2F2439, #1E1F29, #343650);
  
 
}

/** responsive */

    @media (max-width: 765px) {
      #app{
        grid-template-rows: 390px auto;
      }
    }
</style>
