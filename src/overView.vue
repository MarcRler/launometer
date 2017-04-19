<template>
  <v-ons-page>
    <custom-toolbar>Launometer</custom-toolbar>
    <v-ons-list>
      <v-ons-list-header>Notifications</v-ons-list-header>
      <v-ons-list-item
        tappable
        @click="$ons.notification.alert('Hello, world!')"
        >
        <div class="center">
          Alert
        </div>
      </v-ons-list-item>
      <v-ons-list-item
        tappable
        @click="$ons.notification.confirm('Are you ready?')"
        >
        <div class="center">
          Confirmation
        </div>
      </v-ons-list-item>
      <v-ons-list-item
        tappable
        @click="$ons.notification.prompt('What is your name?')"
        >
        <div class="center">
          Prompt
        </div>
      </v-ons-list-item>
    </v-ons-list>
  </v-ons-page>
</template>

<script>
  import customToolbar from 'customToolbar';
  import app from 'App';

  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      } 
    },
    props: ['pageStack'],
    components: { customToolbar }
  }
</script>


