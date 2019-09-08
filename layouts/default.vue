<template>
  <v-app :style="{background: $vuetify.theme.themes[theme].background}">
    <v-footer color="transparent">
      <v-btn
        v-for="button in media"
        :key="button.icon"
        class="mx-3"
        :href="button.link"
        :target="button.target"
        text
      >
        <font-awesome-icon :icon="button.icon" color="white" style="font-size: 18px" />
      </v-btn>
    </v-footer>
    <v-content>
      <nuxt />
    </v-content>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      media: [
        {
          icon: ['fab', 'github'],
          link: 'https://www.github.com/raytruong',
          target: '_blank'
        },
        {
          icon: ['fab', 'linkedin'],
          link: 'https://www.linkedin.com/in/ray-truong',
          target: '_blank'
        },
        {
          icon: ['fas', 'envelope'],
          link: 'mailto:rtruong@purdue.edu',
          target: '_blank'
        }
      ]
    };
  },
  computed: {
    theme() {
      return this.$vuetify.theme.dark ? 'dark' : 'light';
    }
  }
};
</script>

<style>
.v-application {
  font-family: 'Overpass', sans-serif;
}
</style>
