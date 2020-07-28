<template>
  <v-container v-bind="container">
      <v-card v-for="entry in entries" :key="entry.key" v-bind="card">
        <v-card-title class="text-decoration-underline">{{entry.title}}</v-card-title>
        <v-card-subtitle>{{entry.date}}</v-card-subtitle>
      </v-card>
  </v-container>
</template>

<script>
export default {
  layout: 'blog',
  data () {
    return {
      container: {
      },
      card: {
        flat: true,
        tile: true,
        color: "transparent"
      },
      entries: [
        {
          title: "Still under construction...",
          date: "",
          key: 0
        }
      ]
    }
  }
}
</script>

<style scoped>
.v-container {
  max-width: 200px
}

</style>
