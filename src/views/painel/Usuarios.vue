<template>
<div>
  <v-data-table
    :headers="headers"
    :items="desserts"
    sort-by="calories"
    class="elevation-1"
  >
    <template v-slot:top>
      <v-toolbar flat color="white">
        <v-toolbar-title>ADMINISTRADORES 2019</v-toolbar-title>
        <v-divider
          class="mx-4"
          inset
          vertical
        ></v-divider>
        <div class="flex-grow-1"></div>
        <v-dialog v-model="dialog" max-width="500px">
          <template v-slot:activator="{ on }">
            <v-btn color="primary" dark class="mb-2" v-on="on">Novo</v-btn>
          </template>
          <v-card>
            <v-card-title>
              <span class="headline">{{formTitle }}</span>
            </v-card-title>

            <v-card-text>
              <v-container>
                <v-row>
                  <v-col cols="12" sm="6" md="4">
                    <v-text-field v-model="editedItem.name" label="Nome"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <v-text-field v-model="editedItem.calories" label="Idade"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <v-text-field v-model="editedItem.fat" label="Telefone"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <v-text-field v-model="editedItem.carbs" label="Emprego"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" md="4">
                    <v-text-field v-model="editedItem.protein" label="Cidade"></v-text-field>
                  </v-col>
                </v-row>
              </v-container>
            </v-card-text>

            <v-card-actions>
              <div class="flex-grow-1"></div>
              <v-btn color="blue darken-1" text @click="close">CANCELAR</v-btn>
              <v-btn color="blue darken-1" text @click="save">SALVAR</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-toolbar>
    </template>
    <template v-slot:item.action="{ item }">
      <v-icon
        small
        class="mr-2"
        @click="editItem(item)"
      >
        Editar
      </v-icon>
      <v-icon
        small
        @click="deleteItem(item)"
      >
        Deletar
      </v-icon>
    </template>
    <template v-slot:no-data>
      <v-btn color="primary" @click="initialize">Reset</v-btn>
    </template>
  </v-data-table>
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

    data: () => ({
      dialog: false,
      headers: [
        {
          text: 'Nome ',
          align: 'left',
          sortable: false,
          value: 'name',
        },
        { text: 'Idade', value: 'idade' },
        { text: 'Cargo', value: 'emprego' },
        { text: 'E-mail', value: 'email' },
        { text: 'Telefone', value: 'tel' },
        { text: 'Usuário', value: 'usu' },
        { text: 'Editar adm', value: 'action', sortable: false },
      ],
      desserts: [],
      editedIndex: -1,
      editedItem: {
        name: '',
        tel:'' ,
        emprego:'' ,
        email:'' ,
        cid: '',
      },
      defaultItem: {
        name: '',
        tel:'' ,
        emprego: '',
        email:'' ,
        cid: '',
      },
    }),

    computed: {
      formTitle () {
        return this.editedIndex === -1 ? 'Novo' : 'Editar'
      },
    },

    watch: {
      dialog (val) {
        val || this.close()
      },
    },

    created () {
      this.initialize()
    },

    methods: {
      initialize () {
        this.desserts = [
          {
            name: 'ALINE IASMIM DA SILVA DAMIÃO',
            idade:'17',
            emprego:'Back-end Developer',
            email:'aline@contato.com',
            tel:'(16)99125-6178',
            usu:'Aline',

          },
          {
            name: 'SAMUEL PINHEIRO DA SILVA JÚNIOR',
            idade:'19',
            emprego:'Game Design',
            email:'samuel@contato.com',
            tel:'(16)99125-6178',
             usu:'Samuca',
          },
          {
            name: 'DAPHNE HELENA SILVA BERGO',
            idade:'26',
            emprego:'UI/UX Designer',
            email:'daphne@contato.com',
            tel:'(16)99125-6178',
             usu:'Delphine',
          },
          {
            name: 'JOSÉ AIRTON JÚNIOR',
            idade:'38',
            emprego:'Fullstack Developer',
            email:'junior@contato.com',
            tel:'(16)99125-6178',
             usu:'Junior',
          },
          {
            name: 'PRISCILA AGDA LUZIA MODESTO',
           idade:'18',
            emprego:'Front-end Developer Junior',
            email:'priscila@contato.com',
            tel:'(16)99125-6178',
             usu:'Priscil4o',
          },
          {
            name: 'LUÍS FERNANDO FANTE',
            idade:'18',
            emprego:'Data Base Analytics Sênior',
            email:'luisfante@contato.com',
            tel:'(16)99125-6178',
             usu:'Fante',
          },
          {
            name: 'VINÍCIUS TRONCO FAUSTO',
            idade:'18',
            emprego:'Fullstack Developer',
            email:'fausto@contato.com',
            tel:'(16)99125-6178',
             usu:'Fausto',
          },
          {
            name: 'ERICK PETRUCELLI',
            idade:'32',
            emprego:'Vue.js Developer Sênior',
            email:'erick@contato.com',
            tel:'(16)99125-6178',
             usu:'ADMIN',
          },
          {
            name: 'ANA CRISTINA ANTONELLI PEDRA',
            idade:'33',
            emprego:'I.T Suport',
            email:'ana.pedracristina@outlok.com',
            tel:'(16)99125-6178',
             usu:'Ana',
          },
          {
            name: 'RAYANE PAVLECHENKO ROMAVJ',
            idade:'23',
            emprego:'PHP Developer',
            email:'rayne@contao.com',
            tel:'(16)99125-6178',
             usu:'Rayray',
          },
        ]
      },

      editItem (item) {
        this.editedIndex = this.desserts.indexOf(item)
        this.editedItem = Object.assign({}, item)
        this.dialog = true
      },

      deleteItem (item) {
        const index = this.desserts.indexOf(item)
        confirm('Você realmente deseja deletar este administrador?') && this.desserts.splice(index, 1)
      },

      close () {
        this.dialog = false
        setTimeout(() => {
          this.editedItem = Object.assign({}, this.defaultItem)
          this.editedIndex = -1
        }, 300)
      },

      save () {
        if (this.editedIndex > -1) {
          Object.assign(this.desserts[this.editedIndex], this.editedItem)
        } else {
          this.desserts.push(this.editedItem)
        }
        this.close()
      },
        painel(){
      this.$router.push('/painel')
    },
    },
  }
</script>