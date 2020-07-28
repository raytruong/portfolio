<template>
  <v-app>
    <v-app-bar v-bind="bar">
      <v-container>
        <v-layout justify-end>
          <v-btn
              tile
              elevation="0"
              color="transparent"
              class="ma-1"
              nuxt
              :to="entries"
          >
          {{bar.title_text}}
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn
              v-for="button in bar.buttons"
              :key="button.route"
              tile
              outlined
              :color="button.color"
              class="ma-1"
              nuxt
              :to="button.route"
          >
          {{button.text}}
          </v-btn>
        </v-layout>
      </v-container>
    </v-app-bar>
    <v-main>
        <nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      bar: {
        app: true,
        color: 'transparent',
        elevation: 0,
        title_text: 'ray\'s journal',
        buttons: [
          {
            text: 'home',
            color: 'primary',
            route: '/',
          }
        ]
      }
    }
  }
}
</script>

<style>
.container {
  max-width: 700px
}
</style>
