<template>
  <div>

  <head>
    <meta charset="utf-8">
    <title></title>
    <link rel="stylesheet" href="style.css">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.1/css/all.css">
  </head>
  <body>
<header>
 <img class="logo" @click="inicial" src="../assets/logo_doctype.svg">
    <input type="checkbox" id="chk">
    <label for="chk" class="show-menu-btn">
      <i class="fas fa-bars"></i>
    </label>

    <ul class="menu">
      <a style="color:white;" @click="inicial">Início</a>
      <a style="color:white;"  @click="prj">Projetos</a>
      <a style="color:white;" @click="hack">Hackathon</a>
      <a style="color:white;" @click="sobre">Sobre</a>
      <a style="color:white;"  @click="contato">Contato</a>
      <a style="color:white;" @click="time">Login</a>
      <label for="chk" class="hide-menu-btn">
        <i class="fas fa-times"></i>
      </label>
    </ul>
</header>
   

  </body>

    <!-- <v-toolbar
   color="blue-grey darken-4  white--text">
       
      <v-toolbar-title @click="inicial"><!DOCTYPE></v-toolbar-title>

      <div class="flex-grow-1"></div>

      <v-toolbar-items>
        <v-btn class=" white--text" text @click="inicial">Início</v-btn>
        <v-btn class=" white--text" text @click="prj">Projetos</v-btn>
        <v-btn class=" white--text" text @click="hack">Hackathon</v-btn>
        <v-btn class=" white--text" text @click="sobre">Sobre Nós</v-btn>
        <v-btn class=" white--text" text @click="contato">Contato</v-btn>
        <v-btn class=" white--text" text @click="time">Usuário</v-btn>
      </v-toolbar-items>
    </v-toolbar> -->
</div>
  

</template>
<script>
export default {
methods: {
    inicial () {
      this.$router.push('/')
    },
    prj(){
      this.$router.push('/paginas/projetos')
    },
    hack(){
      this.$router.push('/paginas/hackathon')
    },
    sobre(){
      this.$router.push('/sobre')
    },
    contato(){
      this.$router.push('/paginas/contato')
    },
     time(){
      this.$router.push('/painel/login')
    }
    
  }
}
</script>

<style>
header{
  height: 100px;
  background: black;
  padding: 0 20px;
  color: #fff;
  display: flex;
}
.logo{
  line-height: 100px;
  justify-content: left;
  height: 100%;
  width: 90px;
}

.menu{
float: right;
  line-height: 100px;
}
.menu a{
  text-transform: uppercase;
  text-decoration: none;
  padding: 0 10px;
  transition: 0.4s;
}

.show-menu-btn,.hide-menu-btn{
  transition: 0.4s;
  font-size: 30px;
  cursor: pointer;
  display: none;
}
.show-menu-btn{
  float: right;
}
.show-menu-btn i{
  line-height: 100px;
}

#chk{
  position: absolute;
  visibility: hidden;
  z-index: -1111;
}

@media screen and (max-width:800px) {
  .show-menu-btn,.hide-menu-btn{
    display: flex;
  }
  .menu{
    z-index: 2;
    position: absolute;
    width: 100%;
    height: 500px;
    background: #333;
    right: -100%;
    top: 0;
    text-align: center;
    padding: 80px 0;
    line-height: normal;
    transition: 0.7s;
  }
  .menu a{
    display: block;
    padding: 20px;
  }
  .hide-menu-btn{
    position: absolute;
    top: 40px;
    right: 40px;
  }
  #chk:checked ~ .menu{
    right: 0;
  }
 
  .v-parallax{
    position: relative;
    z-index: -12000;
  }
 
}
</style>