<template>
  <div>
    <v-data-table
      :headers="headers"
      :items="desserts"
      :page.sync="page"
      :items-per-page="itemsPerPage"
      hide-default-footer
      class="elevation-1"
      @page-count="pageCount = $event"
    ></v-data-table>
    <div class="text-center pt-2">
      <v-pagination v-model="page" :length="pageCount"></v-pagination>
      <v-text-field
        :value="itemsPerPage"
        label="Items per page"
        type="number"
        min="-1"
        max="15"
        @input="itemsPerPage = parseInt($event, 11)"
      ></v-text-field>
    </div>
    <!-- botão para voltar -->
    <v-container fluid>
     <!-- centralizado -->
     <div class="text-center">
       <!-- evento click -->
    <v-btn @click="painel"
    color="cyan"
    >  <!--essa flecha antes é a de fechadura do v-btn =D -->
    Voltar
    </v-btn>
    
    </div>
  </v-container>
  <!-- final do botão -->
  </div>
</template>
<script>
  export default {
    data () {
      return {
        page: 1,
        pageCount: 0,
        itemsPerPage: 11,
        headers: [
          {
            text: 'Inscritos Hackathon (2019)',
            align: 'left',
            sortable: false,
            value: 'name',
          },
        { text: 'Idade', value: 'idade' },
        { text: 'Emprego/Curso', value: 'emprego' },
        { text: 'E-mail', value: 'email' },
        { text: 'Telefone', value: 'tel' },
        { text: 'Cidade', value: 'cid' },
        ],
        desserts: [
          {
            name: 'GEORDANA BEATRIZ SOUZA DE KÁSSIO',
            idade:'17',
            emprego:'Analise e Desenvolvimento de Sistemas',
            email:'geordana.kassio@outlook.com',
            tel:'(16)99125-6178',
            cid:'Taquaritinga-SP'
            
          },
          {
            name: 'EVELYN DA SILVA ROMANOVA',
            idade:'20',
            emprego:'Back-end Developer Pleno',
            email:'evy.romanova@gmail.com',
            tel:'(16)99125-6178',
            cid:'Guariba-SP'
            
          },
          {
            name: 'ESDRAS ARTHUR DA SILVA OLIVEIRA',
            idade:'21',
            emprego:'UI/UX Designer',
            email:'esdras.oliveiraEASO@gmail.com',
            tel:'(16)99125-6178',
            cid:'(16)99125-6178'
          },
          {
            name: 'CARLOS EMANUEL SANTOS',
            idade:'26',
            emprego:'Fullstack Developer',
            email:'carlos.santosE7@gmail.com',
            tel:'(16)99125-6178',
            cid:'Monte Alto'
          },
          
          {
            name: 'KAMILA YASMIN DAMIÃO',
            idade:'23',
            emprego:'PHP Developer',
            email:'kamilayasmin.damiao@gmail.com',
            tel:'(16)99125-6178',
            cid:'Matão-SP'
          },
          {
            name: 'GUILHERME HOTARU PECCHI',
           idade:'18',
            emprego:'Sistemas para Internet',
            email:'guilherme.hotaru.pecchi@gmail.com',
            tel:'(16)99125-6178',
            cid:'Jaboticabal-SP'
          },
          {
            name: 'JULYA DANDARIO PINTO FONSECA',
            idade:'30',
            emprego:'Data Base Analytics Sênior',
            email:'julya@contato.com',
            tel:'(16)99125-6178',
            cid:'Taquaritinga-SP'
          },
          {
            name: 'ARIADNE SILVESTRINE PECCHI',
            idade:'20',
            emprego:'Sistemas para Internet',
            email:'ariadne.pecchisilvrestrine@gmail.com',
            tel:'(16)99125-6178',
            cid:'Guariba-SP'
          },
          {
            name: 'LUAN HENRIKE DA SILVA JÚNIOR',
            idade:'17',
            emprego:'Analise e Desenvolimento de Sistemas',
            email:'luan.henrikedasilva@outlook.com',
            tel:'(16)99125-6178',
            cid:'Matão-SP'
          },
          {
           name: 'HELENE ROBERTA LEONHARDT',
            idade:'22',
            emprego:'Vue.js Developer Pleno',
            email:'hel.leonhardt@gmail.com',
            tel:'(16)99125-6178',
            cid:'Taquaritinga-SP'
          },
          {
            name: 'DIEGO MATHEUS DOS SANTOS DIONÍSIO',
            idade:'19',
            emprego:'Design',
            email:'dieg.matheus@outlok.com',
            tel:'(16)99125-6178',
            cid:'Araraquara-SP'
          },
        ],
      }
    },
    methods: {
   
    painel(){
      this.$router.push('/painel')
    }
    
  }
  }
</script>