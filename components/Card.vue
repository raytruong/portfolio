<template>
  <v-card
    v-bind="card"
  >
    <v-container>
      <v-card-title :class="card.name_typography">{{card.name}}</v-card-title>
      <v-card-text :class="card.subheading_typography">{{card.subheading}}</v-card-text>
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
          class="mx-5"
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
      card: {
        name: `Ray Truong.`,
        name_typography: 'display-3 font-weight-light',
        subheading: 'Software Engineer & Yappie',
        subheading_typography: 'subtitle-2 font-weight-light justify-center',
        elevation: 0,
        color: "transparent"
      },
      buttons: [
        {
          text: 'journal',
          color: '#' + 'primary',
          route: 'journal'
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
          route: '/resume.pdf'
        }
      ],
      media: [
        {
          icon: ['fa', 'envelope'],
          color: '#' + 'primary',
          link: 'mailto:ray@raytruong.dev',
          target: '_blank'
        },
        {
          icon: ['fab', 'github-alt'],
          color: '#' + 'primary',
          link: 'https://www.github.com/raytruong',
          target: '_blank'
        },
        {
          icon: ['fab', 'linkedin-in'],
          color: '#' + 'primary',
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
