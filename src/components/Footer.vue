<template>
  <div>
    <v-container fluid class="bg">
      <v-row align="center">
        <!-- <v-col cols='12' align="center" class="mb-0 pb-0">
            <v-img
                src="@/../public/codeweb.png"
                aspect-ratio="4.7" 
                max-width="450px" 
                class="mt-5"
            >
            </v-img>
        </v-col>-->
        <v-col cols="12" md="12" class="text-center py-14">
          <h1>Comienza a crear tu presencia web</h1>
          <p>
            Disfruta al iniciar tu negocio online desde cero
            <b>Nosotros</b> te ayudamos
          </p>
          <v-btn color="#5ae4a7">Comenzar</v-btn>
        </v-col>
      </v-row>
    </v-container>


<v-footer
    color="#5ae4a7"
  >
  <v-row 
  justify="center"
  >
    <v-card
      flat
      tile
      class=" white--text text-center p"
      color="#5ae4a7"

    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0 text-center" >
       Empresa orientada a la elaboracion y creacion de paginas web, diseño grafico de contenido digital para redes sociales y paginas web.
       <br/>
        Diseño de marca "logo" y marketing digital para el crecimiento SEM y organico de las empresas. 
       <br/>
       Creada y ubicada en Venezuela, cuenta con personas experimentadas en cada area para una mejor calidad de servicio.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        <p><strong>{{ codeweb }}</strong></p>
        <b>Desde el 2020</b>
      </v-card-text>
    </v-card>
    </v-row>
  </v-footer>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data: () => {
    return {
        codeweb: '<CodeWeb/>',
        icons: [
        'facebook',
        'email',
        'phone',
      ],
    };
  },
};
</script>

<style scoped>
.bg {
  background-color: #f5f5f573;
}
h1 {
  font-size: 65px;
  font-weight: 300;
}
p {
  font-size: 25px;
  font-weight: 300;
}
.v-btn {
  color: rgba(255, 255, 255, 0.932);
}

@media (max-width: 1040px) {
  h1 {
    font-size: 54px;
  }
  p {
    font-size: 20px;
  }
}

@media (max-width: 800px) {
  h1 {
    font-size: 44px;
  }
  p {
    font-size: 20px;
  }
}
</style>