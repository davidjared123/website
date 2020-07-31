<template>
  <v-container fluid class="pt-0">
      <v-row align="center">
          <v-col class="text-center" cols="12" md="5" >
            <h1>Contacto</h1>
            <p class="mb-0">Escribir para mas informacion</p>
            <p>te guiaremos en el camino</p>
            <v-btn depressed>Contactanos</v-btn>
            <br/>
            <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-5 mt-8 pa-8"
            icon
            >
          <v-icon size="25px">{{ icon }}</v-icon>
        </v-btn>
          </v-col>
          <v-col class="" cols="12" md="7">
            <v-img src="@/../public/call.svg" aspect-ratio="1.4"></v-img>
          </v-col>
      </v-row>
      
         <v-footer 
         absolute
            class="font-weight-medium"
         >
        <v-spacer></v-spacer>
        <div>&copy; {{ new Date().getFullYear() }}</div>
        </v-footer>
  </v-container>
</template>

<script>
export default {
name: 'Contactme',
codeweb: '<CodeWeb/>',
data: ()=>{
    return{
        icons: [
        'facebook',
        'email',
        'phone',
        ]
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

    .footer{
        font-size: 25px;
    }
    </style>