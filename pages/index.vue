<template>
  <v-layout fill-height column justify-center align-center>
    <v-card tile flat color="transparent">
      <v-container>
        <v-card-title class="display-2 font-weight-thin">{{name}}</v-card-title>
        <v-card-text class="subtitle-2 font-weight-thin">{{subheading}}</v-card-text>
        <!-- <blockquote class="blockquote">
          <small>&#8220;{{quote}}&#8221;</small>
          <footer>
            <small>
              <em>&mdash;{{author}}</em>
            </small>
          </footer>
        </blockquote>-->
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
          >{{button.text}}</v-btn>
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
            <font-awesome-icon :icon="button.icon" color="white" style="font-size: 18px" />
          </v-btn>
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
      name: `|`,
      subheading: 'Software Engineer & Patagonia Enthusiast',
      buttons: [
        {
          text: 'about',
          color: '#' + 'primary',
          route: 'about'
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
      quote: `Do you think... God stays in heaven because he too lives in fear of what he's created, here on Earth?`,
      author: 'Dr. Romero, Spy Kids 2',
      media: [
        {
          icon: ['fa', 'envelope'],
          link: 'mailto:ray@raytruong.dev',
          target: '_blank'
        },
        {
          icon: ['fab', 'github-alt'],
          link: 'https://www.github.com/raytruong',
          target: '_blank'
        },

        {
          icon: ['fab', 'linkedin-in'],
          link: 'https://www.linkedin.com/in/ray-truong',
          target: '_blank'
        }
      ]
    };
  },
  created() {
    //Refactor later with function currying ;)
    setTimeout(() => {
      this.name = '|';
      setTimeout(() => {
        this.name = 'R|';
        setTimeout(() => {
          this.name = 'Ra|';
          setTimeout(() => {
            this.name = 'Ray|';
            setTimeout(() => {
              this.name = 'Ray |';
              setTimeout(() => {
                this.name = 'Ray T|';
                setTimeout(() => {
                  this.name = 'Ray Tr|';
                  setTimeout(() => {
                    this.name = 'Ray Tru|';
                    setTimeout(() => {
                      this.name = 'Ray Truo|';
                      setTimeout(() => {
                        this.name = 'Ray Truon|';
                        setTimeout(() => {
                          this.name = 'Ray Truong|';
                          let blink = false;
                          setInterval(() => {
                            blink = !blink;
                            blink ? (this.name = 'Ray Truong') : (this.name = 'Ray Truong|');
                          }, 900);
                        }, 200);
                      }, 100);
                    }, 100);
                  }, 100);
                }, 100);
              }, 100);
            }, 100);
          }, 100);
        }, 100);
      }, 300);
    }, 500);
  },
  computed: {}
};
</script>
