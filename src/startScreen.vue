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
        <div style="text-align: center; margin-top: 30px;" class="center">
            <p><v-ons-button modifier="outline" style="margin: 6px 0">Mit Google registrieren</v-ons-button></p>
            <p><v-ons-button modifier="outline" style="margin: 6px 0">Mit Facebook registrieren</v-ons-button></p>
            <p><v-ons-button modifier="outline" style="margin: 6px 0">Neuen Account erstellen</v-ons-button></p>
        </div>
    </v-ons-list>
  </v-ons-page>
</template>

<script>
  import customToolbar from 'customToolbar';
  import overView from 'overView';
  export default {
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(overView);
       }
     },
     props: ['pageStack'],
     components: { customToolbar }
  }
</script>
