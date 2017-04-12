<template>
  <v-ons-page>
    <custom-toolbar>Launometer</custom-toolbar>
    <v-ons-list>
        <v-ons-list-header></v-ons-list-header>
        <!--Login-Bereich-->
            <div style="text-align: center; margin-top: 30px;" class="center">
                <p><v-ons-input type="text" placeholder="Nutzername" float modifier="underbar"></v-ons-input></p>
                <p><v-ons-input type="password" placeholder="Passwort" float modifier="underbar"></v-ons-input></p>
                <p><v-ons-button @click="push"> Einloggen</v-ons-button></p>
            </div>
        <!--Registrieren-->
        <v-ons-list-header></v-ons-list-header>
    </v-ons-list>
  </v-ons-page>
</template>

<script>
  import customToolbar from 'customToolbar';
  import page2 from 'Page2';
  export default {
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(page2);
       }
     },
     props: ['pageStack'],
     components: { customToolbar }
  }
</script>
