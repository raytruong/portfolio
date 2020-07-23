<template>
  <v-app>
    <v-app-bar v-bind="bar">
      <v-container>
        <v-layout justify-end>
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
    <v-content>
        <nuxt />
    </v-content>
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
        title_text: 'Ideas worth keeping to yourself',
        buttons: [
          {
            text: 'entries',
            color: 'primary',
            route: 'entries'
          },
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
