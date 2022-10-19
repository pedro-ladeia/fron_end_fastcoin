<template>
    <v-app-bar
        class="pt-4 nav-bar-Wrapper"
        color="transparent"
    >
    <v-toolbar-title class="logo">FastCoin</v-toolbar-title>
    <v-bottom-navigation
    class="nav-bar-opts"
    :value="value"
    color="teal"
    width="50%"
    grow
  >
    <v-btn class="btn-nav">
      <span>Notices</span>
    </v-btn>

    <v-btn class="btn-nav">
      <span>Graphics</span>
    </v-btn>

    <v-btn class="btn-nav">
      <span>Articles</span>
    </v-btn>

    <v-btn class="btn-nav">
      <span>TokenPedia</span>
    </v-btn>

  </v-bottom-navigation>
    

    <v-text-field
        class="mr-10"
        prepend-inner-icon="mdi-magnify"
        v-model="strSearch"
        :label="lblSearch"
        color="teal"
        ></v-text-field>

        <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs" v-on="on">
            <v-icon>mdi-earth</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item :key="n" @click="() => {}">
            Português
          </v-list-item>

          <v-list-item :key="n" @click="() => {}">
            English
          </v-list-item>

          <v-list-item :key="n" @click="() => {}">
            Español
          </v-list-item>

          <v-list-item :key="n" @click="() => {}">
            普通话
          </v-list-item>

        </v-list>
      </v-menu>

    <!--<v-btn class="ml-12"> <v-icon>mdi-earth</v-icon></v-btn>-->

    </v-app-bar>
</template>


<style>

    .nav-bar-Wrapper {
        background: rgba(255, 255, 255, 0) !important;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1) !important;
        backdrop-filter: blur(3.4px) !important;
        border: none !important;
    }
    .nav-bar-Wrapper .logo {
        font-size: 20pt;
    }

    .nav-bar-Wrapper .nav-bar-opts {
        background-color:transparent !important;
        border: none;
        box-shadow: none !important;
        margin: 0 4rem 0 5rem;
    }
    .nav-bar-Wrapper .nav-bar-opts span {
        font-size: 12pt;
    }



</style>

<script>
export default {
    data() {
        return {
            strSearch: '',
            lblSearch: 'Search'
        }
    }
}
</script>