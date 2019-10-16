<template>
  <v-footer
    color="blue-grey darken-2"
    padless
    
  >
    <v-row
      justify="center"
      no-gutters
      
    >
     <v-icon
       color="white"
        class="my-2"
      >
        mdi-email
      </v-icon>
      <v-icon
       color="white"
        class="my-2"
      >
        mdi-facebook-box
      </v-icon>
       <v-icon
       color="white"
        class="my-2"
      >
        mdi-github-box
      </v-icon>
       <v-icon
       color="white"
        class="my-2"
      >
        mdi-twitter-box
      </v-icon>
      
      <v-col
      
        class="blue-grey darken-3 py-4 text-center white--text"
        cols="12"
        
        
      >
      <v-list-item-title>Av. General Joaquim nº1627, Centro - Taquaritinga-SP</v-list-item-title>
      
        {{ new Date().getFullYear() }} — <strong>DOCTYPE</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
  export default {

  }
</script>