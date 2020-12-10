<template>
  <v-app>
    <v-app-bar flat app color="secondary">
      <v-app-bar-nav-icon
        color="primary"
        v-if="$vuetify.breakpoint.xsOnly"
        @click.stop="drawer = !drawer"
      >
      </v-app-bar-nav-icon>
      <v-toolbar-title>
        <v-img contain height="32" src="./assets/logo.png"></v-img>
      </v-toolbar-title>
      <v-spacer />
      <v-toolbar-items v-if="$vuetify.breakpoint.smAndUp">
        <v-btn text>Услуги и цены</v-btn>
        <v-btn text>Акции</v-btn>
        <v-btn text>О компании</v-btn>
        <v-btn text>Контакты</v-btn>
      </v-toolbar-items>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute bottom temporary>
      <v-list nav dense>
        <v-list-item-group>
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <h1>Hello</h1>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'App',

  components: {
  },

  data: () => ({
    drawer: false
  })
})
</script>
