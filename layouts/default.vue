<style>
  html, body {
    overflow: hidden;
  }
  .__main {
    height: 600px;
    overflow-y: auto;
  }

</style>

<template>
    <v-app>
      <v-main class="__main pr-16 pl-16 pt-2">
        <Nuxt />
      </v-main>
    </v-app>
  </template>

  
  <script>
  export default {
    name: 'DefaultLayout',
    
    data() {
      return {
      }
    },
  }
  </script>
  