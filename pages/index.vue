<template>
  <v-app app>
    <v-card
      color="grey lighten-4"
      dense
    >
      <v-toolbar  >
        <v-app-bar-nav-icon  @click.stop="drawer = !drawer" ></v-app-bar-nav-icon>

        <v-toolbar-title>Mi App</v-toolbar-title>

        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn text>Inicio</v-btn>
          <v-btn text>Buscar</v-btn>
          <v-btn text>Acerca de</v-btn>
        </v-toolbar-items>
      </v-toolbar>
      <v-navigation-drawer
      v-model="drawer"
      absolute
      bottom
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="white--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Inicio</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buscar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Acerca de</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

  </v-card>
    <v-main>
      <v-container>
        <Home />
      </v-container>
    </v-main>

  </v-app>
</template>
<script>
export default {
  
  name: "App",
  data: () => ({
    drawer: false,
    group: null,
  }),

  watch: {
    group () {
      this.drawer = false
    },
  },
};
</script>