<template>
<div app>

  <v-app-bar 
    app
    >
      <v-app-bar-nav-icon class="hidden-sm-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-sm-and-down">
      <v-btn text>
        <span>INICIO</span>
      </v-btn>

      <v-btn text>
        link
        <!-- <span>Prueba</span>
        <v-icon>expand_more</v-icon> -->
      </v-btn>

      <v-btn text>
        <span>Prueba</span>
        <v-icon>expand_more</v-icon>
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
          <v-list-item-title class="title">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
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
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

        </div>
</template>

<script>
  export default {
    name: 'Toolbar',

    data: () => ({
      drawer: null,
      items: [
          { title: 'Dashboard', icon: 'dashboard' },
          { title: 'Photos', icon: 'image' },
          { title: 'About', icon: 'help' },
        ],
        right: null,
      }),
  }
</script>
