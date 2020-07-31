<template>
  <Contactme></Contactme>

</template>

<script>
import Contactme from '@/components/Contactme.vue'
  export default {
    
    components: {
    Contactme
    },

    data () {
      return {
        alignmentsAvailable: [
          'start',
          'center',
          'end',
          'baseline',
          'stretch',
        ],
        alignment: 'center',
        dense: false,
        justifyAvailable: [
          'start',
          'center',
          'end',
          'space-around',
          'space-between',
        ],
        justify: 'center',
      }
    },
  }
</script>