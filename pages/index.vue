<template>
  <v-layout fill-height column justify-center align-center>
    <v-card tile flat color="transparent">
      <v-container>
        <v-card-title class="display-3 font-weight-thin">{{name}}</v-card-title>
        <v-card-text class="subtitle-2 font-weight-thin">{{subheading}}</v-card-text>
        <blockquote class="blockquote">
          <small>&#8220;{{quote}}&#8221;</small>
          <footer>
            <small>
              <em>&mdash;{{author}}</em>
            </small>
          </footer>
        </blockquote>
        <v-card-actions>
          <v-btn
            v-for="button in buttons"
            :key="button.route"
            tile
            outlined
            :color="button.color"
            class="ma-1"
            nuxt
            :to="button.route"
          >{{button.text}}</v-btn>
        </v-card-actions>
      </v-container>
    </v-card>
  </v-layout>
</template>

<script>
import axios from 'axios';
export default {
  data: function() {
    return {
      name: `Raymond Truong`,
      subheading: 'Software Engineer',
      buttons: [
        {
          text: 'portfolio',
          color: '#' + 'primary',
          route: 'portfolio'
        },
        {
          text: 'resume',
          color: '#' + 'primary',
          route: 'resume'
        },
        {
          text: 'contact',
          color: '#' + 'primary',
          route: 'contact'
        }
      ],
      quote: `Do you think... God stays in heaven because he too lives in fear of what he's created, here on Earth?`,
      author: 'Dr. Romero, Spy Kids 2'
    };
  }
};
</script>
