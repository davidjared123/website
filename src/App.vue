<template>
  <v-app>

    <Toolbar></Toolbar>

    <!-- <Main></Main> -->

  <v-main>
    <router-view>
    </router-view>
  </v-main>
   
  </v-app>
</template>

<script>
import Toolbar from './components/Toolbar';
import Main from './components/Main';

export default {
  name: 'App',

  components: {
    Toolbar,
    Main,
  },

  data: () => ({
    //
  }),
};
</script>
