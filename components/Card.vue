<template>
  <v-card
    v-bind="card"
  >
    <v-container>
      <v-card-title :class="name.typography" :color="name.color">{{name.text}}</v-card-title>
      <v-card-text :class="subheading.typography" :color="subheading.color">{{subheading.text}}</v-card-text>
      <v-card-actions>
        <v-btn
          v-for="button in buttons"
          :key="button.route"
          tile
          outlined
          :color="button.color"
          class="ma-1"
          :href="button.href"
          :target="button.target"
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
        elevation: 0,
        color: "transparent"
      },
      name: {
        text: `Ray Truong.`,
        typography: 'display-3 font-weight-thin',
        color: 'primary'
      },
      subheading: {
        text: 'Computer Science Student & Denim Snob',
        typography: 'subtitle-2 font-weight-light',
        color: 'primary'
      },
      buttons: [
        {
          text: 'journal',
          color: 'primary',
          route: 'entries'
        },
        {
          text: 'portfolio',
          color: 'primary',
          route: 'portfolio'
        },
        {
          text: 'resume',
          color: 'primary',
          href: '/resume.pdf',
          target: '_blank'
        }
      ],
      media: [
        {
          icon: ['fa', 'envelope'],
          color: 'primary',
          link: 'mailto:ray@raytruong.dev',
          target: '_blank'
        },
        {
          icon: ['fab', 'github-alt'],
          color: 'primary',
          link: 'https://www.github.com/raytruong',
          target: '_blank'
        },
        {
          icon: ['fab', 'linkedin-in'],
          color: 'primary',
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
