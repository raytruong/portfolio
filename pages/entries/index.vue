<template>
  <v-container>
      <v-card
          v-for="entry in entries"
          flat
          color="transparent"
          :key="entry.attributes.title"
      >
        <v-card-title
            class="text-decoration-underline"
        >
          <v-btn
              elevation="0"
              color="transparent"
              class="hover-btn"
              :ripple="false"
              nuxt
              :to="getPermalink(entry)"
          >
          {{entry.attributes.title}}
          </v-btn>
      </v-card-title>
      <v-card-subtitle class="ml-4">{{entry.attributes.date}}</v-card-subtitle>
    </v-card>
  </v-container>
</template>

<script>
export default {
  layout: 'blog',
  async asyncData() {
    const resolve = require.context("~/entries/", true, /\.md$/);
    const imports = resolve.keys().map(key => {
      const [, name] = key.match(/\/(.+)\.md$/);
      return resolve(key);
    });
    return {
      entries: imports
    };
  },
  data() {
    return {
      prefix: 'entries',
      data () {
        return {
          card: {
            flat: true,
            tile: true,
            color: "transparent",
          }
        }
  }
    }
  },
  methods: {
    getPermalink(post) {
        return  `${this.prefix}/${post.meta.resourcePath.split('\\').pop().split('/').pop().split('.')[0]}`;
    }
  }
};
</script>

<style scoped>
.hover-btn::before {
  background-color: transparent
}
</style>
