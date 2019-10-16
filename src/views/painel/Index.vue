<template>
<div>
  <!-- card -->
  <v-card>
    <v-navigation-drawer
      expand-on-hover
      permanent
      relative
    >
    <!-- dentro do card -->
      <template v-slot:prepend>
        <!-- lista -->
        <v-list>
          <!-- itens da lista -->
          <v-list-item>
            <!-- intens da lista: avatar -->
            <v-list-item-avatar>
              <!-- avatar tem a cor amarela -->
              <v-avatar color="red">
                <!-- dentro dessa cor há um escrito em branco "AD" -->
                <span class="white--text headline">AL</span>
              </v-avatar>
            </v-list-item-avatar>
          </v-list-item>

          <v-list-item
            link
            two-line
          >
            <v-list-item-content>
              <!-- título da lista -->
              <v-list-item-title class="title">Bem-vindo de volta!</v-list-item-title>
              <!-- subtítulo -->
              <!-- nome que aparece no login -->
              <v-list-item-subtitle>{{ user.nome }}</v-list-item-subtitle>
            </v-list-item-content>
            <!-- ações da lista -->
            <v-list-item-action>
              <!-- [icone] -->
              <v-icon>mdi-menu-down</v-icon>
            </v-list-item-action>
          </v-list-item>
        </v-list>
        
      </template>

      <v-divider></v-divider>

      <v-list
        nav
        dense
      >
      <!-- item da lista com link -->
        <v-list-item link>
          <!-- ícone -->
          <v-list-item-icon>
            <v-icon @click="manut" color="black">mdi-rocket</v-icon>
          </v-list-item-icon>
          <!-- escrito ao lado do ícone, um título -->
          <v-list-item-title @click="manut">Inscritos Hackathon</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <!-- ícone com links -->
            <v-icon @click="usuario" color="black">mdi-account-multiple</v-icon>
          </v-list-item-icon>
          <!-- o @click é um evento, dentro dele há o método que é o caminho aonde ele irá  percorrer -->
          <v-list-item-title @click="usuario">Administradores</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon @click="sair" color="black">mdi-location-exit</v-icon>
          </v-list-item-icon>
          <v-list-item-title @click="sair">Sair</v-list-item-title>
        </v-list-item>

  
      </v-list>
    </v-navigation-drawer>
  
 
  </v-card>

  
    <!-- imagens -->  
  <template>
    <!-- container fluído -->
  <v-container fluid>
    <v-row>
      <!-- v-col para as colunas, no tamanho desktop elas terão de ocupar 6, no tamanho mobile 4 -->
      <v-col cols="6" sm="4">
        <!-- o v-img permite que importemos imagens -->
        <v-img
          src="https://cdn.pixabay.com/photo/2016/03/26/13/09/cup-of-coffee-1280537__340.jpg"
          gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
        ></v-img>
      </v-col>

      <v-col cols="6" sm="4">
        <v-img src="https://cdn.pixabay.com/photo/2018/05/04/10/30/team-3373638__340.jpg">
          <div class="fill-height bottom-gradient"></div>
        </v-img>
      </v-col>

      <v-col cols="6" sm="4">
        <v-img src="https://cdn.pixabay.com/photo/2015/01/08/18/27/startup-593341__340.jpg">
          <div class="fill-height repeating-gradient"></div>
        </v-img>
      </v-col>
    </v-row>
    
  </v-container>
  
  <!-- final do cartão de alerta -->
</template>
<!-- template das imagens -->
  

</div>

</template>
<style>

</style>
<script>
// os métodos são os caminhos que cada propriedade click irá nos levar
export default {
   computed: {
    user () {
      return this.$ls.get('user')
    }
  },
// o método sair irá em router e chamará pelo caminho /painel/login e assim por diante
  methods:{
    sair(){
      this.$router.push('/painel/login')
    },
    usuario(){
      this.$router.push('/painel/usuarios')
    },
    manut(){
      this.$router.push('/painel/inscritos')
    }

  },
   data () {
      return {
        alert: true,
      }
    },
}
</script>

