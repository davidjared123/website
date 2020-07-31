<template>
  <div class="mt-5">
    <v-container>
      <v-row>
        <v-col
        v-for="(item, index) in items"
        :key="index"
        >
          <v-card
            max-width="344"
            class="mx-auto"

          >
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title class="headline">{{
                  item.name
                }}</v-list-item-title>
                <v-list-item-subtitle>{{ codeweb }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>

            <v-img 
            :src="item.img" 
            class="mx-5"
            >
            </v-img>

            <v-card-text>
              Visit ten places on our planet that are undergoing the biggest
              changes today.
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
  </div>
</template>

<script>
export default {
  name: "Services",

  data: () => {
    return {
        codeweb: '<CodeWeb/>',
      items: [
        {
          name: "Desarrollo web",
          img: require("@/../public/page.png"),
        },
        {
          name: "Diseño Grafico",
          img: require("@/../public/diseno.png"),
        },
        {
          name: "Analisis de datos",
          img: require("@/../public/engineer.png"),
        },
        {
          name: "Diseño de Logo",
          img: require("@/../public/logo.png"),
        },
        {
          name: "Marketing",
          img: require("@/../public/marketing.png"),
        },
        {
          name: "Mantenimiento Web",
          img: require("@/../public/mantenimiento.png"),
        },
      ],
    };
  },
};
</script>

<style scoped>
    
</style>