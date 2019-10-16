<template>
  <v-app>
    <app-header/>
    <router-view />
    <app-footer/>
    
  </v-app>
</template>

<script>
import AppFooter from './components/AppFooter'
import AppHeader from './components/AppHeader'
import estilo from './css/estilo.css'
export default {
  name: 'App',
  components:{
    AppFooter, AppHeader,
  },
  css:{
    estilo,
  }
}
</script>
