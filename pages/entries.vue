<template>
  <v-container>
      <v-card
          v-for="entry in entries"
          v-bind="card"
          :key="entry.key"
      >
        <v-card-title
            class="text-decoration-underline"
        >
          <v-btn
          elevation="0"
          color="transparent"
          class="hover-btn"
          :ripple="false"
          >
          {{entry.title}}
          </v-btn>
      </v-card-title>
      <v-card-subtitle class="ml-4">{{entry.date}}</v-card-subtitle>
    </v-card>
</v-container>
</template>

<script>
let entries = []
entries.push({
  key: 0,
  title: 'Under Construction',
  date: '7.28.20'
})
export default {
  layout: 'blog',
  data () {
    return {
      card: {
        flat: true,
        tile: true,
        color: "transparent",
      },
      entries: entries
    }
  }
}
</script>

<style scoped>
.hover-btn::before {
  background-color: transparent
}
</style>
