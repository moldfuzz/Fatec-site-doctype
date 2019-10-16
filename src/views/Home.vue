<template>
  <div>
     <v-parallax
         dark
        src="../assets/universe-hackathon.png"
       >
      <v-row
      align="center"
      justify="center"
      
       >
      
      <h4 class="subheading display-3 text-center font-weight-black">Venha fazer parte do nosso time!</h4>
      <div class="text-center">
          <v-btn class="ma-5" outlined color="white">saiba mais</v-btn>
      </div>
      </v-row>
    
        </v-parallax>

  <body>
    <section class="servicos-section">
      <div class="inner-width">
        <h2 class="section-titulo">{O que fazemos}</h2>
        <p class="texto">
          Tudo feito com muito <strike>café</strike> amor e profissionalismo</p>
        <hr class="border"/>
        <div class="servicos-container">

          <div class="servico-box">
            <div class="servico-icon">
              <i class="fas fa-mobile-alt"></i>
            </div>
            <h3 class="servico-titulo">Apps</h3>
            <p class="servico-desc">
              Desenvolvemos de aplicativos e jogos para celulares dos sistemas Androind, iOS e Windows Phone.
            </p>
          </div>

          <div class="servico-box">
            <div class="servico-icon">
              <i class="fas fa-users"></i>
            </div>
            <h3 class="servico-titulo">Acessibilidade</h3>
            <p class="servico-desc">
              Nós da  &lt;!DOCTYPE&gt; acreditamos que todos os nossos clientes merecem uma boa experiência com nossos produtos. Assim, fornecemos serviços que contribuem para proporcionar ou ampliar a inclusão de pessoas com deficiência.  
            </p>
          </div>

          <div class="servico-box">
            <div class="servico-icon">
              <i class="fas fa-brain"></i>
            </div>
            <h3 class="servico-titulo">Inteligência artificial</h3>
            <p class="servico-desc">
              Criamos aplicações que aprendem a base de dados para lidarem com grande volume de informações seja por texto, voz ou fotos.
            </p>
          </div>

          <div class="servico-box">
            <div class="servico-icon">
              <i class="fas fa-file-alt"></i>
            </div>
            <h3 class="servico-titulo">Otimização de sites (SEO)</h3>
            <p class="servico-desc">
              Utilizamos do conjunto de técnicas SEO para deixar a pesquisa pelo seu site na primeira página em qualquer mecanismo de busca.
            </p>
          </div>
          <div class="servico-box">
            <div class="servico-icon">
              <i class="fas fa-code"></i>
            </div>
            <h3 class="servico-titulo">Sites</h3>
            <p class="servico-desc">
              Oferecemos os melhores serviços de criação e manutenção de sites responsivos (HTML e CSS) + um painel de controle (VueCli).
            </p>
          </div> 
          
          <div class="servico-box">
            <div class="servico-icon">
              <i class="fas fa-pen-fancy"></i>
            </div>
            <h3 class="servico-titulo">Webdesign</h3>
            <p class="servico-desc">
              Aplicamos fundamentos de Design para a criação de layouts para sites. Utilizando conhecimentos como Tipografia, Teoria das cores, Diagramação, Gestalt, entre outros.
            </p>
            </div>
            
        </div>
        </div>
    </section>
        <section class="projetos-destaques">
        <h2 class="section-titulo">{Projetos}</h2>
        <p class="texto">
        Igual aos nossos? pode procurar, não há!
        </p>
        <hr class="border"/>
        <div class="text-center">
<v-btn class="ma-5 text-center" outlined color="white">EU QUERO</v-btn>
        </div>
         
    </section>

      <section>
        <h2 class="section-titulo">{Palestras}</h2>
        <p class="texto">
          Buscamos incentivar cada vez mais os talentos escondidos no interior de São Paulo, compartilhando experiências, conhecimentos e sorrisos! 
        </p>
        <hr class="border"/>
      
  <v-card
    :loading="loading"
    class="mx-auto my-12"
    max-width="374"
  >
   

    <v-card-title> Entenda o universo SEO - Fatec Araraquara</v-card-title>
    <v-card-text>
      <v-row align="center">
        
      </v-row>

      <div class="my-4 subtitle-1 black--text">
        Salão Azul | Terça-feira
      </div>

      <div>A convidada Daphne Helena,CEO da &lt;!DOCTYPE&gt;, falará sobre o conjunto de técnicas SEO e seus benefícios além de ensinar a como pôr em prática.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>
    <v-card-text>
      <div class="title text--primary">Reserve seu horário!</div>
      <v-chip-group
        v-model="selection"
        active-class="deep-purple accent-4 white--text"
        column
      >
        <v-chip>09:30</v-chip>
        <v-chip>14:30</v-chip>
        <v-chip>18:30</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="deep-purple accent-4"
        text
        @click="reserve"
      >
        Reserve
      </v-btn>
    </v-card-actions>
  </v-card>

        
      </section>            
        
      
  </body>

  </div>
</template>

<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
    }),

    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
    },
  }
</script>

