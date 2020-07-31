<template>
  <div class="mt-5">
    <v-container>
      <v-row>
        <v-col
        v-for="(item, index) in items"
        :key="index"
        cols="12" md="3"
        >
          <v-card
            class="mx-auto"
             max-height=""

          >
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title class="headline">{{
                  item.name
                }}</v-list-item-title>
                <v-list-item-subtitle>{{ item.subtitle }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>

            <v-img 
            :src="item.img" 
            class="mx-5"
            >
            </v-img>

            <v-card-text
            height="400"
            >
              {{ item.description }}
            </v-card-text>

            <v-card-actions>
              <v-btn text color="#5ae4a7">
                Saber más
              </v-btn>
            </v-card-actions>
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
      <v-card-title color="#5ae4a7">
        <strong class="subheading">Get connected with us on social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          dark
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>{{ codeweb }}</strong>
      </v-card-text>
    </v-card>
  </v-footer>
  </div>
</template>

<script>
export default {
  name: "Team",

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
          name: "David Pérez",
          subtitle: "Desarrollador Web",
          img: require("@/../public/page.png"),
          description: 'Experimentado en desarrollo web, con tecnologias como Javascript, html5, css6, Vue Js entre otras tecnologias modernas para el desarrllo escalable de las aplicaciones'
        },
        {
          name: "Melanie de Martinez",
          subtitle: "Diseño Grafico",
          img: require("@/../public/diseno.png"),
          description: 'Trayectoria y experiencia en trabajos para publicidad y diseño de marca, excelente en el manejo de herramientas como Photoshop e Illustrator'
        },
        {
          name: "Valentin Herrera",
          subtitle: "Analista de datos",
          img: require("@/../public/engineer.png"),
          description: 'Cientifico de datos con experiencia en trabajos para diferentes empresas, usando tecnologias actuales y lenguajes de programacion como Python'
        },
        {
          name: "Angelica Martinez",
          subtitle: "Marketing Digital",
          img: require("@/../public/engineer.png"),
          description: 'Especialista en crecimiento organico y SEO con estrategias tacticas modernas para un mejor rendimiento, con el uso de herramientas de medicion y analitica web'
        }
      ],
    };
  },
};
</script>

<style scoped>
    
</style>