<template>
  <v-card height="150"
  class="black">
 
  
    <v-footer
      absolute
      class="font-weight-regular white--text black"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>&lt;!Doctype&gt;</strong>
      
      </v-col>
      <v-col
      class="text-center"
        cols="12"
      >
       <i class="fab fa-facebook-square"></i> <i class="fab fa-github-square"></i> <i class="fab fa-twitter-square"></i> 
      </v-col>
    </v-footer>
  </v-card>
</template>
<style  scoped>
i{
  color:white;
  margin:10px;
  font-size: 33px;
}
</style>