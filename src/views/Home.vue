<template>
  <div>
     <v-parallax
         dark
        src="../assets/parralax-image.jpg"
       >
      <v-row
      align="center"
      justify="center"
      
       >
      
      <h4 class=".title display-3 text-center font-weight-black">Venha fazer parte da 12º do nosso #Hackathon!</h4>
        <h4 class="subtitle display-1 text-center font-weight-black">Não perca a chanche de fazer parte de nosso time!</h4>
      </v-row>
     
     <div class="text-center">
          <v-btn class="ma-5" outlined color="white">saiba mais</v-btn>
      </div>
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
        <div class="projetos-container">
          <div class="projetos-box">
            <div class="projetos-icon">
            <i class="fas fa-meteor"></i>
            </div>
        
            </div>
        </div>
        
          
        <p class="texto">
        Não deixe seu negócio entrar em extinção! venha para a &lt;!DOCTYPE&gt;
        </p>
        <hr class="border"/>
        <div class="text-center">
<v-btn class="ma-5 text-center" outlined color="white">VEJA COMO</v-btn>
        </div>
         
    </section>

      <section>
        <h2 class="section-titulo">{Onde estamos}</h2>
        <p class="texto">
          Adoraríamos te receber em nossa casa! 
        </p>
        <hr class="border"/>
        
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

