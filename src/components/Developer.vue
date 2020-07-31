<template>
  <div class="mt-5">
    <v-container>
        <h1 class="text-center">Desarrollo web</h1>
        <h3 class="text-center">Ejemplos de tendencias web</h3>
      <v-row>
        <v-col
        v-for="(item, index) in items"
        :key="index"
        cols="12" md="12"
        >
          <v-card
            class="mx-auto"

          >
            <v-list-item>
              <v-list-item-content class="text-center">
                <v-list-item-title class="headline">
                    {{ item.name }}
                </v-list-item-title>
                <v-list-item-subtitle>{{ item.subtitle }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>

            <v-img 
            :src="item.img" 
            class=""
            >
            </v-img>

            <v-card-text
            height="0"
            >
              {{ item.description }}
            </v-card-text>

            <!-- <v-card-actions>
              <v-btn text color="#5ae4a7">
                Saber más
              </v-btn>
            </v-card-actions> -->
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <v-footer
    dark
    padless
    class="mt-10"
  >
    <v-card
      class="flex"
      flat
      tile
      color="#5ae4a7"
    >

      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>{{ codeweb }}</strong>
      </v-card-text>
    </v-card>
  </v-footer>
  </div>
</template>

<script>
export default {
  name: "Developer",

  data: () => {
    return {
        codeweb: '<CodeWeb/>',
        icons: [
        'facebook',
        'mail',
        'instagram',
      ],
      items: [
        {
          name: "Minimalista",
          subtitle: "menos es más",
          img: require("@/../public/minimalistaapple.jpg")
        },
        {
          name: "Contenido Dividido",
          subtitle: "fusion de contenido",
          img: require("@/../public/dividido.jpg")
        },
        {
          name: "Colores",
          subtitle: "diseño atrevido y unico",
          img: require("@/../public/color.png")
        },
        {
          name: "Tipografias",
          subtitle: "simple y atractivo",
          img: require("@/../public/tipografias.jpg")
        },
        {
          name: "3D",
          subtitle: "imagenes en tercera dimension",
          img: require("@/../public/3d.jpg")
        },
        {
          name: "Contenido Multimedia",
          subtitle: "Fotos y videos atractivos",
          img: require("@/../public/videos.gif")
        },
        {
          name: "Animaciones",
          subtitle: "anima tu web, pero no mucho",
          img: require("@/../public/animacion.gif")
        },
        {
          name: "Efecto Parallax",
          subtitle: "movimiento al bajar y subir",
          img: require("@/../public/parallax.gif")
        },
        {
          name: "Ilustraciones",
          subtitle: "imagenes personalizadas",
          img: require("@/../public/vector.gif")
        },
      ],
    };
  },
};
</script>

<style scoped>
 h1{
     font-size: 80px;
     font-weight: 300;
     
 } 

 h3{
     font-size: 30px;
     font-weight: 300;
 }  

 @media (max-width: 1000px){
   h1{
     font-size: 50px;     
 } 

 h3{
     font-size: 20px;
 }   
 } 
 @media (max-width: 370px){
   h1{
     font-size: 40px;     
 } 
 h3{
     font-size: 18px;
 }
 
 } 
</style>