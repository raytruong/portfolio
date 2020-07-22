<template>
  <v-layout
    fill-height
    column
    justify-center
    align-center
  >
  <v-card
    v-bind="card"
  >
    <v-container>
      <v-card-title :class="card.subheading_typography">{{card.subheading}}</v-card-title>
      <v-card-actions>
        <v-btn
          v-for="button in buttons"
          :key="button.route"
          tile
          outlined
          :color="button.color"
          class="ma-1"
          :href="button.href"
          nuxt
          :to="button.route"
        >
          {{button.text}}
        </v-btn>
      </v-card-actions>
    </v-container>
  </v-card>
  </v-layout>
</template>

<script>
export default {
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  data () {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred',
      card: {
        subheading: '404',
        subheading_typography: 'subtitle font-weight-light justify-center',
        color: "transparent",
        elevation: 0
      },
      buttons: [
        {
          text: 'home',
          color: '#' + 'primary',
          route: '/'
        }
      ],
    }
  },
  head () {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title
    }
  }
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
