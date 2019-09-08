<template>
  <v-layout fill-height column justify-center align-center>
    <blockquote class="blockquote">
      {{ quote }}
      <footer>
        <small>
          <em>&mdash;{{ author }}</em>
        </small>
      </footer>
    </blockquote>
    <v-btn tile outlined color="primary" class="ma-1" nuxt to="/">/</v-btn>
  </v-layout>
</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {
      quote: "",
      author: ''
    };
  },
  async created() {
    let res = await axios.get('api');
    this.quote = res.data.text;
    this.author = res.data.source;
  }
};
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
