<template>
  <v-card
    flat
    tile
    color="transparent"
  >
    <v-container>
      <v-card-title class="display-2 font-weight-thin">{{name}}</v-card-title>
      <v-card-text class="subtitle-2 font-weight-thin">{{subheading}}</v-card-text>
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
      <v-card-actions>
        <v-btn
          v-for="button in media"
          :key="button.icon"
          class="mx-3"
          :href="button.link"
          :target="button.target"
          text
        >
          <font-awesome-icon :icon="button.icon" :color="button.color" style="font-size: 18px" />
        </v-btn>
      </v-card-actions>
    </v-container>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      name: `Ray Truong`,
      subheading: 'Software Engineer & Yappie',
      buttons: [
        {
          text: 'blog',
          color: '#' + 'primary',
          route: 'blog'
        },
        {
          text: 'portfolio',
          color: '#' + 'primary',
          route: 'portfolio'
        },
        {
          text: 'resume',
          color: '#' + 'primary',
          href: '/resume.pdf',
          route: ''
        }
      ],
      media: [
        {
          icon: ['fa', 'envelope'],
          color: "white",
          link: 'mailto:ray@raytruong.dev',
          target: '_blank'
        },
        {
          icon: ['fab', 'github-alt'],
          color: "white",
          link: 'https://www.github.com/raytruong',
          target: '_blank'
        },
        {
          icon: ['fab', 'linkedin-in'],
          color: "white",
          link: 'https://www.linkedin.com/in/ray-truong',
          target: '_blank'
        }
      ]
    }
  }
}
</script>

<style>

</style>
