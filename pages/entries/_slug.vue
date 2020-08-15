<template>
  <v-container>
    <div>
      <component :is="entryComponent" />
    </div>
  </v-container>
</template>
<script>
export default {
  layout: 'entry',
  async asyncData({ params }) {
    try {
      let entry = await import(`~/entries/${params.slug}.md`);
      return {
        title: entry.attributes.title,
        date: entry.attributes.date,
        entryComponent: entry.vue.component
      };
    } catch (err) {
      return false;
    }
  }
};
</script>
