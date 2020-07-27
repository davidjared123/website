<template>
  <v-app>
    
    <Toolbar></Toolbar>

    <v-main>
      
    </v-main>
   
  </v-app>
</template>

<script>
import Toolbar from './components/Toolbar';

export default {
  name: 'App',

  components: {
    Toolbar,
  },

  data: () => ({
    //
  }),
};
</script>
