<style>
  html, body {
    overflow: hidden;
  }
  .__main {
    height: 600px;
    overflow-y: auto;
    background: url("~/static/img/imgbg2.gif") no-repeat !important;
    background-color: #000 !important;
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

        imgBg: 'img/imgbg.gif'
      }
    },
  }
  </script>
  