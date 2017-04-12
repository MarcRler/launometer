<template>
  <v-ons-navigator :page-stack="pageStack">
    <component :is="page" v-for="page in pageStack" :page-stack="pageStack"></component>
  </v-ons-navigator>
</template>

<script>
  import start from 'startScreen';
  import page2 from 'Page2';

  export default {
    data() {
      return {
        pageStack: [start]
      }
    }
  }
</script>
