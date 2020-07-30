<template>
  <v-container fluid>
      <v-row align="center">
          <v-col class="text-center" cols="12" md="6" >
            <h1 >Desarrollo web</h1>
            <p class="mb-0">desarrollo de sitios web</p>
            <p>y análisis de datos</p>
            <v-btn depressed>Solicitar Web</v-btn>
            
          </v-col>
          <v-col class="" cols="12" md="6">
            <v-img src="@/../public/main.png" aspect-ratio="1.20"></v-img>
          </v-col>
      </v-row>
  </v-container>
</template>

<script>
export default {
name: 'Main',
data: ()=>{
    return{

    }
}
}
</script>

<style scoped>
    h1{
        font-size: 5rem;
        font-weight: 300;
    }
    p{
        font-size: 1.8rem;
        font-weight: 280; 
    }

    @media (max-width: 600px){
    h1{
       font-size: 3.5rem; 
    }
    p{
        font-size: 1rem;
    }
    }

    @media (max-width: 400px){
    h1{
       font-size: 2.5rem; 
    }
    }
    </style>