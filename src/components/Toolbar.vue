<template>
<div app>

  <v-app-bar 
    app
    >
      <v-app-bar-nav-icon class="hidden-sm-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>
        <v-img src="@/../public/codeweb.png" aspect-ratio="4.7" width="150px"></v-img>
      </v-toolbar-title>

      <v-spacer></v-spacer>
      <!-- menu -->

      <v-toolbar-items class="hidden-sm-and-down">
      <v-btn 
      text
      to="/"
      >
        <span>INICIO</span>
      </v-btn>


      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }" class="bg">
        <v-btn 
        flat
        text
        v-bind="attrs"
        v-on="on"
        >
          <v-icon left>expand_more</v-icon>
          <span>SERVICIOS</span>
        </v-btn>
        </template>

        <v-list>
          <v-list-item 
          v-for="(item, index) in servicios" :key="index" 
          router :to="item.route"
          class="width ">
            <v-list-item-title>{{item.title}}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>

      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }" class="bg">
        <v-btn 
        flat
        text
        v-bind="attrs"
        v-on="on"
        >
          <v-icon left>expand_more</v-icon>
          <span>Nosotros</span>
        </v-btn>
        </template>

        <v-list>
          <v-list-item 
          v-for="(item, index) in nosotros" :key="index" 
          router :to="item.route"
          class="width ">
            <v-list-item-title>{{item.title}}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>

      <v-btn 
      text
      to="contacto"
      >
        <span>contacto</span>
      </v-btn>

      </v-toolbar-items>
    </v-app-bar>

  <!-- drawer -->

<v-navigation-drawer 
  v-model="drawer"
  absolute
  temporary
>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title ml-7">
            <v-img src="@/../public/codeweb.png" aspect-ratio="4.7" width="160px"></v-img>
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          :to="item.route"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

      <v-list-group
        v-for="item in drawerItems"
        :key="item.title"
        v-model="item.active"
        :prepend-icon="item.action"
        no-action
      >
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title v-text="item.title"></v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item
          v-for="subItem in item.items"
          :key="subItem.title"
          :to="subItem.route"
        >
          <v-list-item-content>
            <v-list-item-title v-text="subItem.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>
    

      </v-list>
    </v-navigation-drawer>

        </div>
</template>

<script>
  export default {
    name: 'Toolbar',

    data: () => ({
      drawer: null,

      drawerItems: [
          {
            action: 'design_services',
            title: 'SERVICIOS',
            items: [
              {title: 'Diseño Web', route: '/desarrollo-web'},
              {title: 'Landing Pages', route: '/landing-page' },
              {title: 'Analisis de datos', route: '/analisis-de-datos' },
              {title: 'Diseño de Marca', route: '/diseño-de-marca' },
              {title: 'Diseño Grafico', route: '/diseño-grafico' },
              {title: 'Marketing digital', route: '/marketing' }
            ],
          },
          {
            action: 'group',
            title: 'NOSOTROS',
            items: [
              {title: "Nuestro equipo", route: '/equipo'},
              {title: "Portafolio", route: 'portafolio'},
            ],
          },
        ],



      items: [
          { title: 'INICIO', icon: 'home', route: '/' },
          { title: 'CONTACTO', icon: 'call', route: '/contacto' },
        ],
        servicios: [
          {title: 'Desarrollo web', route: '/desarrollo-web' },
          {title: 'Analisis de datos', route: '/analisis-de-datos' },
          {title: 'Landing Pages', route: '/landing-page' },
          {title: 'Diseño de Marca', route: '/diseño-de-marca' },
          {title: 'Diseño Grafico', route: '/diseño-grafico' },
          {title: 'Marketing digital', route: '/marketing' }
        ],
        nosotros: [
         {title: "Nuestro equipo", route: '/equipo'},
         {title: "Portafolio", route: 'portafolio'},
        ],

        right: null,
      }),
  }
</script>

<style scoped>
    .width{
      text-align: right;
    }
</style>